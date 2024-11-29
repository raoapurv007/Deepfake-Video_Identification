# Deepfake-Video_Identification
  Our project is a Deep learning project which is a sub branch of Artificial Intelligence
 and deals with the human brain inspired neural network technology. Computer vi
sion plays an important role in our project. It helps in processing the video and
 frames with the help of Open-CV. A PyTorch trained model is a classifier to classify
 the source video as deepfake or pristine.

 Tn this we use convolutional neural network for analysis of a video.

 # Libraries Used
 1. **torch :**  The fundamental Python library for machine learning, providing tensor computations, automatic differentiation, and neural network building blocks.

 2. **torchvision :** A collection of datasets, models, and transforms commonly used for computer vision tasks, including image classification, object detection, and semantic segmentation. It's particularly useful for loading and preprocessing image data.

 3. **os :** Provides a way to interact with the operating system, such as file and directory operations, environment variables, and system-specific functionalities.

 4. **numpy:** A library for numerical computations, essential for handling numerical arrays and matrices. It's used for efficient array operations, linear algebra, and mathematical functions.

 5. **cv2:** A comprehensive computer vision library for tasks like image and video processing, object detection, and face recognition. It provides functions for reading, writing, and manipulating images, as well as implementing image processing algorithms.

 6. **matplotlib:** A plotting library for creating static, animated, and interactive visualizations. It's useful for visualizing data, such as image plots, histograms, and scatter plots.

 7. **face_recognition:** A library specifically designed for face recognition, providing functions for face detection, face encoding, and face comparison. It can be used to extract facial features, which are crucial for identifying potential manipulations in deepfake images.

 8. **json:** A library for working with JSON data, which is a common format for storing and exchanging data. It can be used for configuration files, storing model parameters, or other data serialization needs.

 9. **pandas:** A data analysis and manipulation tool, often used for data cleaning, exploration, and analysis. It can be useful for handling metadata, labels, and other tabular data related to the deepfake images.

 10. **copy:** Provides functions for copying objects, useful for creating copies of data structures without modifying the originals.

 11. **glob:** A library for finding files matching specific patterns, useful for organizing and accessing large datasets of images.

 12. **random:** A library for generating random numbers, which can be used for tasks like data shuffling, random sampling, or initializing model parameters.

 13. **sklearn:** A versatile machine learning library that offers various algorithms for classification, regression, clustering, and other tasks. It can be used for training and evaluating deepfake detection models, as well as for feature engineering and model selection.

# Images

**Initial Interface**


![2 (6)](https://github.com/user-attachments/assets/a31d91c3-2064-458f-aeb8-009ca0c6b1ea)



**Frames Splitting**


![2 (4)](https://github.com/user-attachments/assets/0c5ab52a-0806-4639-bf5d-06a8e2e57946)



**Output**



![2 (5)](https://github.com/user-attachments/assets/ffd2c77e-a2ad-47f9-8fca-aef9b786e2b4)


# Algorithm Details

 **ResNext CNN :** The pre-trained model of Residual Convolution Neural Net
work is used. The model name is resnext50_32x4d()[22]. This model consists
 of 50 layers and 32 x 4 dimensions. Figure shows the detailed implementation
 of model

 **LSTM Layer :** LSTM is used for sequence processing and spot the temporal
 change between the frames.2048-dimensional feature vectors is fitted as the
 input to the LSTM. We are using 1 LSTM layer with 2048 latent dimensions
 and 2048 hidden layers along with 0.4 chance of dropout, which is capable to
 do achieve our objective. LSTM is used to process the frames in a sequential
 manner so that the temporal analysis of the video can be made, by comparing
 the frame at ‘t’ second with the frame of ‘t-n’ seconds. Where n can be any
 number of frames before t.

