---
description: >-
  This section explains the settings options in the configuration screen of
  applications built with Portalgraph.
---

# Portalgraph Application Settings Options

## Main Screen Settings

Press the **F12 key** to open the settings screen. The settings screen is split into two tabs, **Camera** and **Tracker**: pick **Camera** for a quick single-webcam setup, or **Tracker** for a VIVE tracker or multi-screen setup.\
(The screenshot below is from the version before the tab split; the items it lists now live on the **Tracker** tab.)

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Tracker tab

* **IPD:** The distance between the left and right eyes (in mm). Usually, no changes are needed.
* **Camera Lock:** Check this box to fix the viewpoint. When you press the **Position Set** button, a countdown will begin, and the viewpoint will be fixed at the coordinates at the end of the countdown.
* **Tracker Position:** Set the face tracking position here. For camera tracking, select **EyeCenter**. When you click **Apply**, the dropdown values are applied to eye coordinates and eye rotation.
* **Tracker App AutoStart :** If checked, the designated tracker app specified in the textbox below will start automatically when the application launches. You can select **Camera** (for webcam tracking) or **OpenVR** (for VIVE tracker) from the dropdown.
* **Full Screen:** Switches between exclusive full screen and full-screen windowed (borderless) mode. Flickering or input lag can vary by environment, so try switching this if you notice either.
* **View Count, Screen, Offset, Scale:** These settings apply when using Portalgraph on multiple screens or secondary displays. Set the number of screens in **View Count** and specify the screen number in **Screen** (the main screen is 1). Use **Offset** and **Scale** if only part of the screen is used; the bottom-left corner is offset (0,0). Click **Apply** to confirm changes. Note: Changing the screen count or screen number requires restarting the application.

### Camera tab

A simplified tab for getting up and running quickly with a single webcam. Enter the screen size (in inches) and click **OK** to apply — this covers the same ground as the **Camera Tracking Screen Settings** section below, but in one place. Applying settings here also sets up **Tracker App AutoStart** and the tracker position (equivalent to **EyeCenter**) automatically, so you don't need to configure those separately on the Tracker tab. For Advanced Mode and the 3D display mode options, see **Camera Tracking Screen Settings** below — the fields are the same, just consolidated into this tab.

## Calibration Settings Screen

Click **Next (N)** on the **Tracker** tab to open the calibration screen (use this for multi-screen setups, or to choose Tracker vs. Camera per screen).

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160124.png" alt=""><figcaption></figcaption></figure>

#### 3D Dropdown

Allows selection of the 3D display mode. The available options are as follows:

* **Side-By-Side**: Splits the screen left and right.
* **Top-And-Bottom**: Splits the screen top and bottom.
* **Anaglyph**: Red-blue glasses mode. You can select the color separation method in the dropdown on the right (Dubois works in most cases).
* **No 3D**: Displays in 2D. The dropdown on the right lets you choose between the right-eye and left-eye views.
* **2 Outputs**: Outputs the right-eye view to a separate output terminal. Use the dropdown on the right to select which screen to output to.

## Screen Trimming

Click **Screen Trimming** in the calibration screen to open a screen where you can adjust the visible area directly with the arrow keys. This is useful for fine-tuning alignment, for example when a projector's image extends beyond the physical screen.

* **Arrow keys**: Move the visible area (offset) up, down, left, or right.
* **Shift + Arrow keys**: Resize the visible area (scale).

The current Offset and Scale values are shown on screen. These are the same values as **Offset** and **Scale** in the main settings screen, so you can also fine-tune them there afterwards. Click **OK** to confirm, or **Cancel** to revert.

## Camera Tracking Screen Settings&#x20;

Clicking **Camera** in the calibration screen opens the camera tracking calibration screen (the **Camera** tab on the main settings screen contains the same items).

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
