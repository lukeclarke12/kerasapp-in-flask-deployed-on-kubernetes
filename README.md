# A Keras deep learning REST API built using Flask and deployed on Kubernetes

In this project I created a deep learning REST API using the ResNet50 model (which has been trained on ImageNet) and Flask. I then dockerized this application and deployed on Kubernetes so it could be publically accessed on live on a scalable and reliable cluster.


## Starting the Keras server

Below you can see the image we wish to classify, a _dog_, but more specifically a _beagle_:

![dog](dog.jpg)

The Flask + Keras server can be started locally by running:

```sh
$ python app.py 
Using TensorFlow backend.
 * Loading Keras model and Flask starting server...please wait until server has fully started
...
 * Running on http://127.0.0.1:5000
```


## Submitting requests to the Kubernetes server

Of course, the API is no longer live as these would be costly for me to up keep! However, 
requests were submitted via cURL:


$ python simple_request.py 
1. beagle: 0.9901
2. Walker_hound: 0.0024
3. pot: 0.0014
4. Brittany_spaniel: 0.0013
5. bluetick: 0.0011
```
