---
layout: post
title:  "Making Music with Ruby"
---

Concept: Making Music Signals with Ruby

Sample Rate
------
Number of data values for each second of audio
Measured in Hertz
>CDs use 44,000 Hertz sample rate

Amplitude
-----
"Loudness", how loud the sound is

Frequency
------
"Pitch", how often the sound is emitted

Types of Sound Waves
--------
1. Sin
1. Random
1. Triangle
1. Saw
1. Square

>Most sounds are multiple waves used together.

Fourier Transform
---------
"Frequency Mode" of a sound wave

Every waveform is just the sum of simple sinusoids of different frequencies

Analysis
--------

1. Pitch detection (tuner)
1. Wave shaping (equalizer, autotune)

Ruby!
=====

Audio Libraries
---------
1. Ruby Audio
1. Easy Audio (port audio wrapper)
1. easy_vst (use Ruby to generate sound waves that are ported to Ableton)

Sample using the VST synth:

{% highlight ruby %}
  # plays a bass drum
  $.music.fn = -> { e(SINE) * e(EXP_FALLOFF)}
{% endhighlight %}

