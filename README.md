# Detectify

# Abstract
Detectify is an Android application developed in Kotlin that utilizes the device's 
camera to detect real-time movement of objects. By analyzing pixel differences 
between frames, the app identifies changes and notifies the user when movement is 
detected. It features a user-friendly interface with multiple screens, including a 
home screen, an information screen, and a dedicated detection screen. The app 
demonstrates effective use of camera permissions, provides accurate movement 
detection, and offers potential for future enhancements such as image/video capture 
and integration with smart home devices.

# Introduction
Detectify is an Android application developed using Kotlin and Android Studio. 
The app utilizes the camera functionality of the device to detect movement of 
objects in real-time. When movement is detected, the app notifies the user by 
displaying a toast message. The app allows users to switch between different 
screens/pages, including a home screen, a page displaying information about the 
app, and a screen for detecting object movement.

# Features
The key features of the Detectify include:
• Real-time object movement detection using the device's camera.
• Display of a toast message when object movement is detected.
• Multiple screens/pages for user interaction.
• Ability to switch between different screens/pages.
• Permission handling for accessing the device's camera.
• Efficient image processing for detecting movement.
• Use of image comparison techniques to identify changes between frames.

# Project Structure
The project follows a standard Android project structure created in Android
Studio. The main components of the project structure are:
• MainActivity: serves as the entry point of the application and manages 
the navigation between different screens/pages.
• detect_movement.xml: XML layout file defining the UI for the object 
movement detection screen.
• activity_main.xml: XML layout file defining the UI for the home 
screen.
• about.xml: XML layout file defining the UI for the information screen.
• Camera2API: handles the camera functionality, including opening the 
camera, capturing frames, and processing images for movement 
detection.
• convertImageToBitmap(): converts the captured Image object into a 
Bitmap for image processing.
• detectMovement(): compares the current and previous frames to detect 
movement by calculating the pixel differences.
• getPermission(): checks and requests the necessary camera permission 
from the user.
• onRequestPermissionsResult(): handles the result of the permission 
request.
• openCamera(): opens the camera and sets up the capture session.
• onImageAvailableListener(): processes the captured image frames and 
detects object movement.
• page0(), page1(), page2(): methods for switching between different 
screens/pages.

# Implementation Details
The Detectify utilizes the Camera2 API for accessing the device's camera and capturing 
frames. The captured frames are processed using image comparison techniques to identify 
changes in pixel values. By calculating the pixel differences, the app determines whether object 
movement is detected. The UI is updated accordingly, displaying a toast message when 
movement is detected.
The TextureView class is used to display the camera preview on the screen. The ImageReader
class is employed to obtain the frames captured by the camera. The captured frames are 
converted to Bitmap objects using the convertImageToBitmap() method for image processing.
The detectMovement() method compares the current frame with the previous frame to calculate 
the pixel differences. If the number of different pixels exceeds a defined threshold, object 
movement is considered to be detected. A toast message is then displayed using the 
runOnUiThread() method to notify the user.
The app handles camera permission requests using the getPermission() method, which checks 
if the required permission is granted. If not, it requests the permission from the user using the 
requestPermissions() method. The result of the permission request is handled in the 
onRequestPermissionsResult() method.

# Conclusion
The Object Movement Detection App is a practical application that demonstrates 
real-time object movement detection using the camera functionality of an Android 
device. It provides a user-friendly interface and effectively notifies the user when 
object movement is detected. The app can be further enhanced by adding additional 
features such as capturing and saving images/videos, adjusting detection sensitivity, 
and integrating with other smart home devices.
