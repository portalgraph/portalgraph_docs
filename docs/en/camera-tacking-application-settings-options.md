# Camera Tacking Application Settings Options

This section explains how to configure head tracking using a webcam.

#### Portalgraph Settings

Launch an application built with Portalgraph and open the settings screen (by default, press F12). Check the "Auto-launch Tracker App" option, then select "Camera" from the dropdown below it. The camera tracking software will launch automatically the next time the application starts.

<figure><img src=".gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Set Tracker Position to "EyeCenter".

<figure><img src=".gitbook/assets/image (23) (1).png" alt=""><figcaption></figcaption></figure>

Click "Next" to proceed to the calibration screen, then click "Camera."

<figure><img src=".gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

If you are using a webcam built into your PC located just above the screen with a standard 16:9 monitor, enter the screen size in the camera tracking settings screen and click OK.

<figure><img src=".gitbook/assets/Screenshot 2024-11-09 160131.png" alt=""><figcaption></figcaption></figure>

If that is not the case, check Advanced Mode, manually enter the screen size, and input the camera's position and rotation. For XYZ, the positive directions are up, right, and away from you (into the screen) when facing the screen, respectively.

<figure><img src=".gitbook/assets/Screenshot 2024-11-09 160142.png" alt=""><figcaption></figcaption></figure>

#### Camera Tracking App Settings

The camera tracking app is preconfigured for standard built-in PC webcams, so if you are using your device's built-in camera, simply select the camera and click Apply to complete the setup.

<figure><img src=".gitbook/assets/cameraEn.png" alt=""><figcaption></figcaption></figure>

If you are using a non-standard camera or want more accurate tracking, click "Calibration" to start a countdown. Use a measuring tape or similar tool to measure the distance, and position your face so that your eyes are exactly 50 cm directly in front of the camera. When the countdown finishes, the camera's field of view and focal length will be adjusted.

<figure><img src=".gitbook/assets/spaces_aJCTlOkQcgkhVMLcuHBm_uploads_CB72gJJtC3gZNAc2iyek_image.webp" alt=""><figcaption></figcaption></figure>

The following tips will help ensure a comfortable experience:

* Keep the camera resolution low to reduce CPU load (640×360 is sufficient).
* A camera with high FPS support provides better responsiveness.
* A wide field-of-view camera allows you to move within a larger area, but distortion increases toward the edges of the field of view.
* The developer uses this camera, which supports a 120-degree field of view and 60 fps: [https://amzn.asia/d/8dBhXX2](https://amzn.asia/d/8dBhXX2)
* You can check your camera's supported resolutions and FPS under "Video settings" in the Windows Camera app settings.
