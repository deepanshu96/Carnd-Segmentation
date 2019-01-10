# Semantic Segmentation
### Files for the project submission
 - [helper.py](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/helper.py)
 - [main.py](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/main.py)
 - [project_tests.py](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/helper.py)
 - [Runs folder](https://github.com/deepanshu96/Carnd-Segmentation/tree/master/runs/1546951226.595684)
 - [Output youtube video link](https://www.youtube.com/watch?v=QbqBNXFpiAA)
### Introduction
In this project, I labeled the pixels of a road in images using a Fully Convolutional Network (FCN).

### Implementation
I implemented the main.py file in the code. The main functions that were implemented were load_vgg, layers, optimize, train_nn and run. In the load_vgg function the vgg model was loaded making up the encoding part of the convolutional network and in the layers function the decoding part was coded according to the below model:-

![alt text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/screens/Screen%20Shot%202019-01-10%20at%2010.56.59%20AM.png)

The hyperparameters that were used to train the network were:-
* keep probabilty = 0.5
* learning_rate = 0.00001
* standard deviation = 0.01
* L2 regularization = 1e-3
* Epochs = 25
* Batch size = 5

The training was able to reduce the overall loss after the the iterations, shown below:-

![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/screens/Screen%20Shot%202019-01-10%20at%2010.13.11%20AM.png)

The images from the dataset after 25 epochs which were labeled are shown below :-


![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/runs/1546951226.595684/um_000000.png)
![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/runs/1546951226.595684/um_000025.png)
![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/runs/1546951226.595684/um_000050.png)
![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/runs/1546951226.595684/um_000076.png)

I used udacity workspace for training the above model so the location of the data used by default in the workspace - /data.
The sample images of workspace is shown below :-

* ![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/screens/Screen%20Shot%202019-01-08%20at%206.14.31%20PM.png)
* ![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/screens/Screen%20Shot%202019-01-08%20at%206.12.57%20PM.png)
* ![alt_text](https://github.com/deepanshu96/Carnd-Segmentation/blob/master/screens/Screen%20Shot%202019-01-08%20at%206.13.03%20PM.png)

##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://www.cvlibs.net/download.php?file=data_road.zip).  Extract the dataset in the `data` folder.  This will create the folder `data_road` with all the training a test images.

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
