## Docker Installation


### For Ubuntu/Debian
```
sudo apt install docker.io
```
### For Arch 
```
sudo pacman -S docker
```

### After Installation
1. If service is not Running , Then Do this 
```
sudo systemctl start docker.service
sudo systemctl enable docker.service
```
##### For Checking Run :
```
sudo docker run hello-world 
```

# Basic Docker Commands :
1. For Searching An image.
```bash
$ docker search image-name  
```
2. For Runnig An Image , If Image is not Present It Will Download The image.
```bash
$ docker run
```
3. Show Docker Process , -a Flag for all process
```
$ docker ps -a 
```
 
  
