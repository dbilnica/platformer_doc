# LSPlayer

The `LSPlayer` script controls the movement and behavior of the player on the level selection screen. The player moves between MapPoint objects and can trigger level loading.

## Properties

- `currentPoint` (MapPoint): The current MapPoint the player is standing on.
- `moveSpeed` (float): The speed at which the player moves between MapPoints.
- `levelLoading` (bool): A flag indicating whether a level is currently loading.
- `manager` (LSManager): A reference to the LSManager instance.

## Methods

- `Start()`: This method is called before the first frame update, but it's not used in this script.
- `Update()`: This method is called once per frame. It moves the player towards the current MapPoint. If the player is close to the MapPoint and a level isn't currently loading, it handles player input to move to adjacent MapPoints or trigger level loading.
- `SetNextPoint(MapPoint nextPoint)`: This method sets the player's current MapPoint to the specified next point, hides the level info UI, and plays a sound effect.