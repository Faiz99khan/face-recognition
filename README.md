# Face Recognition
It recognizes face at real time as well as in image with very good accuracy. It consist of FaceNet deep learning model and SVM statistical model.  Now, it is built on small database, database consists of 8 people(5 bollywood actors, 2 my brothers and me), but it can be extended easily on large no. of people. It can be used in attendance system, person tagging in the photo and in other related applications by making some modification in it.

## test model
### - image
![](prediction/test1.jpg)
<img src="prediction/test2.jpg" width="500" height="515" >
![](prediction/after_add_hritik.jpg)


### - real-time
![](prediction/test_realtime.gif)

It shows some lags because my laptop has low configuration.

## working
First, The dataset is created by collecting around 15-25 solo photos of each person in different pose, orientation and lighting conditon.Then, faces are extracted from all these photos by using **MTCNN library**. After that, these face images convert into embeddings representation by using state of the art **Facenet-Keras model**. Finally, we run **SVM classifier** to clasify these embeddings into  different persons class.

If we want to add new person in the database in future, we can easily done it by following same procedure as above for 1 person.

## Dependency
 click [here](requirements.txt) to show dependencies 
 
## License
Licensed under [MIT Licencse](LICENSE)

## Reference
* FaceNet is a face recognition system that was described by Florian Schroff, et al. at Google in their 2015 paper titled 
[“FaceNet: A Unified Embedding for Face Recognition and Clustering”](https://arxiv.org/abs/1503.03832).
* A notable example is ["Keras FaceNet by Hiroki Taniai"](https://github.com/nyoki-mtl/keras-facenet).His project provides a script for converting the Inception ResNet v1 model
from TensorFlow to Keras. He also provides a pre-trained Keras model ready for use.Download facenet-keras pre-trained model from ["here"](facenet_model/facenet_keras.h5).

