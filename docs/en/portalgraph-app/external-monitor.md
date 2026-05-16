# External Monitor Settings

This page explains how to configure Portalgraph when using a 3D projector or similar device connected to your PC. When using a large screen such as a projector, a VIVE Tracker is used for viewpoint tracking.

Press **F12** while the Portalgraph application is running to open the settings screen.

<figure><img src="../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

In the **View Count** field on the right, enter the number of screens on which to display the Portalgraph view, then enter the display number for each screen (1 = main display, 2 and above = sub-displays; this depends on your environment).

<figure><img src="../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

**Click "Apply" to apply the values — changes will not take effect unless you click Apply. If the screen you are using changes, you will need to restart the application.**

**Offset and Scale do not normally need to be edited. Skip the following unless you need to restrict the display area.**\
Use these settings if you want to display the image in only part of the screen. Offset uses (0, 0) as the bottom-left and (1, 1) as the top-right; Scale ranges from 0 to 1 (same as Unity's camera viewport).

<figure><img src="../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

From the **3D** dropdown, select the 3D mode that matches your 3D projector or other display device.

<figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

* **Side-By-Side** — Left-right split 3D
* **Top-And-Bottom** — Top-bottom split 3D
* **Anaglyph** — Red-blue 3D glasses. The color split method can be selected from the dropdown on the right.
* **No 3D** — No 3D output
* **2 outputs** — Splits the left-eye and right-eye images across two separate video outputs. The left-eye image is output to the screen currently being configured, and the right-eye image is output to the screen selected in the sub-display dropdown.

After configuring, use the VIVE Tracker to calibrate the screen. For initial VIVE Tracker setup and calibration, refer to the [VIVE Tracker Setup Guide](vive-tracker-guide.md).
