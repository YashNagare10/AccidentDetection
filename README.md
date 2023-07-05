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
