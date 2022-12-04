# Project Sauron

- This project was built with the purpose of an automated attendance system using the Nvidia Jetson Nano 4GB

- This repository is an translation from PT-BR and adaptation for entry in the Nvidia Jetson Specialist Certification Program of the Sauron system hosted here: https://github.com/brunocatani/Sauron



Required Hardware:

- Nvidia Jetson Nano 4GB
- CSI/USB Camera 
- WI-FI Dongle/Module (Intel 8265AC M.2 Key E)


## Requerimentos 

- OpenCV 4.6.0 compiled with CUDA & CUDNN: 
https://github.com/opencv/opencv/releases

- Jetpack SDK 4.6.2: 
https://developer.nvidia.com/embedded/jetpack-sdk-462

- Dlib 19.17: 
https://github.com/davisking/dlib

- Face Recognition 1.3.0: 
https://github.com/ageitgey/face_recognition

- Python-Telegram-Bot 13.14:
https://github.com/python-telegram-bot/python-telegram-bot



## Compiling OpenCV with CUDA on the Jetson Nano

Complete tutorial by QENGINEERING
https://qengineering.eu/install-opencv-4.5-on-jetson-nano.html

## Compiling DLIB with CUDA + Face-Recognition install

- Installing base dependencies
- Instalando dependências base

Open terminal with CTRL+T 

```
sudo apt-get update
sudo apt-get install python3-pip cmake libopenblas-dev liblapack-dev libjpeg-dev
```
- Numpy installation
```
pip3 install numpy
```
- Baixar e descompactar Dlib
```
wget http://dlib.net/files/dlib-19.17.tar.bz2 
tar jxvf dlib-19.17.tar.bz2
cd dlib-19.17
```
- Editar cudnn_dlibapi.cpp 
```
gedit dlib/cuda/cudnn_dlibapi.cpp
```

- CTRL+F para encontrar 
```
forward_algo = forward_best_algo;
```

- Editar linha
```
//forward_algo = forward_best_algo;

```
- Compilar e instalar Dlib (30-60 minutos na Jetson Nano)
```
sudo python3 setup.py install
```

- Instalar biblioteca Face_Recognition
```
sudo pip3 install face_recognition
```


--US-EN--

This project is part of "Projeto Integrador 2022/2" supervised by the profesor Rafael Barbosa
