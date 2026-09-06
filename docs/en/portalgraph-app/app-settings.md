---
description: >-
  This section explains the settings options in the configuration screen of
  applications built with Portalgraph.
---

# Portalgraph Application Settings Options

## Main Screen Settings

Press the **F12 key** to open the settings screen. The settings screen is split into two tabs, **Camera** and **Tracker/Custom**: pick **Camera** for a quick single-webcam setup, or **Tracker/Custom** for a VIVE tracker or multi-screen setup that needs finer control.\
(The screenshot below is from before the tab split; its items now live in the tabs/common area below.)

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Common items (shown at the bottom of the screen regardless of tab)

* **IPD:** The distance between the left and right eyes (in mm). Usually, no changes are needed.
* **Camera Lock:** Check this box to fix the viewpoint. When you press the **Position Set** button, a countdown will begin, and the viewpoint will be fixed at the coordinates at the end of the countdown.
* **Full Screen:** Switches between exclusive full screen and full-screen windowed (borderless) mode. Flickering or input lag can vary by environment, so try switching this if you notice either.
* **Close (Esc):** Closes the settings screen.

### Camera tab

A simplified tab for getting up and running quickly with a single webcam. Enter the 3D display mode (defaults to Anaglyph) and the screen size (in inches), and it takes effect as soon as you move focus out of the field — there's no button to click.\
The **Manual Adjustment** button opens a screen where you can adjust the screen center's position and orientation directly with the arrow keys.\
Checking **Advanced Mode** switches to detailed fields: screen size in meters (width × height), camera position (top/bottom/left/right/center plus an XYZ offset), and camera angle — the same fields as **Camera Tracking Screen Settings** below.\
This tab is built so beginners can get going without thinking about the details: whenever a value takes effect here, **View Count** is automatically set to 1 screen, and **Tracker App AutoStart** plus the tracker position (equivalent to **EyeCenter**) are configured automatically too.

### Tracker/Custom tab

For VIVE tracker setups or anything needing finer control. It builds on whatever the Camera tab last configured, letting you customize further.

* **Tracker Position:** Select the tracker's position relative to the face from the dropdown (presets like **Camera/Eye Center**, **Forehead**, etc.). If no preset fits, enter the eye coordinates and eye rotation directly to customize it.
* **View Count, Screen, Offset, Scale:** These settings apply when using Portalgraph on multiple screens or secondary displays. Set the number of screens in **View Count** and specify the screen number in **Screen** (the main screen is 1). Use **Offset** and **Scale** if only part of the screen is used; the bottom-left corner is offset (0,0). Click **Apply** to confirm changes. Note: Changing the screen count or screen number requires restarting the application.
* **Tracker App AutoStart:** If checked, the tracker app selected in the dropdown/textbox below starts automatically when the application launches. Click **Launch** to try starting it right away.
* **Next (N):** Opens the calibration screen for detailed multi-screen calibration, or to choose Tracker vs. Camera on a per-screen basis.

## Calibration Settings Screen

Click **Next (N)** on the **Tracker/Custom** tab to open the calibration screen.

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160124.png" alt=""><figcaption></figcaption></figure>

(The screenshot above is from an older version. Each screen shows its screen number and a frame giving its size in meters — the trimmed area's size if it's been trimmed — plus **3D** and **Input** dropdowns, four buttons — **Tracker**, **Camera**, **Manual Adjustment**, **Screen Trimming** — and **Close All (Esc)** / **Close (Esc)**.)

#### 3D Dropdown

Allows selection of the 3D display mode. The available options are as follows:

* **Side-By-Side**: Splits the screen left and right.
* **Top-And-Bottom**: Splits the screen top and bottom.
* **Anaglyph**: Red-blue glasses mode. You can select the color separation method in the dropdown on the right (Dubois works in most cases).
* **No 3D**: Displays in 2D. The dropdown on the right lets you choose between the right-eye and left-eye views.
* **2 Outputs**: Outputs the right-eye view to a separate output terminal. Use the dropdown on the right to select which screen to output to.

#### Input Dropdown

Selects the input device (defaults to **Mouse**).

The four buttons — **Tracker**, **Camera**, **Manual Adjustment**, **Screen Trimming** — let you pick which kind of calibration to run.

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

In the calibration screen, click **Tracker** to open the tracker settings screen.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* **Screen Size**: Enter the size of your monitor in meters.
* **Screen Angle Correction**: If your screen is vertical or horizontal, select this option to automatically adjust the angle during calibration.
* **Tracker Position**: Specify the position to align the tracker with the screen during calibration. **Center** is usually appropriate, but you can choose a more stable position if using a projector screen where the center is soft, or if using a 3D TV where screen reflections may interfere with tracker stability.
