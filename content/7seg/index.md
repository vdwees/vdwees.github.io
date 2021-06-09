---
title: 'SevenSeg: a number scanner app'
date: "2021-02-19T00:00:00Z"
tags:
  - computer vision
  - accessibility
  - iOS
summary: a number scanner app for seven-segment displays
---


Have you ever found yourself waiting for a microwave, and wished you could walk
away and get a reminder when its done? Or maybe you are vision-impaired and
would like an app to read aloud how much time is left on the machine. That's
what this app is for.
 
Devices such as microwaves, washing machines, and ovens often have electronic
seven-segment displays to indicate how long until the machine is done (the ones
in my house do, at least). SevenSeg uses state of the art computer vision
techniques to extract the digits out of timer displays, with first-class
support for seven-segment displays.

The app is not limited to timers- it should work for displays that
are not timers as well. For example, it could also be used to read time
displayed on a digital clock or the temperature display of a digital thermostat
or oven.

If you'd like to give the app a try, you can find it on
[TestFlight](https://testflight.apple.com/join/DdPnqnlA). Any feedback is
welcome!

## Usage

<figure>
  <img
    src="/images/help-light.png"
    alt="View of app in help mode. Some text is visible to instruct how to use the app."
    width="31%">
  <img 
    src="/images/scan-light.png" 
    alt="View of app in scanner mode. A timer with the digits 0 9 5 9 is visible in the camera window, and the digits 0 9 5 9 appear as the recognized text at the bottom of the app."
  width="31%">
  <img
    src="/images/reminder-light.png"
    alt="View of app in reminder mode. There is a button to set a reminder for 9 minutes 59 seconds and another to set a reminder for 9 hours 59 minutes."
    width="31%">
</figure>

The app consists of a camera view and an overlay with the best guess set of
digits in enlarged text. When a digital display into view, the app will
generate some haptic feedback and update the digits in real-time. If VoiceOver
is active, the app will read aloud the digits as they are updated.

If the digits are tapped or the overlay is dragged upward, the camera is paused
and the user is presented with some options based on what number was scanned.
Dragging the overlay back down or tapping on the digits will return the app to
its initial state and the camera will start capturing digits again.

Initially, the only option when the overlay is expanded is to schedule a
notification for later, interpreting the captured digits as a timer. Feedback
about other integrations should be added is welcome.

## Troubleshooting

For best performance, ensure the seven-segment display is clean, well-lit and
free of glare. If the target screen is glossy, you might have better success
when holding the camera at a slight angle.

## Discussion

Some discussion of the app can be found on
[reddit](https://old.reddit.com/r/Blind/comments/lnm796/app_to_scan_digital_timers/).

## Privacy

This app needs access to your device's camera, but does not collect any data.
All image processing is on the device itself. If you would like to use the
"Create Reminder" feature, you will also need to allow the app to set
notifications. These are also only on the device itself, so no data is
collected.

## Limitations

Computer vision is challenging, and some digital timer manufacturers seem to
think that they should make their timer displays as complex and glossy as
possible. Indeed, digital timers have been around for a while and there is a
huge range of designs.

I wish I could say this app supports all timers, but its possible it does not
support one of yours. If you'd like me to try and support a particular timer,
feel free to send me relevant pictures and info via email, keeping in mind that
some timers or lighting environments will always be out of scope.

In any case, this app is provided as-is. Use it at your own risk. It's really
not suitable for situations where someone could get hurt.
