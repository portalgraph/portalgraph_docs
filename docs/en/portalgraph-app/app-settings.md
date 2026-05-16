---
description: >-
  This section explains the settings options in the configuration screen of
  applications built with Portalgraph.
---

# Portalgraph Application Settings Options

## Main Screen Settings

Press the **F12 key** to open the settings screen.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

* **IPD:** The distance between the left and right eyes (in mm). Usually, no changes are needed.
* **Camera Lock:** Check this box to fix the viewpoint. When you press the **Position Set** button, a countdown will begin, and the viewpoint will be fixed at the coordinates at the end of the countdown.
* **Tracker Position:** Set the face tracking position here. For camera tracking, select **EyeCenter**. When you click **Apply**, the dropdown values are applied to eye coordinates and eye rotation.
* **Tracker App AutoStart :** If checked, the designated tracker app specified in the textbox below will start automatically when the application launches. You can select **Camera** (for webcam tracking) or **OpenVR** (for VIVE tracker) from the dropdown.
* **View Count, Screen, Offset, Scale:** These settings apply when using Portalgraph on multiple screens or secondary displays. Set the number of screens in **View Count** and specify the screen number in **Screen** (the main screen is 1). Use **Offset** and **Scale** if only part of the screen is used; the bottom-left corner is offset (0,0). Click **Apply** to confirm changes. Note: Changing the screen count or screen number requires restarting the application.

## Calibration Settings Screen

Click **Next (N)** in the main settings screen to open the calibration screen.

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160124.png" alt=""><figcaption></figcaption></figure>

#### 3D Dropdown

Allows selection of the 3D display mode. The available options are as follows:

* **Side-By-Side**: Splits the screen left and right.
* **Top-And-Bottom**: Splits the screen top and bottom.
* **Anaglyph**: Red-blue glasses mode. You can select the color separation method in the dropdown on the right (Dubois works in most cases).
* **No 3D**: Displays in 2D. The dropdown on the right lets you choose between the right-eye and left-eye views.
* **2 Outputs**: Outputs the right-eye view to a separate output terminal. Use the dropdown on the right to select which screen to output to.

## Camera Tracking Screen Settings&#x20;

Clicking **Camera** in the calibration screen opens the camera tracking calibration screen.

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160131.png" alt=""><figcaption></figcaption></figure>

If the camera is positioned directly above the center of the screen, facing straight forward, and your PC screen has a 16:9 aspect ratio, simply enter the screen size (in inches) in this screen and click **OK** to complete the setup.

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160142.png" alt=""><figcaption></figcaption></figure>

* **Screen Size**: Enter the size of your monitor in meters.
* **Camera Position**: Select the camera’s mounting position (top, bottom, left, right, or center) from the dropdown, and enter the distance from this position in meters in the text box. The XYZ axes are defined with positive directions as follows: right, up, and away from the screen.
* **Camera Angle**: Enter this if the camera is not perpendicular to the screen.

## Tracker Settings Screen

In the calibration screen, click **Camera** to open the tracker settings screen.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* **Screen Size**: Enter the size of your monitor in meters.
* **Screen Angle Correction**: If your screen is vertical or horizontal, select this option to automatically adjust the angle during calibration.
* **Tracker Position**: Specify the position to align the tracker with the screen during calibration. **Center** is usually appropriate, but you can choose a more stable position if using a projector screen where the center is soft, or if using a 3D TV where screen reflections may interfere with tracker stability.
