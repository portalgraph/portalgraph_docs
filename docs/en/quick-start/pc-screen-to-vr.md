# Turn Your PC Screen into a VR Space

This page explains how to use the freely distributed Unity-chan Live Stage! for Portalgraph to enjoy an existing Portalgraph app. Using a standard PC monitor, webcam-based viewpoint tracking, and anaglyph (red-blue) glasses, you can experience a VR space that appears to emerge from inside your screen. This is designed for PC screens up to 30 inches, viewed from within 1 meter of the display.

Portalgraph generates imagery based on the screen's size and position along with the user's viewpoint. Because of this, the system requires calibration to understand the screen dimensions and how the camera sees the environment — this page will walk you through that process.

<figure><img src="../.gitbook/assets/image.avif" alt=""><figcaption></figcaption></figure>

## Requirements

* **Operating System:** Windows 10 or later
* **Portalgraph Runtime Installation:** [Download here](https://portalgraph.booth.pm/items/6256749)
* **Webcam**
* **Red-Blue(Cyan) 3D Glasses:**&#x20;
  * [Amazon](https://a.co/d/hm6o0UR)

## How to Use

If the Portalgraph runtime is not yet installed, install it first.

[https://portalgraph.itch.io/portalgraph-runtime](https://portalgraph.itch.io/portalgraph-runtime)

Next, download Unity-chan Live Stage! for Portalgraph, extract the archive, and double-click UnityChan CRS.exe to launch it.

[https://portalgraph.itch.io/portalgraph-free-demos](https://portalgraph.itch.io/portalgraph-free-demos)

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

The camera tracking app will launch automatically. Select your camera, click "Apply," and return to the Unity-chan Live Stage window.

<figure><img src="../.gitbook/assets/cameraEn.png" alt=""><figcaption></figcaption></figure>

## \*If the camera image is not displayed:

Close the camera tracking app and Unity-chan Live Stage, install the VC++ Runtime, and relaunch.

[https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

## Calibration

Portalgraph needs to know the size and coordinates of your screen in order to operate, so you will enter these values through calibration.

On the first launch of the Portalgraph application, the camera tracking calibration screen will be displayed. (If it does not appear, press F12 to open the settings screen, then click "Next" → "Camera.")

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160131.png" alt=""><figcaption></figcaption></figure>

Enter your screen size.

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160124.png" alt=""><figcaption></figcaption></figure>

Click "Close" and Unity-chan will appear inside your screen. Put on your anaglyph (red-blue) glasses to see her moving in 3D from any angle.

<figure><img src="../.gitbook/assets/image.avif" alt=""><figcaption></figcaption></figure>

The Portalgraph application supports the following keyboard controls by default:

* **WASD R F** — Move forward/back/left/right/up/down (hold Shift for slow movement)
* **Q E T G Z C** — Rotate left/right, up/down, and tilt (hold Ctrl to rotate in 90° increments)
* **1 2** — Change scale
* **3** — Reset scale

Adjust the camera position, angle, and scale to match the size and orientation of your screen.

### ※ If the image appears distorted

#### Camera Adjustment

The camera tracking app is calibrated by default for the field of view (FOV) of a typical webcam. If your camera has a significantly different FOV, please calibrate the camera tracking app.

<figure><img src="../.gitbook/assets/cameraEn.png" alt=""><figcaption></figcaption></figure>

Click "Calibration" to begin a countdown. Position yourself so that your eyes are 50 cm directly in front of the camera and wait — the values will be set automatically.

<figure><img src="../.gitbook/assets/spaces_aJCTlOkQcgkhVMLcuHBm_uploads_CB72gJJtC3gZNAc2iyek_image.webp" alt=""><figcaption></figcaption></figure>

#### Entering the Exact Screen Size

If your PC does not have a standard 16:9 display, or if the camera is not positioned directly above the center of the screen, the image may not display correctly. In that case, configure the following in the Unity-chan Live Stage! app.

Press F12 in the Unity-chan Live Stage window to open the settings screen.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Click "Next."

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160124.png" alt=""><figcaption></figcaption></figure>

Click "Camera" to open the camera tracking calibration screen.

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160131.png" alt=""><figcaption></figcaption></figure>

Check "Advanced Mode."

<figure><img src="../.gitbook/assets/Screenshot 2024-11-09 160142.png" alt=""><figcaption></figcaption></figure>

Measure your monitor's dimensions and enter the screen size in meters. For camera position, use the dropdown to select the camera's position relative to the screen (Top, Bottom, Left, Right, or Center), then enter the offset from that position in meters. The X, Y, and Z axes correspond to right, up, and forward relative to the screen, respectively. Enter the camera angle only if your camera is not perpendicular to the screen (this normally does not need to be changed).

Click "OK" → "Close" after entering your values and the image should display correctly.
