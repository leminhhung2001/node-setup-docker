<!--Create a image from docker file -->

docker build -t my-node-app:v0.0.1

<!-- Run image -->

sudo docker run -p 5001:8080 my-node-app:v0.0.1
