# COMP9517_9517Iku :microphone:
Welcome to COMP9517Iku code base! This repository contains the **source code** of the project and **instructions** on how to run our software! 

Hope you like it ! :smiley: :+1:

We have provided two approaches to adjust the COTS problem which are **YOLOv5** and **SVM + HoG**. They will be introduced on how to run it below.

## 1. YOLOv5
### Step 0
Please make sure you download/git-clone the latest version of [YOLOv5](https://github.com/ultralytics/yolov5) :smiley:

Do
e.g.,
```shell
    !git clone https://github.com/ultralytics/yolov5.git
```
in the current diretory.

### Step 1
Unzip the "Source code.zip", you will get two folders "hog+svm" and "YOLOv5", we choose the latter.

### Step 2
According to the video demonstration, there is a jupyter notebook written for YOLOv5 software demonstration. Now open the jupyter notebook in your favourite code editor. It is recommended to use [Anaconda](https://www.anaconda.com/) or [vscode](https://code.visualstudio.com/) with [Jupyter notebook extension](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) available.

### Step3
Change to **yolov5** directory, and then install all the requirements in order to run the software. 
```bash
%cd yolov5 
```
```bash
%pip install --user -qr requirements.txt
```
Then restart the kernal of the notebook, and change to **yolov5** directory again.

**PLEASE MAKE SURE YOU HAVE INSTALLED THE CORRECT VERSION OF PYTORCH, WE USE YOLOv5 torch-1.8.0**:exclamation::exclamation::exclamation:

### Step4
This will create a YOLOv5 notebook instance for all the subsequent operations.
```python
import torch
import utils
display = utils.notebook_init()
```

### Step5
There is no need to train the images again, unless you have custome dataset. We have provided the trained model [best.pt](YOLOv5\best.pt) in the submission. 

To run the inference, please run the following in the notebook,
```bash
!python detect.py --weight [pathToBest.pt] --source [pathToTestImages] --save-txt
```
Once the inferencing is finished, look for lines like **Results saved to [path]**, this is the folder where the inferenced result will be saved into.

## Note:
Since YOLOv5 has performed better than SVM, there will no instructions on how to use SVM, but we have provided the source code and experiments along the develoment for your information.

If you would like calculate average F2 score, please use /YOLOv5/F2_score.ipynb together with train.csv for calcualtion.

 Thank you :)