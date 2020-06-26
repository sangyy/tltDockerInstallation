# tltDockerInstallation

# 1.安装NVIDIA Container Runtime
https://blog.csdn.net/byaa34616/article/details/100951724

# 2.安装docker
https://docs.docker.com/engine/install/ubuntu/

# 3.(选作)在 docker run 省掉--rm --gpus all参数，改成默认不带参数就开启GPU环境

Docker Default Runtime
To enable access to the CUDA compiler (nvcc) during docker build operations, add "default-runtime": "nvidia" to your /etc/docker/daemon.json configuration file before attempting to build the containers:

{
    "runtimes": {
        "nvidia": {
            "path": "nvidia-container-runtime",
            "runtimeArgs": []
        }
    },

    "default-runtime": "nvidia"
}
You will then want to restart the Docker service or reboot your system before proceeding.

https://github.com/dusty-nv/jetson-containers
