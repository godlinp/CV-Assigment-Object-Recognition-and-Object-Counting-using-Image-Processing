# CV-Assigment-Object-Recognition-and-Object-Counting-using-Image-Processing

This code is a Python script that uses the OpenCV library to detect and label objects in an image. Specifically, it identifies and counts phones, pens, and books in the given image. Below is an explanation of each section of the code along with some details:

## Importing Libraries

This section imports the necessary libraries for image processing, including OpenCV (cv2), numpy, and a function (`cv2_imshow`) from the Google Colab library for displaying images.

## Sample image with containing objects
The sample image is now available in the main branch.

## Object Detect: Phone

This describes describes on how to detect phones in the image:

1. The image is loaded using the cv2.imread('image.png') function.
2. Next, the loaded image is converted to the HSV color space, known for its effectiveness in color-based object detection.
3. Lower and upper color range values are defined for the phone. These values represent a range of hues (color), saturation, and value.
4. A mask is created to identify regions in the image that match the color range specified for the phone.
5. Morphological transformations  are then applied to the mask to enhance the detection of phones.
6. Using these techniques, the contours of identified phones are located.
7. Subsequently, respective bounding boxes are drawn around these regions and labeled for clear identification.
8. Finally, the number of detected phones is revealed alongside the image, concluding this stage of the process.


## Object Detect: Pens

This field describes on how to detect pens in the image:

1. The same image is loaded and converted to the HSV color space.
2. Lower and upper color range values are defined for the pen, representing a range of hues, saturation, and value.
3. A mask is created for the pen based on the specified color range.
4. Morphological operations are applied to the pen mask to enhance pen detection.
5. Contours of the detected pen regions are found.
6. Subsequently, respective bounding boxes are drawn around these regions and labeled for clear identification.
7. Finally, the number of detected pens is revealed alongside the image, concluding this stage of the process.

## Object Detect: Books

This field describes on how to detect books in the image:

1. The same image is loaded and converted to the HSV color space.
2. Lower and upper color range values are defined for books. In this case, there are multiple color range definitions for different shades of the book covers.
3. An empty mask for books is initialized, and the masks for different book shades are combined using a bitwise OR operation.
4. Morphological operations are applied to the book mask to enhance object detection.
5. Contours of the detected book regions are found.
6. Bounding boxes are drawn around the detected books, and labels are added to them.
7. The count of detected books is displayed along with the image.

## Display

At the end of each section, the script uses `cv2_imshow` to display the image with bounding boxes and labels around the detected objects.
To use this code, download the .pynb file and use "image.png" for testing purposes.
