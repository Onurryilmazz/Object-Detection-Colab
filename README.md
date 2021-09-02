# Object Detection with Colab

In this repository, the codes and outputs of the object detection application made using google colab were shared. Zombie detection was made with the model trained with zombie pictures taken from the internet in the notebook shared as Zombie detection. At the same time, an experiment was made with a zombie photo taken from a movie scene and a certain success was achieved.

## Files


|                |Files|                         |
|----------------|-------------------------------|-----------------------------|
|[images](https://github.com/Onurryilmazz/Object-Detection-Colab/tree/main/images "images")|`Folder with sample printouts`                        
|[Zombie_Detection.ipynb](https://github.com/Onurryilmazz/Object-Detection-Colab/blob/main/Zombie_Detection.ipynb "Zombie_Detection.ipynb")         |`File with source code"` 


> Note:  I used Tensorflow's Object Detection API to perform object detection on images.


## Model and Data

- Data : Data set consisting of zombie pictures produced in computer environment
- pre-trained model : ssd_resnet50
- data labeling : colab_utils.annotate

## Clone the Tensorflow Model Garden and Install Object  Detection API

```
 !git clone --depth 1 https://github.com/tensorflow/models/
 ```

```
!cd models/research/ && protoc object_detection/protos/*.proto --python_out=. && cp object_detection/packages/tf2/setup.py . && sed -i 's/>=2.5.1/==2.5.0/' setup.py && python -m pip install .
 ```

## Dataset preparation

When we download the dataset, it comes untagged. It needs to be labeled before giving it to the model. I used colab_utils.annotate function for this and tagged my data.

## Training 

After downloading the pre-trained model file, I made the appropriate changes for our problem through the config file that came. Then I created the model and Checkpoints. After making the inputs suitable for our model, I made it ready for the train phase.l.

## Results
![Result1](https://github.com/Onurryilmazz/Object-Detection-Colab/blob/main/images/zombie-anim%20(1).gif)

![Result2](https://github.com/Onurryilmazz/Object-Detection-Colab/blob/main/images/deneme.jpg)
