# 🧑‍🤝‍🧑 Gender and Age Detection 👨‍👩‍👧‍👦

## ℹ️ About the Project:

In this Python Project, I used Deep Learning to accurately identify the gender and age of a person from a single image of a face. I used models trained by [Tal Hassner and Gil Levi](https://talhassner.github.io/home/projects/Adience/Adience-data.html). The predicted gender may be one of ‘Male’ 👨 and ‘Female’ 👩, and the predicted age may be one of the following ranges: (0 – 2), (4 – 6), (8 – 12), (15 – 20), (25 – 32), (38 – 43), (48 – 53), (60 – 100) (8 nodes in the final softmax layer). It is very difficult to accurately guess an exact age from a single image because of factors like makeup 💄, lighting 💡, obstructions, and facial expressions. And so, I made this a classification problem instead of making it one of regression.

## 💾 Dataset:

For this python project, I used the Adience dataset; the dataset is available in the public domain and you can find it [here](https://www.kaggle.com/ttungl/adience-benchmark-gender-and-age-classification). This dataset serves as a benchmark for face photos and is inclusive of various real-world imaging conditions like noise, lighting, pose, and appearance. The images have been collected from Flickr albums and distributed under the Creative Commons (CC) license. It has a total of 26,580 photos of 2,284 subjects in eight age ranges (as mentioned above) and is about 1GB in size. The models I used had been trained on this dataset.

## 🐍 Additional Python Libraries Required:

* OpenCV
    ```bash
    pip install opencv-python
    ```
* argparse
    ```bash
    pip install argparse
    ```

## 📂 The contents of this Project:

* `opencv_face_detector.pbtxt`
* `opencv_face_detector_uint8.pb`
* `age_deploy.prototxt`
* `age_net.caffemodel`
* `gender_deploy.prototxt`
* `gender_net.caffemodel`
* `detect.py`

For face detection, we have a `.pb` file - this is a protobuf file (protocol buffer); it holds the graph definition and the trained weights of the model. We can use this to run the trained model. And while a `.pb` file holds the protobuf in binary format, one with the `.pbtxt` extension holds it in text format. These are TensorFlow files. For age and gender, the `.prototxt` files describe the network configuration and the `.caffemodel` file defines the internal states of the parameters of the layers.

## ⚙️ Usage:

1.  Download my Repository ⬇️
2.  Open your Command Prompt or Terminal and change directory to the folder where all the files are present. 💻
3.  **Detecting Gender and Age of face in Image** Use Command:
    ```bash
    python detect.py --image <image_name>
    ```
    **Note:** The Image should be present in the same folder where all the files are present. 🖼️
4.  **Detecting Gender and Age of face through webcam** Use Command:
    ```bash
    python detect.py
    ```
5.  Press `Ctrl + C` to stop the program execution. 🛑

## 🖼️ Examples:

![Screenshot 2025-04-30 212323](https://github.com/user-attachments/assets/e2311913-1a3f-48f6-a94f-9cb3b6d0f23e)
![Screenshot 2025-04-30 212932](https://github.com/user-attachments/assets/3da0d99e-d796-4b59-b10b-04ffd0d06e4d)
![Screenshot 2025-04-30 212500](https://github.com/user-attachments/assets/26c0c13f-fc74-4f4f-82c9-e4b77a1e3333)

