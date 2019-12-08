# Document-Scanner
Document Scanner using 2 approaches viz. Hough Transform &amp; Autoencoders
1. Photos - Original dataset for training
2. Annotations - XML files for annotations of document in the images
3. Maskedimages - Masks for the training images (Used in AutoEncoders)
4. Hough Images/Canny - Output of the images for the respective approach

This project was inspired by this: https://blogs.dropbox.com/tech/2016/08/fast-and-accurate-document-detection-for-scanning/

Training Dataset consists of training images as well as their augmented images (As sufficient data was not available)

1. Hough Transform
Pipeline for this approach:
    1. Opening operation on the image
    2. Gaussian Blurring
    3. Thresholding the images
    4. Laplacian edge detection
    5. Hough Transform

2. AutoEncoders
This approach needed masks for the images which were generated with help of annotation files and Generating_masks.ipynb

These masks were feeded to a 7 layered convolutional network with only 20 training epochs.
The results were better when compared with Hough Transform. 
