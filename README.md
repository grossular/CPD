# DC CPD

This repository contains the code and presentation for the Digital Catapult machine learning CPD module.

## Get the Code

Download the zip from [HERE](https://github.com/grossular/CPD/archive/master.zip)

### Running in Google Colaboratory

 - Navigate to - [https://colab.research.google.com](https://colab.research.google.com)
 - Sign in with Google account.

#### Pull Directly into google colab
- Select File -> Upload Notebook... -> Github
- Paste this URL: [https://github.com/grossular/CPD](https://github.com/grossular/CPD)
- Select the notebook you wish to use.

#### Upload sheets from local copy

 - Select File -> Upload Notebook...
 - Drag and drop or browse to select the notebook you wish to use.

### Running locally

#### Build and run docker container

```
cd CPD/Docker

docker build -t lspvic/tensorboard-notebook:v2 .

cd ../   # Make sure you cd to the root of the project

docker run --rm -it -p 8888:8888 -p 6006:6006 -p 4040:4040 \
-v $(pwd):/home/jovyan/work lspvic/tensorboard-notebook:v2 \
start-notebook.sh --NotebookApp.token=''
```

Once that is running you can connect to the notebook server on http://0.0.0.0:8888
