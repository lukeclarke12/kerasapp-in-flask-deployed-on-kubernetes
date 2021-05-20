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

![Screen Shot 2021-05-20 at 20 31 10](https://user-images.githubusercontent.com/71552393/119035520-f376da00-b9af-11eb-8313-3f6fd37425ab.png)




![Screen Shot 2021-05-20 at 20 39 47](https://user-images.githubusercontent.com/71552393/119035537-f70a6100-b9af-11eb-8078-e2f46703a599.png)



Results: 
1. beagle: 0.9726
2. Walker_hound: 0.0060
3. pot: 0.0043
4. bluetick: 0.0024
5. Basset: 0.0019

