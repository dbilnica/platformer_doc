# LSManager

The `LSManager` script manages the level selection screen in the game. It sets the player's starting position based on the last level played and handles level loading.

## Properties

- `player` (LSPlayer): A reference to the LSPlayer instance.
- `allPoints` (MapPoint[]): An array of all MapPoint objects in the scene.

## Methods

- `Start()`: This method is called before the first frame update. It initializes the `allPoints` array by finding all MapPoint objects in the scene. It then sets the player's position based on the last level played, stored in PlayerPrefs under the key "CurrentLevel".
- `Update()`: This method is called once per frame, but it's not used in this script.
- `LoadLevel()`: This method initiates the level-loading coroutine.
- `LoadLevelCo()`: This coroutine plays a sound effect, fades the screen to black, and loads the scene associated with the player's current MapPoint.