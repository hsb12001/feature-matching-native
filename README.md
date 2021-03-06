# Augmented Reality Feature Matching using the NDK with an async approach for >= Android 4.0

<img src="/featurematchingnative.png" alt="Feature matching native" width="400px"/>

### What is this repository for?
* Uses the camera image to search for a specified template image within it via a feature matching approach using the OpenCV C++ library. The detected object is marked with lines within the scene. This can be used to e.g. find a logo.
* uses an async approach, that means that not every frame will be searched for the object and the GUI stays fluent/responsible
* the OpenCV Java library is used as well for loading the template image. The processing on the other hand is done by the OpenCV C++ library only. 
* currently the async calculated image is painted over the live camera preview which can be seen on the edge. This might be changed in the future.
* Version 1.1

### How do I get set up?
* IDE: Android Studio (tested with 2.2.2)
* Android SDK & NDK
* Dependencies: OpenCV 3.0.0 library (included)
* Template image location: res/drawable Changeable in CameraPreviewView
* Make sure the app has the required permission on start, as there is no runtime-check yet! (Camera)

### Default template image
<img src="/app/src/main/res/drawable/coca_cola.bmp" alt="" width="200px"/>

Copyright of the logo: The Coca-Cola Company

### Who do I talk to?
* Repo owner and developer: android@michaeltroger.com

### Credits
* The passing of the camera frame data from Java to C++ and the async approach is based on Jay Rambhia's AsyncCamera  https://github.com/jayrambhia/AsynCamera
* The feature matching is based on this official OpenCV tutorial http://docs.opencv.org/2.4/doc/tutorials/features2d/feature_homography/feature_homography.html Unlike in this application their version is using OpenCV 2 and is for use with normal images
* This C++ library integration builds on code from the Android Open Source Project: https://github.com/googlesamples/android-ndk/tree/master/hello-libs
