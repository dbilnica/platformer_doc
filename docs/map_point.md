# MapPoint

The `MapPoint` script represents a point in the overworld map. It contains information about the level it's associated with, the points it's connected to, and the badges earned for the level.

## Properties

- `up`, `right`, `down`, `left` (MapPoint): The points in the map connected to this point.
- `isLevel` (bool): A flag indicating whether this point represents a level.
- `isLocked` (bool): A flag indicating whether the level represented by this point is locked.
- `levelToLoad` (string): The name of the level scene to load for this point.
- `levelToCheck` (string): The name of the level scene to check for unlocking this point.
- `levelName` (string): The name of the level represented by this point.
- `gemsCollected`, `totalGems` (int): The number of gems collected in this level and the total number of gems.
- `bestTime`, `targetTime` (float): The best time achieved in this level and the target time.
- `gemBadge`, `timeBadge` (GameObject): The badges displayed when the player has collected all gems and achieved the target time.

## Methods

- `Start()`: This method is called before the first frame update. It loads the player's progress for this level from PlayerPrefs, unlocks the level if the requirements are met, and activates badges if the player has earned them.
- `Update()`: This method is called once per frame, but it's not used in this script.
