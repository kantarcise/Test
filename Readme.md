Deep Performance Evaluation Tool with Using YOLO (Ana başlık)


In this project we aimed to report the performance of YOLO on COCO dataset. In COCO dataset there are approximately 81k training images and 41k validation images. Detailed descriptions can be found from the COCO dataset's homepage (buraya linkinin köprüsü kurulursa iyi olur http://cocodataset.org/#home). 

I used YOLOv3-608 model to see how YOLO provides performance in training and validation photos. I chose this model because if we look at other models of YOLO, we can observe that YOLOv3-608 is better than other models according to homepage of YOLO (buraya linkinin köprüsü kurulursa iyi olur https://pjreddie.com/darknet/yolo/). I used darknet, which is the backbone of YOLO with python interpreter. Also I used OpenCV library with python interpreter. 

The steps of making the project can be divided into 3, which are: getting ground truth (GT) information from COCO dataset and obtaining photo names, extraction of predictions which are made by YOLO for training and validation photos, and looking performance of YOLO with reporting YOLO's predictions according to ground truth data. (madde madde yazılırsa güzel olur).


Installing Neccessary Environments (alt başlık)

For using codes in this file, you must install neccessary libraries. For installing them, you can write terminal to
pip3 install -r requirements.txt (bunu madde halinde yazarsak iyi olabilir)
and all environments will install automatically. Also we use ipython notebook while looking performance on YOLO. If you want to use it, you must install Jupyter Notebook. For installing it you can write terminal to
pip3 install jupyter (madde halinde olabilir)
and it will install automatically.


Adjusting the Ground Truth and Image Id Files (alt başlık)

For arranging this files, I write a python script and with using them we can obtain these files. You can find this script in reciprosity files. It's name is CocoAnnoations.py. Before using this code, you must set annotation files path and you must enter the annotation file name (train or val) with changing target variable.
After adjusting python file you can run this script with writing terminal to 
python3 CocoAnnotations.py (madde halinde olabilir)


Running YOLO for Getting Predictions (Alt başlık)

For getting appropriate results you can use code which is in the YoloPrediction.py. For using it you must use image id txt which is created in previous step. Also you must change paths in the code and give true directory of YOLO config file and YOLO weight file. After setting these variables you can run the code with writing terminal to
python3 YoloPrediction.py


Running Evaluation Tool For Obtaining YOLO Performance (Alt Başlık)

For running evaluation tool we can use Evaluate_Models.ipynb which is in the directory of evaluation. We must copy training files which are ground truth and prediction of YOLO into trainglogs and validation files into vallog. If you want to skip first and second step, you can use the files which are in the YOLO-Files. I added my results for training in the trainlogs and for validation in the vallog file. 
