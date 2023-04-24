## Motivation

The BBBC datasets were curated in 2012 by Vebjorn Ljosa, Katherine L Sokolnicki and Anne E Carpenter at the Broad Institute of Massachusetts Institute of Technology and Harvard to help developers of new algorithms test them against a common collection of images and ground truths. This particular dataset was designed to help understand the effects of defocusing on the segmentation of cellular objects in imagesm for which simulated images were created with varying degrees of defocusing.

The work on the collection of datasets was funded by US National Institutes of Health grant R01 GM089652.
 
## Composition

The dataset consists of image data (.tif). There are 1200 images of width 696 pixels and height 520 pixels for each level of blurring, and 1200 ground truth images. No confidential information is included.

## Collection process

The data was produced using publicly available image simulation software (SIMCEP: Lehmussola et al., IEEE T. Med. Imaging, 2007 and Lehmussola et al., P. IEEE, 2008). I used the unblurred subset of the dataset.

## Preprocessing/cleaning/labelling

As the data was simulated, no preprocessing, cleaning or labelling was necessary.

## Uses

The dataset could be used to investigate the effect of blurring (by defocusing) on image segmentation accuracy.
Models trained on this dataset may not generalize well to data that is not similar to the training data, for example images with lower contrast or where there should be more than two output classes.

## Distribution

The dataset is publicly and freely available.

## Maintenance

At the time of publication, the collection of datasets was maintained by the authors of the publication (Vebjorn Ljosa, Katherine L Sokolnicki and Anne E Carpenter).
