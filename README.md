# CP2K Installation Steps
The easiest way to install CP2K is by Docker container.

Step 1:
Update your Linux system
```shell
sudo apt-get update
```
Step 2:
Setup Docker container
```shell
sudo apt install docker.io
```
```shell
sudo snap install docker
```

Step 3:
Pull CP2K directly from Docker container
```shell
sudo docker pull cp2k/cp2k:2023.2_mpich_generic_psmp
```

Hooray! You successfully install CP2K. Now do some test run:
```shell
sudo docker run -it --rm --shm-size=1g -v $PWD:/mnt -u $(id -u $USER):$(id -g $USER) cp2k/cp2k:2023.2_mpich_generic_psmp run_tests
```


