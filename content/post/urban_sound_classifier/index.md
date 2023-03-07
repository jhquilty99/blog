---
date: 2020-12-10T11:00:59-04:00
description: "Utilizes data science techniques to classify urban noises into 10 distinct sounds including a jackhammer, music, and sirens."
featured_image: "soundwaves.jpg"
tags: []
title: "Urban Sound Classifier"
---

Urban soundscapes are hectic places where the sounds of people and machinery are always a commotion. In order to make sense of the busy noises of a city, we developed a data science algorithm to classify these sounds. The classifier is able to distinguish between 10 different urban sounds. I did this project as part of a collaborative masters project at Virginia Tech with Brannon King.

We digested the 10,000+ sound files with the _librosa_ python package and extracted features such as RMS Frequency, Amplitude, and Length. The biggest challenges were overcoming some of the expensive computations of loading and working with the large sound files. We were successful in employing parallel processing and GPU processing to overcome these computational challenges. We also overcame a large hurdle in extracting useful information from the 1000s of bits encoded in a wav file. This required many iterations of spectrograms and attempts at extracting other useful audio information like RMS, fundamental frequency, and rhythm.

The most interesting feature we were able to approximate was beats per second. We were able to do this by identifying high and low amplitude sections of a sound file and count how many distinct high amplitude sections were in each section of sound. By normalizing to one second intervals of sound and generating features for multiple thresholds of silence (periods of low amplitude), we were able to map out multiple dimensions of beats per second for each sound. This feature was important in the final model. 

After testing a Convolutional Neural Network (CNN), XGBoost, and a Random Forest model, we found that that the Random Forest performed the best. With 90%+ accuracy on classifying 10 sounds in an urban setting, we felt accomplished that we could derive features from a nuanced data source. 

You can check out the Google collaboratory here:
https://colab.research.google.com/drive/1-4FxVwCUWGg-J6Cvd_L9ymcLZof1dILO?usp=sharing

The research paper can be found here:
https://drive.google.com/file/d/1Al7MePm7sUYMoe0tUkQT-xoUxHIXTvfn/view?usp=sharing 