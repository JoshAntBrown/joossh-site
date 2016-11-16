---
layout: post
title:  "How to setup, record, and live stream user feedback"
date:   2015-05-14 10:42:40 +0100
---
User testing is an important part of researching and validating products and services. Most people aren’t doing it though. You might say it is too difficult to setup, or too expensive to run. You might have searched for it before, and found countless agencies and products to carry out user testing for thousands of pounds, maybe even more.

<img src="/assets/live-stream-user-testing.jpg" alt="Photo of a user testing session" class="bordered">

You could always just run a user testing session without anything to record the session, but then how would you refer to what happened, how will you back up your points with hard research, how will you share your results with the rest of the team? If you are not recording the lessons from your user testing sessions, you may as well not be doing any user testing.

So what if there was a way that you could broadcast the session to your team live, have it automatically saved into a video archive, in a way that would let the team see both the user and the screen of the device. What if you could do that with 5 things that you probably already have access to.

All you need to get started is a user to test on, a mobile device, a computer with internet access and a webcam. We did this on a Macbook and iPhone but there is no reason all this would not be possible to do on a Windows machine.

## Recording the Device
We currently have two options for recording the screen of the device, one wired and one wireless. Both of these methods require an iOS device and only the wireless method supports Windows. Although with a little bit of work I am sure there is a solution that exists to do this with Android.

We’ll start with the wired method which is by far the easiest, it doesn’t require you to install any additional software or buy any hardware providing you have the latest version of Mac OS X. Firstly, you’ll need to plug your iOS device in via USB. Then you can launch Quicktime and select File > New Movie Recording from the menu bar. The recording screen will default to your iSight camera, but ignore that and click on the small downward-facing triangle next to the record button and you’ll be able to pick your iOS device as the source. Then we’re done, you don’t need to get it to start recording or anything, you just want to have a window showing the screen running on your computer.

The wireless method does cost some money as it uses a piece of software called Reflector, which you only need to install to your computer. It currently works on both Mac and Windows and serves your computer as an airplay location that you can mirror your device to. Again, once you’ve got your screen displayed on your computer this step is done.

## Setting the stage
For our next part, we will set the stage and set up our streaming software. In order to do this, we need to install a free open source piece of software which works on Windows and recently Mac as well. This software is called OBS or Open Broadcasting Software, it allows you to take multiple sources and process them into a video which can then be sent to streaming services such as YouTube.

Above you can see the software we are using, we’ve created a scene and named it iPhone Capture. A scene basically holds the information about the sources and their settings and location on the screen. Next to the scene you can see those sources that we are bringing into our scene.

We can choose from a list of various different sources that allow us to create something tailored to our requirements.

For us, we need to capture the window that we’re recording our device to, so this could be Quicktime or Reflector. Then we want to capture audio from a microphone this is under audio input capture. Next we want to include the webcam so we add that as a Video Capture Device input. Once we’ve got our sources onto the scene we can move them around and change their sizes to get them where we want them.

## Streaming
Now we have our streaming software setup we need to create a live event on YouTube to give us a place to set OBS to stream to. In order to do this, you’ll need to head to the Video Manager in the YouTube Creator Studio section. Then you’ll be able to go to the Live Events and Create Live Event.

Creating a live event will allow you to set information such as the title, time, description and access whether it is public or private. The one option you must choose is to set the type to Custom otherwise, you’ll be setting up a Google+ Hangouts live stream. There are some advanced settings, but they shouldn’t need changing for this.

Once saved, you’ll progress to the Ingestion Settings screen, this lets you choose the quality you want to broadcast at and gives you the information you’ll need to stream from OBS. The maximum quality you can stream at will vary depending on your machine and internet connection so you’ll need to have a play with that. We settled with 480p to ensure stability on poor wifi connections, but could easily have gone up to 1080p.

After you’ve picked your basic ingestion rate you’ll be given your stream name, and URLs. You’ll only need the stream name as OBS already has the URLs saved.

All you need to do is load the stream settings panel on OBS, pick YouTube as the service and then enter your stream name from YouTube as your stream key.

All that’s left is to head back to the main OBS screen and press the ‘Start Streaming’ button, you’ll need to head back to the YouTube page for the event and go to the Live Control Room. This page will give you a stream status that tells you that they are receiving your broadcast and highlight any issues. Once you have been streaming for a short amount of time, you’ll need to click ‘Preview’, and then once it has been reviewed and tested you’ll need to click ‘Start Streaming’.

At the end of the stream, you’ll need to press ‘Stop Streaming’ in OBS and then the same again in the Live Control Room of YouTube. This will start the process of rendering your stream into a video on YouTube. We then add these videos to a playlist to collect them all together in one place.
