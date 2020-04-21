# BackgroundRemoval
BackgroundRemoval is an application that allows taking pictures then holding onto human subjects and erasing the background. Application uses Machine Learning model to predict and delete the background.

## Library
The application has a library package. There are 4 main components:
-VisionPredictor: used to manage and execute the model
-VisionImage: process captured images to prepare for the prediction of model
-OnDeviceModel: contains information and load model file for prediction
-VisionResult: Access to the results of the prediction

Class VisionPredictor handles all the complex processing associated with running a model on a device, including pre-processing - these are necessary operations to prepare images to format the input for the model. ) and post-processing (post-processing output from the model to get the desired result)
For each predictor containing the predict method take VisionImage as argument and return it as VisionResult

## Setting
Clone project to the device and run the application
When opening the application for the first time, the application will download the model and save it in the internal memory of the device with the name viettelbackgroundremoval.tflite
Then the application will switch to the camera screen to take a picture
User can switch between camera before and after to take pictures by pressing the toggle button at the right bottom of the screen
at the screen the camera will have the line dashed, which is located on top someone
after the shooting, The application will display the image with the Delete Font button.
When the Delete Font button is clicked, the background is deleted and the background is converted to gray-white color.
