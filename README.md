# AccidentDetection
A system which is able to detect an accident from video footage provided to it using a camera.
The System is designed as a tool to help out accident victims in need by timely detecting an accident and henceforth informing the authorities of the accident.

# How to run
1. Download project zip file, unzip it.
2. Create folder with name mydata inside AccidentDetection and add two sub-directories test_set and training_set.
3. Create two folders accident and no_accident inside test_set and training_set.
4. Download dataset from kagle https://www.kaggle.com/datasets/ckay16/accident-detection-from-cctv-footage.
5. Move images from dataset directories data -> test -> accident to test_set -> accident and data -> test -> non accident to test_set -> no_accident.
6. Similarly do it for images in data -> train folder.
7. Then install required python libraries (flask, flask_sqlalchemy, flask_login, matplotlib, opencv, tensorflow, twilio) using command pip install <package-name>.
8. Then to run use command python mySite.py.
9. To get messages on accident detection create account on Twilio, and replace account_sid and auth_token in supportedFile.py with one you got from your twilio account.
10. Then uncomment and replace from and to numbers in predict() method in supportedFile.py.
   
# Result of project
# 1. When Accident is detected

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/aecbe938-29f2-4942-b0ce-705e56668d39)

# 2. No Accident detected

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/5b681284-ccc6-477c-9984-9b1a774373fb)

# Algorithm
CNN (Convulational Neural Network) is a Deep Learning algorithm which can take in an input image, assign importance (learnable weights and biases) to various aspects/objects in the image and be able to differentiate one from the other.
Architecture of CNN:
![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/24ca7029-faa9-4a02-a4b2-48e2fcb22a6c)

There are three steps in CNN
# 1. Convolutional Layer
Convolutional is the first layer to extract features from an input image. Convolutional preserves the relationship between pixels by learning image features using small squares of input data. It is a mathematical operation that takes two input such as Image matrix and a filter or kernel.

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/d3a7cdf5-daa2-4e3d-b8db-9bab459d954e)

Consider a 5 x 5 whose image pixel values are 0, 1 and filter matrix 3 x 3 as shown in below.

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/29c2b2d0-5714-4bd3-b797-611e9a8fa491)

Then the convolution of 5 x 5 image matrix multiplies with 3 x 3 filter matrix which is called “Feature Map” as output shown in below.

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/e78e7f81-6c1d-4527-8714-bd6fda55929c)

# 2. Filter Matrix/Kernel
Convolution of an image with different filters can perform operations such as edge detection, blur and sharpen by applying filters. The below example shows various convolution image after applying different types of filters (Kernels)

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/43ca80ca-c86f-4af6-ba82-21d526860d4c)

# 3. ReLU
ReLU stands for Rectified Linear Unit for a non-linear operation. The output is ƒ(x) = max(0,x).

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/a89cc700-bc25-43e0-ba53-a69b1c06a9de)

# 4. Pooling
Pooling layers section would reduce the number of parameters when the images are too large.
Max Pooling
Average Pooling
Sum Pooling

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/2cd248e0-18d7-4451-9cd0-7c7c37032411)

# 5. Fully Connected Layer
The layer we call as FC layer, we flattened our matrix into vector and feed it into a fully connected layer like a neural network.

![image](https://github.com/YashNagare10/AccidentDetection/assets/88041908/a5deb5f7-45e8-4d82-9b45-21c5b98aeafd)
