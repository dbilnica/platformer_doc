# LSCamera

The `LSCamera` script controls the camera movement in the game. It follows the player's movement while ensuring the camera remains within defined boundaries.

## Properties

- `minPos` (Vector2): The minimum X and Y coordinates the camera is allowed to move to.
- `maxPos` (Vector2): The maximum X and Y coordinates the camera is allowed to move to.
- `target` (Transform): The target object the camera follows, usually set to the player's transform.

## Methods

- `Start()`: This method is called before the first frame update, but it's not used in this script.
- `LateUpdate()`: This method is called once per frame after the Update function, which ensures the camera moves after the player has moved. It clamps the camera's position to the defined min and max positions, then updates the camera's position to follow the target.