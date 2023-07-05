# AccidentDetection
A system which is able to detect an accident from video footage provided to it using a camera.
The System is designed as a tool to help out accident victims in need by timely detecting an accident and henceforth informing the authorities of the accident.

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
