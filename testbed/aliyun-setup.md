
![Image](https://github.com/router-gao/cuda-demo/assets/144886373/dfaffd09-face-4bf2-a9f4-e54a80963c4d)


![Image](https://github.com/router-gao/cuda-demo/assets/144886373/bea04070-dc3b-43ee-9fa0-a18b9af7c0b6)


![image](https://github.com/router-gao/cuda-demo/assets/144886373/a39e4232-fbf3-4b0a-b3fb-c904a55e993d)


Download/Clone CUDA-Samples to local Ubuntu machine, zip the package, upload it to Aliyun and unzip it.

git clone

```shell
sudo apt-get update -y | apt-get install -y git
sudo git --version
sudo git clone https://github.com/NVIDIA/cuda-samples.git
```

zip

```shell
apt-get install zip -y
zip -r cuda-samples.zip cuda-samples/
```

scp the zip file to cloud instance

```shell
scp cuda-samples.zip ecs-user@[public-ip]:/tmp
```

unzip

```shell
cd /tmp/
unzip cuda-samples.zip
```

