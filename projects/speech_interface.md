---
layout: project
type: project
image: images/voicekit.png
title: Google Voicekit Interface for Chatbot
permalink: projects/speech_interface

date: 2018-07-23
labels:
  - Google Voicekit
  - Google Speech to Text API
  - Raspberry Pi

summary: Voice interface for Raspberry Pi based chatbot.
---

I came accross AIY Google Voicekit recently and thought would give a try. You can build your own intelligent speaker like Alexa, Google Home in $50.<br/>

I rushed to Target to buy Voicekit, came home, followed the manual and connected the hardware as instructed. Boom, it worked like a charm in 1.5  hrs.

After that, I used Google Cloud Speech Recognition API to convert speech to text and send the text message to my Raspberry pi chatbot as input. I send this as a REST API call for the Flask Webserver that is running in Pi. I created a dedicated endpoint for this and it worked really well.

Google has done a great work in speech recognition and the accuracy is pretty good. FB Messenger is no longer neccessary for communicating to Pi. I can talk to it directly from Google VoiceKit by pressing a button.

[Google Speech to Text API](https://cloud.google.com/speech-to-text/)<br/>
