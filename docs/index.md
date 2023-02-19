#Face Mask Detection using Deep Learning

This project is designed to detect whether a person is wearing a face mask or not in real-time using deep learning. The project is built using the TensorFlow deep learning framework and OpenCV for real-time video processing.
##Project Structure

The project has the following structure:

css

face-mask-detection/
├── dataset/
│   ├── with_mask/
│   └── without_mask/
├── trained-model/
├── detect_mask_video.py
├── train_mask_detector.py
├── haarcascade_frontalface_default.xml
└── README.md

The dataset/ directory contains two subdirectories: with_mask/ and without_mask/. These directories contain images of people wearing and not wearing masks, respectively. The trained-model/ directory contains the trained deep learning model. The detect_mask_video.py script is used to detect face masks in real-time using a web camera. The train_mask_detector.py script is used to train the deep learning model on the dataset. The haarcascade_frontalface_default.xml file is a pre-trained face detection model.
##Requirements

The project requires the following dependencies to be installed:

    Python 3.6 or above
    TensorFlow 2.0 or above
    OpenCV 4.2 or above
    NumPy
    Matplotlib

##Usage
Training the model

To train the deep learning model, run the following command:

css

python train_mask_detector.py --dataset dataset --model trained-model/mask_detector.model

This command will use the images in the dataset/ directory to train the model and save the trained model to the trained-model/ directory.
Detecting face masks in real-time

To detect face masks in real-time using a web camera, run the following command:

css

python detect_mask_video.py --model trained-model/mask_detector.model --cascade haarcascade_frontalface_default.xml

This command will start the video stream and detect face masks in real-time. When a person is detected wearing a mask, the bounding box around the face will be green, and when a person is detected not wearing a mask, the bounding box will be red.
Conclusion

This project demonstrates how to use deep learning to detect face masks in real-time. The project can be extended to detect face masks in images, videos, or in other scenarios such as in public places, hospitals, and schools.
