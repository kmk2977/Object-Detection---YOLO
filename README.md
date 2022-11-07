# Object-Detection---YOLO

## Introduction

YOLOv5 is a computter vision AI by <a href="https://ultralytics.com">Ultralytics</a>. We will be using [OctoML CLI](https://try.octoml.ai/cli/), a free command line
utility that packages machine learning models into deployable Docker containers with NVIDIA Triton Inference Server. When you’re ready to deploy to production, OctoML CLI can also be used to accelerate and deploy YOLOv5 to over 100 instance types in AWS, Azure and GCP.

![Diagram of inference architecture](images/image1.png)

## Install Docker Desktop

If you don’t already have Docker Desktop installed locally, go ahead and
[install it now](https://www.docker.com/products/docker-desktop/).

![Docker Desktop download page](images/image31.png)

Then start Docker Desktop and you should be greeted with the Docker Desktop UI:

![Docker Desktop application](images/image33.png)

Try running docker info from your laptop’s command prompt to ensure that the
docker server is running correctly:

![Result of running docker info](images/image21.png)

Now grab this basline docker image, it already contains the pytorch installed.
``` shell
docker pull pytorch/pytorch:1.12.1-cuda11.3-cudnn8-runtime
```
After the image is done downloading then check whether the image is installed.
``` shell
docker images
```

After this is done, create a folder -> create a sub-folder docker-mount

Open a command prompt and then type in the following code..
``` shell
docker run -i -t --network host --mount type=bind,source=<SOURCE-Path>,target=/workspace/docker-mount pytorch/pytorch:1.12.1-cuda11.3-cudnn8-runtime
```
replace <SOURCE-Path> with the folder path tto docker-mount folder you just created. 
