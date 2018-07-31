---
layout: project
type: project
image: images/video.jpg
title: Video Streaming
permalink: projects/video_streaming

date: 2017-07-14
labels:
  - picamera
  - Flask
  - Raspberry Pi

summary: Raspberry Pi based chatbot for realtime video streaming.
---

This project is to provide real time video streaming for the Raspberry Pi. The code heavily borrows from MigeulGrinberg and Adrian's blogs below.

I created an endpoint video_feed for the Flask Webserver and video streaming works great. I have also created another end point to take snap of current scene. This is useful when the internet connection is very slow.

I have placed Pi in my living room and the following image shows how it is displayed in the browser. This feature was super useful when I was out of town and wanted to see how my home looks at any moment.

### References:<br/>
1. [https://blog.miguelgrinberg.com/post/video-streaming-with-flask](https://blog.miguelgrinberg.com/post/video-streaming-with-flask)<br/>
2. [https://blog.miguelgrinberg.com/post/flask-video-streaming-revisited](https://blog.miguelgrinberg.com/post/flask-video-streaming-revisited)<br/>
3. [https://www.pyimagesearch.com/2015/06/01/home-surveillance-and-motion-detection-with-the-raspberry-pi-python-and-opencv/](https://www.pyimagesearch.com/2015/06/01/home-surveillance-and-motion-detection-with-the-raspberry-pi-python-and-opencv/)<br/>
