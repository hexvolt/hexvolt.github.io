---
layout: post
title:  "Raspberry Pi - Streaming to Youtube"
date:   2016-08-28 10:47:42 +0300
categories: jekyll update
---

Goal: create a stream on Youtube and start streaming automatically

## What do we need:

1. Setup and use Google API for Youtube

    * [Workflow for setting up an API] Generally, all you need is to create a Server API Key in the [google developers console] and activate the Youtube API in the Library section there.
    * Use [Python API client] to access Youtube. Here is a [Youtube API explorer] with references.
    

2. Use a supervisor?
    
3. How to integrate to the web page? Invoke `sudo supervisorctl start ...` ?
Apparently it is better to build a python script for supervisor which will look into database and run a `raspivid | ffmpeg > youtube` command. Web app will put something to database to start the process. How to stop the process though?

[Workflow for setting up an API]: https://developers.google.com/youtube/v3/getting-started
[Python API client]: https://github.com/google/google-api-python-client
[google developers console]: https://console.developers.google.com/apis 
[Youtube API explorer]: https://developers.google.com/apis-explorer/#p/youtube/v3/
