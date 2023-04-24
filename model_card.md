# Model Card

See the [example Google model cards](https://modelcards.withgoogle.com/model-reports) for inspiration. 

## Model Description

**Input:** The model takes a neural network, a device and an image in PIL format as an input. The neural network can be generated using a number of input channels (depending on the image data type - e.g. one channel for grayscale images) and a number of output categories (e.g. two for "particle" vs. "background").

**Output:** It returns a segmented image in the form of an array with the same shape as the input image. The neural network returns loadable checkpoint files of type .pth.

**Model Architecture:** Unet: see https://doi.org/10.48550/arXiv.1505.04597

## Performance

I used data from the same source as the training data to test the model (600 images, 50% of the available unblurred dataset). The F1 score, calculated on a pixel by pixel basis, was 0.972 for a higher learning rate (10^-3) and 0.979 for a lower one (10^-5).

## Limitations

It looked like the data in the training set was exclusively well-defined bright particles on a dark background, and all were simulated using the same software. I'm not sure the model would work well on image data that isn't similar. Also, it can only identify one class of particles.

## Trade-offs

I think the model would struggle with images that contain non-dark backgrounds, such as carbon supports in electron microscopy, or bright-field images.
