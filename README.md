## Google Cloud

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
