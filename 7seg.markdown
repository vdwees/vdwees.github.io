---
layout: page
title: 7seg
permalink: /7seg/
---

# A Digital Timer Scanner App

![View of app in light-theme help mode](/assets/help-light.png){: width="25%"}
![View of app in light-theme scanner mode](/assets/scan-light.png){: width="25%"}
![View of app in light-theme reminder mode](/assets/reminder-light.png){: width="25%"}

Have you ever found yourself waiting for a microwave, and wished you could walk away
and get a reminder when its done?
Or maybe you are vision-impaired and would like an app to read aloud how much time is left on the machine.
That's what this app is for.
 
Devices such as microwaves, washing machines, and ovens often have electronic seven-segment displays to indicate how long until the machine is done (the ones in my house do, at least). 7seg uses some advanced computer vision techniques to extract the digits out of timer displays, with first-class support for seven-segment displays.

# Usage
The app consists of a camera view and an overlay with the best guess set of digits in enlarged text at the top. If the numbers are tapped or the overlay is dragged upward, the camera is paused and the user is presented the option to schedule a notification for later based on the captured digits. Dragging the overlay back down or tapping on the digits will return the app to its initial state and digits will start getting captured again.

# Troubleshooting
For best performance, ensure timer display is clean, well-lit and free of glare.
If the timer screen is glossy, you might have better success when holding the camera
at a slight angle.

# Limitations
Computer vision is challenging, and some digital timer manufacturers seem to think that they
should make their timer displays as complex and glossy as possible.
Indeed, digital timers have been around for a while and there is a huge range of designs.

I wish I could say this app supports all timers, but its possible it does not support one of yours. If you'd like me to try and support a particular timer, feel free to send me relevant pictures and info via email, keeping in mind that some timers or lighting environments will always be out of scope.

In any case, this app is provided as-is.
Use it at your own risk.
It's really not suitable for situations where someone could get hurt.
