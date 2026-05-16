# Turn a 3D Projector into a VR Space

This page explains how to configure Portalgraph when using a 3D projector or similar device connected to your PC. When using a large screen such as a projector, a VIVE Tracker is used for viewpoint tracking.

Portalgraph generates imagery based on the screen's size, coordinates, and the user's viewpoint. Because of this, the system requires calibration to understand the screen dimensions and position — this page will walk you through that process.

#### Requirement

* A Windows 10 or later PC (with a GPU, or an Intel Core series CPU from within the past five years or equivalent)
* SteamVR installed
* Portalgraph runtime installed [https://portalgraph.itch.io/portalgraph-runtime](https://portalgraph.itch.io/portalgraph-runtime)
* VIVE Tracker
* A 3D projector or 3D television with compatible 3D glasses

#### Setup

If the Portalgraph runtime is not yet installed, install it first. [https://portalgraph.itch.io/portalgraph-runtime](https://portalgraph.itch.io/portalgraph-runtime)

Next, download a Portalgraph-compatible app, extract the archive, and run it. [https://portalgraph.itch.io/persona-portal-kagerou](https://portalgraph.itch.io/persona-portal-kagerou)

#### Initial Setup

Type "Tracker Portalgraph" into the Start menu search bar to launch the VIVE Tracker tracking application. On first launch, a message will appear prompting you to adjust your settings. Because VIVE Trackers are configured by default to be used together with a VR headset, you will need to change the settings to allow use without one. Click "Fix" and then follow the on-screen instructions to exit SteamVR.



#### Display Settings

Launch the Portalgraph application and press **F12** while it is running to open the settings screen.

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

Enter the number of displays on which to show the Portalgraph view in the "View Count" field on the right, then enter the display number on which you want to show the screen (1 = main display, 2 and above = sub-displays; this depends on your environment).

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

**Click "Apply" to apply the values — changes will not take effect unless you click Apply. If the screen you are using changes, you will need to restart the application. After restarting, press F12 again to reopen this screen.**

"Tracker Position" specifies where the VIVE Tracker will be attached. Forehead is recommended in most cases. Attach the tracker so that the USB port faces in the direction of the red arrow.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

If "Auto-launch tracker app" is checked, the tracker app will launch automatically when the application starts. Selecting OpenVR will cause the VIVE Tracker tracking application to launch automatically.



Click "Next" to open the calibration screen.

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

From the 3D dropdown, select the 3D mode that matches your 3D projector, 3D television, or other device:

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

* **Side-By-Side** — Left-right split 3D
* **Top-And-Bottom** — Top-bottom split 3D
* **Anaglyph** — Red-blue 3D glasses. The color split method can be selected from the dropdown on the right.
* **2D** — No 3D output
* **2 outputs** — Splits the left-eye and right-eye images across two separate video outputs. The left-eye image is output to the screen currently being configured, and the right-eye image is output to the screen selected in the sub-display dropdown.

***

After configuring the settings, use the VIVE Tracker to calibrate the screen. Click "Tracker" to open the tracker settings screen. Enter the screen size in meters, click "Calibrate," align the tracker to the center of the screen, and wait for the countdown to complete — calibration will then be applied automatically.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

Close the settings screen, put on your VIVE Tracker and 3D glasses, and look at the screen to experience a VR space expanding from within it.

<figure><img src="../.gitbook/assets/IMG_6760_.jpg" alt=""><figcaption></figcaption></figure>

