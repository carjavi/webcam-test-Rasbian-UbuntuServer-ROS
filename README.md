<p align="center"><img src="./img/webcam.jpg" width="800"  alt=" " /></p>
<h1 align="center"> WebCam testing Rasbian UbuntuServer and ROS </h1> 
<h4 align="right">March 24</h4>

<img src="https://img.shields.io/badge/OS-Linux%20GNU-yellowgreen">
<img src="https://img.shields.io/badge/OS%20-Raspbian%20GNU%2FLinux%2011%20(bulleye)-yellowgreen">


<br>

# Test camara USB Webcam
Check info webcam USB:
```
ls /dev/video*
lsusb
```

# Pictures
### fswebcam
```
sudo apt install fswebcam -y
```
testing:
```
fswebcam image.jpg
```
```
fswebcam --device /dev/video1 image.jpg
```

### ffmpeg
```
sudo apt install ffmpeg -y
ffmpeg -f v4l2 -video_size 1280x720 -i /dev/video0 -frames 1 out.jpg
```

> :memo: **Note:** You can set the device to use for recordings with the fswebcam software with the --device flag. For example, to take an image with the second connected USB webcam using fswebcam:


> :memo: **Note:** ```Para revisar image``` usar WinSCP en windows / SCP commands on linux

<br>

# Videos
```
sudo apt install ffmpeg -y
```
```
ffmpeg -f video4linux2 -framerate 60 -video_size 1920x1080 -input_format mjpeg -i /dev/video0 -f alsa -i hw:1 output.mp4
```

<br>

# Testing from GUI Ubuntu
Application ```cheese```

<br>

# Testing from Browser
https://es.webcamtests.com/

<br>

# Install usb_cam ROS Package
https://github.com/carjavi/ROS-web-video-server

<br>

# Video Streaming Using Python OpenCV/ UDP protocol/ Socket Programming
https://github.com/carjavi/video-streaming-python-openCV-UDP-socket

<br>

---
Copyright &copy; 2022 [carjavi](https://github.com/carjavi). <br>
```www.instintodigital.net``` <br>
carjavi@hotmail.com <br>
<p align="center">
    <a href="https://instintodigital.net/" target="_blank"><img src="./img/developer.png" height="100" alt="www.instintodigital.net"></a>
</p>




