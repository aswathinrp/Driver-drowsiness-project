# Driver-drowsiness-project
Driver-Drowsiness-Detection
Driver drowsiness detection is a project built using Dlib and OpenCV with Python as a backend language.
Logic of project
The project includes direct working with the 68 facial landmark detector and also the face detector of the Dlib library. The 68 facial landmark detector is a robustly trained efficient detector which detects the points on the human face using which we determine whether the eyes are open or they are closed.
![Screenshot (12)](https://user-images.githubusercontent.com/90610747/227428900-c1ecaa0c-f5ff-4b98-b406-9fbb665a840a.png)

Working :


This code uses OpenCV and dlib libraries to detect faces and track eye blinks in real-time from a webcam feed. The code starts by importing the necessary libraries, which are OpenCV for image processing, NumPy for array related functions, and dlib for face landmark detection. The code also imports "face_utils" from the "imutils" library, which contains basic operations of conversion.

Then, it initializes the camera and takes the instance of it. It also initializes the face detector and landmark detector using the dlib library. The "shape_predictor_68_face_landmarks.dat" file is used for face landmark detection.

The script then defines a function "compute" that calculates the distance between two points in the 2D space. Another function called "blinked" calculates the eye aspect ratio to detect eye blinks.

The main part of the code is the while loop that runs indefinitely, continuously reading the frames from the camera. The frames are converted to grayscale, and then the face detector is applied to detect faces in the frame. For each detected face, a rectangle is drawn around it. The face landmark detector is then applied to detect the eye landmarks, and the blinked function is called to determine whether the eyes are open, partially closed, or closed.

Based on the eye aspect ratio, the script determines whether the user is sleeping, drowsy, or active. If the eyes are closed for an extended period, the status is set to "SLEEPING !!!" and the color of the text is set to red. If the eyes are partially closed, the status is set to "Drowsy !" and the color of the text is set to blue. If the eyes are open, the status is set to "Active :)" and the color of the text is set to green. The text status is then displayed on the frame, and the landmarks are drawn on the face frame.

Finally, the frames are displayed on the screen until the user presses the "Esc" key, which breaks the loop and terminates the program.
