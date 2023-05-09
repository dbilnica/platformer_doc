# CameraController

The CameraController script is responsible for handling the camera's movement in the game, following the player while also adjusting the background parallax effect.

## Properties

- `instance`: A singleton instance of the CameraController class.
- `target`: The Transform of the target object the camera should follow (usually the player).
- `farBackground`: The Transform of the far background layer.
- `middleBackground`: The Transform of the middle background layer.
- `minHeight`: The minimum height (Y-axis value) the camera should follow the target.
- `maxHeight`: The maximum height (Y-axis value) the camera should follow the target.
- `lastPos`: The last recorded position of the camera.
- `stopFollow`: A boolean flag to indicate if the camera should stop following the target.

## Methods

### `Awake()`

This method initializes the `instance` property as a singleton instance of the CameraController class.

### `Start()`

This method is called before the first frame update. It initializes the `lastPos` property with the initial position of the camera.

### `Update()`

This method is called once per frame. If the `stopFollow` flag is set to `false`, the following actions are performed:

1. Update the camera's position to follow the target's X-axis value, while clamping its Y-axis value between `minHeight` and `maxHeight`.
2. Calculate the amount of movement the camera has made since the last frame.
3. Update the positions of the `farBackground` and `middleBackground` layers according to the camera's movement to create a parallax effect.
4. Update the `lastPos` property with the current position of the camera.
