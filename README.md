# Timer LB

Timer LB is a simple but useful interval training timer for Android.

<a href="https://f-droid.org/packages/losangebleu.site.timerLB/" target="_blank">
<img src="https://f-droid.org/badge/get-it-on.png" alt="Get it on F-Droid" height="90"/></a>
</a>

## How to use Timer LB

### Workout structure

A workout with timer LB comprises a sequence of rest and work blocks. For example, a workout with two workout blocks will look like

1. block #1
2. rest
3. block #2
4. rest

The length of workout and rest are configurable. By default, it is respectivelly 50 and 10 seconds.
The number of blocks is configurable. By default, it is set to 12 blocks.
The default configuration brings a total workout time of 10 minutes

### Block structure

A block is a series of work/rest interval pairs. 

### Audio and visual cues

Timer LB always gives a warning when you're about to transition to a new interval. 
It consists of one beep from workout to rest, two beeps at start or from rest to workout and clapping at finish.

Once the timer is launched, you will see written how much time is left and if it is for resting or working out.
You will also see a green progress bar indicating how much time is left.

During workout session, a dumbbell will be on the screen, else three sleeping Z will be displayed.

Once the timer is done, a special beep will ring and "DONE" will be written.

### Pause workout

You can pause the timer using the PAUSE button. A CONTINUE button will then appears. Get back to the session tapping it.

### App screen shot
<img src="start.PNG" alt="start" height="90"/>
<img src="ongoing.PNG" alt="start" height="90"/>
<img src="paused.PNG" alt="start" height="90"/>
<img src="end.PNG" alt="start" height="90"/>

---

## Development environment

### Requirements

+ `adb`: used to synchronize the development environment with a device (mobile phone, tablet, etc...)
+ `sdk`: a useful tool to easily install `gradle` versions
+ `gradle`: used to build the application
+ A text editor/processor

### Install tools

+ Follow [this instructions](https://developer.android.com/studio/command-line/adb) to install `adb`.
+ Follow [this instructions](https://sdkman.io/install) to install `sdk`
+ To install `gradle` simply type `sdk install gradle 2.14.1` and type `Y` when the cli asks if you want to use it as the current `sdk` version. This project will only work with gradle version `2.14.1`.
+ Check the gradle version using `gradle --version`. It should be 

### Installing the application in a device

#### ADB connection

First let's synchronize the device usibg adb

+ Type `adb devices`
+ No device should appear unless you connected it by USB. In that case your device is now synchronized with your computer
+ If you want to synchronize it using Wi-Fi you must first enable tcp connections.
+ Type `adb tcpip 5555` to start listening to connections
+ Check that your phone and computer are connected to the same network
+ Now check which is your device's IP address. This can be typically found in `Settings -> System -> About the phone -> State -> IP address`
+ Let's assume your IP is `192.168.0.156`, then type `adb connect 192.168.0.156`.
+ The device should be connected. Check that out typing `adb devices`.

#### Using gradle

Gradle is a tool that we use to build the source code, run tests, release applications, and perform many other tasks.

To build the application we can just type:

+ `gradle installDebug`

It will automatically install the application in your phone using `adb`, that'ß why we need to establish (synchronize) an adb connection first.

Check what other tasks can be performed:

+ `gradle tasks`

---

## License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.
 
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

Copyright (c) 2022 Jeremy Lefort-Besnard <losangebleu.site> <jlefortbesnard@tuta.io>
