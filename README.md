> March 2021:  If you'd like to share your screen & camera with a livestream, check out [record.a.video](https://record.a.video).  Code is related to this repo, but [updated](https://github.com/dougsillars/recordavideo).

Ref 10:03 15/10/2021 : 

1. https://github.com/ryanbekabe/NodeJS-getusermedia-browser-to-rtmp

2. https://github.com/chenxiaoqino/getusermedia-to-rtmp

3. https://github.com/apivideo/browserLiveStream

```git

git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:ryanbekabe/NodeJS-browserLiveStream.git
git push -u origin main

```

# browserLiveStream
Use your webcam, browser and NodeJS to stream live video from a webpage to your users.

Based on the [https://github.com/chenxiaoqino/getusermedia-to-rtmp](https://github.com/chenxiaoqino/getusermedia-to-rtmp) codebase, 
this project allows you to stream directly from the browser to your RTMP endpoint (in this case I am using [api.video](https://api.video) to distribute my stream.)

Since my Livestream is already established at api.video - there are no API keys or authentication needed, the video will just playback, and anyone with the URL for the playabck will be able to watch.  (I am not providing the playback url - this is not a "free streaming tool" :) ).

Requiremennts:  The website will only work in Chrome, Edge and Firefox (Safari/Webkit does not yet support the MediaRecorder API, so unfortunately, no browsers on iPhones will work).

## RTMP video
 The Node backend takes the webcam video, and transcodes it into FLV format - so it can be ingested by any "live straeming" site with an RTMP endpoint, which is configurable in the form on the page.

### api.video

The default RTMP endpojnt is a livestream hosted at [api.video](https://api.video).  

Note: The RTMP endpoint in the code is streaming into my account - and I can see all your videos. Please wear pants. :D

## Camera usage on a webpage

In order to use the webcam in the browser, your site must be served via HTTPS, or you users will have to bypass a security message every time they go to yur site (will work in Chrome, but not in Firefox).  

Alternatively: If you host this site locally on your computer, localhost will allow you to use the camera

To launch your own local version on localhost, simply clone the repo and run "node server.js" on the command line. Youo'll need FFMPEG on the server to do the transcoding. 

In your browser, go to  localhost:1437 - and you are up and running!


##installation

clone the repo
npm install (for all dependencies)
install ffmpeg
node server.js

## Try it out!
This is running at https://livestream.a.video
