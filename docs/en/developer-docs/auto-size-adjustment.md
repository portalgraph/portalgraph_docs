---
description: Auto Size Adjustment
---

# Auto Size Adjustment

Normally, Portalgraph displays objects at the size specified in Unity so that they appear at real-world scale regardless of screen size. This means that a 170 cm tall person would not fit on screen unless using a very large display. However, a feature exists to automatically adjust the world scale to fit the screen.

Set the **Auto Screen Height** field on the Portalgraph prefab's Portalgraph component to the height you want to fit within the screen. The scale will be adjusted automatically so that the specified size fits. To display a person 170 cm tall, enter **2** to scale the world so that 2 meters fits within the screen height.

Note that if the screen height is larger than the specified size, the scale will remain at 1×.

By default, Portalgraph uses the following key bindings:

* **1** — Scale down
* **2** — Scale up
* **3** — Reset (both size and position)

When resetting, the scale will be set to the auto-adjusted value rather than 1×.
