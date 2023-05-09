# MovingPlatform

The `MovingPlatform` script represents a platform that moves along a set of defined points in your game world.

## Properties

- `points` (Transform[]): An array of points that the platform will move between.
- `moveSpeed` (float): The speed at which the platform moves.
- `currentPoint` (int): The index of the current point in the `points` array that the platform is moving towards.
- `platform` (Transform): The transform of the platform that is being moved.

## Methods

- `Start()`: This method is called before the first frame update, but it's not used in this script.
- `Update()`: This method is called once per frame. It moves the platform towards the current point at the defined speed. If the platform is close enough to the current point, it increments `currentPoint` to move to the next point. If `currentPoint` exceeds the length of the `points` array, it resets `currentPoint` to 0.
