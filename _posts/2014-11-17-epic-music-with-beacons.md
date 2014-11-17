---
layout: post
title:  "Epic Music with Beacons"
---

Concept: Play music as someone enters the office

Stack:

* iBeacon iPhone app (Rubymotion) emits broadcast
* Sinatra server listening for a POST request with a name parameter
* Raspberry Pi to play mp3 associated with that name

Misconceptions of beacons:

1. Beacons deliver content.
1. Beacons know when they are detected. Beacons just announce identifiers over and over again
1. Beacon distance is accurate. Bluetooth not meant to determine distance (other RF tech can)
1. iOS can scan for all beacons. Need UUID
1. Beacons track you (your phone can)
