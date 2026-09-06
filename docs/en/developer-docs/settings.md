---
description: >-
  Below are the settings for the Portalgraph prefab. Options that do not require
  editing by developers are struck through.
---

# Settings

## Portalgraph game object

<figure><img src="../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

* **Saves Screen Center**\
  When checked, saves the local coordinates of the screen center (`ScreenCenter`) relative to Portalgraph, allowing coordinates to be retained when reopening the scene.
* **Save Name**\
  Name used to save the screen center coordinates. If the same name is used across scenes, the setting will carry over between scenes.
* ~~**Default Screen Center**~~\
  Specifies the screen center point. Default points to `Portalgraph/ScreenCenter`. No editing required.
* ~~**Default Screen**~~\
  Default screen setting, pointing to `Portalgraph/Screens/Screen`. Clone this for additional screens. No editing required.
* **Auto Screen Height**\
  If set above 0, this automatically scales down to fit the screen height if it exceeds the display size at the default scale. It will not scale down if the default scale already fits the screen.
* ~~**Coordinate System**~~\
  Specifies the tracker coordinate system. No editing required.
* **Tracker Type**\
  Type of tracker used. This setting reflects the calibration type available in the calibration screen.
  * **Both**: Both VIVE Tracker and camera
  * **Tracker**: VIVE Tracker only
  * **Camera**: Webcam only
* ~~**Tracker**~~\
  The tracker mounted on the user’s head. No editing required.
* ~~**Eyes**~~\
  Specifies the viewer's eye positions within the `Coordinate System`. No editing required.
* **Screen Eyes**\
  Defines specific **Eyes** for each screen in a multi-screen, multiplayer setup. For example, if using two screens with a separate tracker for the second screen:
  * Copy `Portalgraph/CoordinateSystem/Trackers/HeadTracker`
  * Add the copied `HeadTracker` to the `Trackers` in `OSCServer` within `Portalgraph/CoordinateSystem`
  * Set the number of elements in `ScreenEyes` to 2, and specify the second element as `(Copied HeadTracker)/EyeCenter`
* **Main Camera**\
  Camera displayed on the main screen when the Portalgraph display screen differs from the PC's primary screen.
* **Pops Up**\
  If checked, the image appears to float in front of the screen.
* ~~**Screen Center Matches Origin**~~\
  When checked, `ScreenCenter` is matched to `Origin` every frame (for handheld setups or syncing with a VR headset). Normally left unchecked, keeping the screen center fixed where it was calibrated. No editing required.
* **Calibration Key Code**\
  Key used to open the settings screen.
* ~~**Calibration Grid**~~\
  Grid component displayed during calibration. No editing required.
* **Config File Base Name**\
  The name for the configuration file. Files are saved in the Documents folder and shared across applications. Change this to a unique name if you do not want settings shared with other applications.
* **Uses External Tracker App**\
  When checked, the external tracker app field appears in the settings screen. If this is enabled and the external tracker app is also enabled in the settings, the specified tracker app will launch automatically when starting the application.
* **Calibration Start SE**\
  Sound effect played when calibration starts.
* **Calibration Count Down SE**\
  Sound effect that plays during the countdown in calibration (a timing cue).
* ~~**Calibration Canvas Prefab**~~\
  Prefab for the calibration screen. No editing required.
* ~~**Main Screen Canvas Prefab**~~\
  Prefab for the main settings screen. No editing required.

## Hierarychy Settings

<figure><img src="../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

* **ScreenCenter**\
  Object representing the center coordinates of the display. To move the camera, adjust this object’s position. The attached `ScreenCenterController` enables keyboard control; deactivate it if unnecessary. The move/rotate keys can be reassigned on its Inspector.
* **Screens/Screen**\
  Manages each screen individually. For multiple screens, the system copies this object for each additional screen. To set background color or post-effects, adjust the `Camera` objects under `Cameras`.
* **Camera**\
  If you’re using multiple displays and the first screen is not for Portalgraph, this camera’s output will display on the first screen.
* **CoordinateSystem**\
  Defines the tracking coordinate system. To scale the entire setup, adjust this object. The attached `TransformScaleController` allows scaling via key input; deactivate if not needed.
* **LeftHand, RightHand**\
  Objects representing the right and left hand controllers.
* **OSCServer**\
  Receives communications from the tracking software, defaulting to port 49570. To change the port, modify the `Port` in the attached `UOscServer` component.
