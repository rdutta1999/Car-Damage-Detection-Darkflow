# Car-Damage-Detection-Darkflow

This repo goes through the process of setting up Darkflow, and using it to train a custom object detection model. Here, I have trained a Car Damage Detection model, that identifies Scratches and Dents and draws a bounding box around it. **Training.ipynb** contains the source code, and the trained model weights can be found [here](https://drive.google.com/drive/folders/1bc0z6HkcAEBRRpk0Y0UGTyjCxe9xfG2K?usp=sharing). 

## Setting Up:-
1) Create a new Python/Anaconda enviroment (optional but recommended).

2) Install the necessary packages:-
    - ```conda install numpy pandas matplotlib opencv cython jupyter```
    - If you have a supported GPU, run ```conda install tensorflow-gpu=1.14```
    - If you don't have a supported GPU or want to train on a CPU, run ```conda install tensorflow=1.14```
    
3) Clone the [Darkflow](https://github.com/thtrieu/darkflow) repository into your working directory and run ```cd darkflow```.

4) Setup darkflow and build the Cython extensions.
    - ```pip install .```
    - ```python setup.py build_ext --inplace```
    
5) Download the yolo weights from [here](https://drive.google.com/drive/folders/0B1tW_VtY7onidEwyQ2FtQVplWEU) and again place in the working directory. More info in the .ipynb file.

6) From the [Object Detection Metrics](https://github.com/rafaelpadilla/Object-Detection-Metrics) repository, download and copy the following into the working directory:- 
    - pascalvoc.py
    - _init_paths.py
    - lib module
    
7) Place the dataset in the following manner:- 
<pre>
├─── darkflow
     ├─── ..
     ├─── ..     
     ├─── cfg
     ├─── lib
     ├─── test_imgs
     ├─── pascalvoc.py
     ├─── _init_paths.py
     ├─── labels.txt
     ├─── Training.ipynb 
     ├─── yolo.weights
     ├─── data
          ├─── annotations
               ├─── annot1.xml
               ├─── annot2.xml
               ├─── annot3.xml
               ├─── annot5.xml
               ├─── annot6.xml
               ├─── ..
               ├─── ..
               └─── ..
           └─── images
               ├─── img1.jpg
               ├─── img2.jpg
               ├─── img3.jpg
               ├─── img4.jpg
               ├─── img5.jpg
               ├─── ..
               ├─── ..
               └─── ..
</pre>

## Outputs
![Pic1](/test_imgs_output/download.png?raw=true)
![Pic2](/test_imgs_output/download1.png?raw=true)
![Pic3](/test_imgs_output/download2.png?raw=true)

## References
- https://github.com/thtrieu/darkflow


- https://github.com/pjreddie/darknet


- https://towardsdatascience.com/yolov2-to-detect-your-own-objects-soccer-ball-using-darkflow-a4f98d5ce5bf


- https://github.com/deep-diver/Soccer-Ball-Detection-YOLOv2


- https://github.com/deep-diver/Object-Detection-YOLOv2-Darkflow


- https://medium.com/@jonathan_hui/map-mean-average-precision-for-object-detection-45c121a31173


- https://github.com/rafaelpadilla/Object-Detection-Metrics
