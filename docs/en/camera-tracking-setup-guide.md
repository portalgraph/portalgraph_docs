---
description: >-
  This guide explains the configuration steps for using a webcam for head
  tracking.
---

# Camera Tracking Setup Guide

## Portalgraph Settings

Run the application created with Portalgraph and open the settings menu (usually by pressing F12). Check the option for "Tracker App Auto Start," then select **Camera** from the dropdown menu below. This setting will automatically start the camera tracking software the next time the application is launched.

<figure><img src=".gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Select **EyeCenter** as the tracker position, then click **Apply**. If the eye coordinates and eye rotation values are all set to zero, no further configuration is needed.



<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Click **Next** to proceed to the calibration screen, then click **Camera**.

<figure><img src=".gitbook/assets/Screenshot 2024-11-09 160124.png" alt=""><figcaption></figcaption></figure>

If you are using a built-in webcam positioned just above a standard 16:9 monitor, enter the screen size in the camera tracking settings screen and click **OK**.

<figure><img src=".gitbook/assets/Screenshot 2024-11-09 160131.png" alt=""><figcaption></figcaption></figure>

If this is not the case, check **Advanced Mode**, then manually enter the screen size and specify the camera’s coordinates and angles. For the XYZ axes, positive directions are upward, to the right, and foward, respectively, relative to the screen.

<figure><img src=".gitbook/assets/Screenshot 2024-11-09 160142.png" alt=""><figcaption></figcaption></figure>

## Camera tracking Application Setting

The camera tracking app is pre-configured for a standard built-in PC webcam, so if you are using an internal camera, simply select the camera and click **Apply** to complete the setup.

<figure><img src=".gitbook/assets/cameraEn.png" alt=""><figcaption></figcaption></figure>

If you are using a specialized camera, click **Calibration** to start a countdown. During this countdown, use a measuring tool to position your face so that your eyes are exactly 50 cm in front of the camera. Once the countdown finishes, the camera’s field of view and focal length will be adjusted accordingly.

<figure><img src=".gitbook/assets/spaces_aJCTlOkQcgkhVMLcuHBm_uploads_CB72gJJtC3gZNAc2iyek_image.webp" alt=""><figcaption></figcaption></figure>

Here are some tips to enhance your experience:

* **Lower Camera Resolution:** Set the camera resolution lower to reduce CPU load (640×360 is sufficient).
* **High-FPS Camera:** A high-FPS camera improves responsiveness.
* **Wide-Angle Camera:** A wide-angle camera allows for more movement within the frame but may introduce distortion towards the edges of the field of view.
* **Recommended Camera:** The developer uses a camera with a 120-degree field of view and 60fps.
* **Check Camera Specs:** You can verify the camera’s supported resolution and FPS in the Windows Camera app under "Video Settings."
