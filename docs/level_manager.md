# LevelManager

The LevelManager script is responsible for managing the level state and handling tasks such as player respawn and level completion.

## Properties

### `instance`

A static instance of the LevelManager class for easy access from other scripts.

### `gemsCollected`

An integer that keeps track of the number of gems collected in the current level.

### `levelToLoad`

A string that stores the name of the next level to load upon completing the current level.

### `timeInLevel`

A float that keeps track of the time spent in the current level.

### `waitToRespawn`

A float that determines the duration to wait before respawning the player.

## Methods

### `Awake()`

This method initializes the `instance` property to reference the LevelManager instance.

### `Start()`

This method initializes the `timeInLevel` to 0 at the start of the level.

### `Update()`

This method updates the `timeInLevel` property with the time spent in the current level.

### `RespawnPlayer()`

This method is responsible for respawning the player by calling the `RespawnCo()` coroutine.

### `RespawnCo()`

This coroutine handles the player respawn process. It deactivates the player, plays a sound effect, fades the screen to black, repositions the player at the spawn point, restores player health, updates the UI, and fades the screen back in.

### `EndLevel()`

This method is responsible for ending the level by calling the `EndLevelCo()` coroutine.

### `EndLevelCo()`

This coroutine handles the level completion process. It plays the level victory sound, stops player input and camera follow, displays the level complete text, fades the screen to black, updates PlayerPrefs with level completion data, and loads the next level.

## Usage

Attach this script to a game object in your level, such as an empty game object named "LevelManager". The script will manage player respawns and level completion events, updating the player's progress and transitioning to the next level when appropriate.
