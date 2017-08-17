## Google Cloud

Enable Compute Engine and Container Engine APIs

# Compute Engine API
# Container Engine API

List available time zones:
```
gcloud compute zones list
```
Set a time zone example:
```
gcloud config set compute/zone europe-west1-d
```

### Cloud shell - launch a new VM instance
```
gcloud compute instances create ubuntu \
--image-project ubuntu-os-cloud \
--image ubuntu-1604-xenial-v20160420c 
```
### ssh login inside instance:
```
gcloud compute ssh ubuntu
```

## Download Go:
```
wget https://storage.googleapis.com/golang/go1.6.2.linux-amd64.tar.gz
sudo rm -rf /usr/local/go
sudo tar -C /usr/local -xzf go1.6.2.linux-amd64.tar.gz
echo "export GOPATH=~/go" >> ~/.bashrc
source ~/.bashrc
```

## Push Images
See all images
```
sudo docker images
```
Docker tag command help
```
docker tag -h
```
Add your own tag
```
sudo docker tag monolith:1.0.0 <your username>/monolith:1.0.0
```
For example (you can rename too!)
```
sudo docker tag monolith:1.0.0 udacity/example-monolith:1.0.0
```
Create account on Dockerhub
To be able to push images to Dockerhub you need to create an account there - https://hub.docker.com/register/

Login and use the docker push command
```
sudo docker login
```
```
sudo docker push udacity/example-monolith:1.0.0
```


