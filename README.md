# FaceScan-Facial-Recognition
Datasets images:
https://drive.google.com/drive/u/0/folders/0AHAbXKiPY3KQUk9PVA


"Description":

Personalized facial recognition attendance system. leverages advanced facial recognition technology to streamline and automate attendance processes. Utilizing a pre-trained deep learning model, this system identifies individuals quickly and accurately, ensuring reliable attendance tracking for educational or corporate settings. It's designed to integrate seamlessly with existing attendance management systems, providing real-time updates and data integrity.

 [Presentation](https://www.canva.com/design/DAGV_U9t8B4/NUe4PyrqZ9HCci0PYnpOlg/edit?utm_content=DAGV_U9t8B4&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)




 # FaceScan-Facial-Recognition

A personalized facial recognition attendance system that leverages advanced deep learning technologies to streamline and automate attendance tracking processes.

## Description

This system identifies individuals quickly and accurately by utilizing pre-trained deep learning models (FaceNet and MTCNN), ensuring reliable attendance tracking for educational or corporate settings. It's designed to integrate seamlessly with existing attendance management systems, providing real-time updates and data integrity.

## Features

- **Real-time Face Detection**: Uses MTCNN (Multi-task Cascaded Convolutional Networks) for accurate face detection
- **Advanced Face Recognition**: Implements FaceNet model for facial feature extraction and matching
- **Video Processing**: Supports multiple video formats (mp4, avi, mov, mkv)
- **Batch Processing**: Efficiently processes video frames at intervals for optimal performance
- **Attendance Tracking**: Automatically generates attendance records in Excel format
- **Web Interface**: User-friendly Flask-based interface for video upload and processing
- **Secure Processing**: Includes confidence thresholds to ensure accurate recognition
- **Export Functionality**: Downloads attendance records in Excel format

## Technical Stack

- **Backend Framework**: Flask
- **Face Detection**: MTCNN
- **Face Recognition**: FaceNet
- **Machine Learning**: SVM (Support Vector Machine) for classification
- **Data Processing**: NumPy, Pandas
- **Computer Vision**: OpenCV
- **Frontend**: HTML/CSS with Bootstrap
- **Tunneling**: ngrok for development access

## Prerequisites

- Python 3.7+
- pip package manager
- CUDA-compatible GPU (recommended for better performance)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Anasmahmoud00/FaceScan-Facial-Recognition
cd FaceScan-Facial-Recognition
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Install additional dependencies:
```bash
pip install mtcnn
pip install keras-facenet
pip install pyngrok
```

4. Set up ngrok:
- Sign up for ngrok account
- Get your authentication token
- Replace the token in the code with your token

## Usage

1. Start the application:
```bash
python facescan_code.py
```

2. Access the web interface:
- The application will provide a ngrok URL in the console
- Open the URL in a web browser
- Upload a video file containing faces to be recognized
- View results and download attendance records

## Dataset Structure

The training data should be organized as follows:
```
train/
    person1/
        image1.jpg
        image2.jpg
    person2/
        image1.jpg
        image2.jpg
val/
    person1/
        image1.jpg
    person2/
        image1.jpg
```

## Model Training

1. Place your training images in the appropriate directory structure
2. Run the face extraction process
3. Generate embeddings using FaceNet
4. Train the SVM classifier
5. Save the models for inference

## File Structure

```
FaceScan-Facial-Recognition/
├── facescan_code.py        # Main application file
├── facenet_svc_model.pkl   # Trained SVM model
├── facenet_label_encoder.pkl # Label encoder
├── temp_uploads/           # Temporary storage for uploaded videos
├── downloads/             # Storage for generated attendance sheets
└── requirements.txt       # Project dependencies
```

## Security Considerations

- Video files are processed and immediately deleted after recognition
- Confidence threshold implemented to prevent false positives
- Secure file handling with extension validation
- Maximum file size limit enforced

## Performance Optimization

- Frame interval processing to reduce computation load
- Minimum detection threshold for reliable recognition
- Memory-efficient video processing
- Batch processing of video frames

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



## Acknowledgments

- FaceNet team for the face recognition model
- MTCNN developers for the face detection implementation
- Flask team for the web framework
- OpenCV community for computer vision tools

