---
description: >-
  This guide explains how to implement a custom tracker app for use with
  Portalgraph.
---

# Tracker App Development Guide

## Overview

Portalgraph applications receive coordinates from the tracker app via OSC (Open Sound Control) communication and display visuals based on those coordinates. The receiving protocol is a subset of the [VirtualMotionTracker API](https://gpsnmeajp.github.io/VirtualMotionTrackerDocument/api/). The default receiving port is **49570**.

**API List** Portalgraph's OSC communication supports the following APIs:

* **/VMT/Room/Unity** `(int)index, (int)enable, (float)timeoffset, (float)x, (float)y, (float)z, (float)qx, (float)qy, (float)qz, (float)qw`\
  Left-handed coordinate system, Quaternion, Room space, similar to Unity (recommended).
* **/VMT/Room/UEuler** `(int)index, (int)enable, (float)timeoffset, (float)x, (float)y, (float)z, (float)rx, (float)ry, (float)rz`\
  Left-handed coordinate system, Euler angles, Room space, similar to Unity (recommended).
* **/VMT/Input/Button** `(int)index, (int)buttonIndex, (float)timeoffset, (int)value`\
  Button input. `value(int)`: 1 = Press, 0 = Release
* **/VMT/Input/Button/Touch** `(int)index, (int)buttonIndex, (float)timeoffset, (int)value`\
  Button touch input. `value(int)`: 1 = Press, 0 = Release
* **/VMT/Input/Trigger** `(int)index, (int)triggerIndex, (float)timeoffset, (float)value`\
  Trigger input. `value(float)`: 0.0 – 1.0
* **/VMT/Input/Trigger/Touch** `(int)index, (int)triggerIndex, (float)timeoffset, (int)value`\
  Trigger touch input. `value(int)`: 1 = Press, 0 = Release
* **/VMT/Input/Trigger/Click** `(int)index, (int)triggerIndex, (float)timeoffset, (int)value`\
  Trigger click input. `value(int)`: 1 = Press, 0 = Release
* **/VMT/Input/Joystick** `(int)index, (int)joystickIndex, (float)timeoffset, (float)x, (float)y`\
  Joystick input. `x, y(float)`: -1.0 – 1.0
* **/VMT/Input/Joystick/Touch** `(int)index, (int)joystickIndex, (float)timeoffset, (int)value`\
  Joystick touch input. `value(int)`: 1 = Press, 0 = Release
* **/VMT/Input/Joystick/Click** `(int)index, (int)joystickIndex, (float)timeoffset, (int)value`\
  Joystick click input. `value(int)`: 1 = Press, 0 = Release

## Registering the App

You can set Portalgraph to automatically launch your custom tracker app.

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

In the settings screen (opened by pressing F12), enter the app’s path in the **Tracker App** field in the bottom-left corner to have it launch automatically on startup.

Alternatively, you can add the app to the dropdown in the bottom-left corner by adding it to the file:\
`(Windows Documents folder)/Portalgraph/portalgraph_user_trackers.json`

Use the following format to register the app in the dropdown.

```
{
  "trackerApps":[
    {
      "name":"Great Tracker",
      "path":"C:/YourGreatTracker.exe"
    }
  ]
}

```
