---
date: '2025-07-16T22:48:30+02:00'
draft: false
title: 'Optimizing max aerobic power training'
tags: [intervals.icu,cycling,training,javascript]
---
# Who is this for?
This article is intended for cyclists who use data from power meters and heart rate sensors for training. I also explain how I use [intervals.icu](https://intervals.icu "intervals.icu"), which is an incredible platform. I upload all my workouts to monitor performance. It's very powerful because I can create custom graphs to show a lot of metrics. I can even extend it with some custom JavaScript.

# Some definitions
## Power
We can measure power in watts with power meters. This can be done indoors with a smart trainer or outdoors with a power meter that can be located in the pedals or cranks, for example.
## FTP
One performance criterion (among others) is FTP: Functional Threshold Power. Theoretically, FTP is the maximum average power we can produce during one hour. A lot of workouts are based on FTP: we have to pedal X minutes at Y% of our FTP. It's far from perfect, but it helps to calibrate training sessions. 
## MAP
Maximum Aerobic Power is an important characteristic. People often compare MAP for cyclists to maximum engine power for vehicles. It represents the maximum power we can produce with a metabolism that uses oxygen. It's possible to produce even more power without oxygen, but these kinds of efforts can't last more than tens of seconds... So, increasing MAP benefits every cyclist, whether they do short races or very long distance ones!

This is a typical training session I used to do:
- warm up 5 minutes
- repeat 4 times:
  - stay ≥ 90% of FTP (Functional Threshold Power) *AND* ≥ 90% of max heart rate for 3 minutes
  - rest 3 minutes
- cool down 10 minutes

Yes, it is not a very long training session, but it's enough for me since I'm a recreational cyclist :wink:

It looks like this on Intervals.icu: ![Intervals.icu workout](/posts/optimizing-map-training-overview.png)

**The most common error would be to focus on power data and not pay attention to heart rate. Both constraints are needed for the workout to be efficient.**

# Measuring efficiency
I added this little piece of code to compute how much time I spend in my target power zone **AND** in my target heart rate zone.
{{< gist polouis af525550f191e176687caae816a0867a >}}
To install it:
- open a workout and click on "Custom" at the bottom of the screen
- add field
- set the correct parameters in the main tab: ![Intervals.icu workout](/posts/optimizing-map-training-field.png)
- add the JavaScript in the script tab

It shows my new stat like this on the top left of the screen: ![Intervals.icu workout](/posts/optimizing-map-training-stat.png)
In the previous workout, I have 4 intervals of 3 minutes at high intensity, which represents a total of 12 minutes. In this workout, I spent 406 seconds (which is 6 minutes and 46 seconds) hitting my target out of a total of 12 minutes, which is quite good.

# Conclusion
I hope you enjoyed this article and I'm happy to share this code. Don't hesitate to try Intervals.icu if you haven't already done so!