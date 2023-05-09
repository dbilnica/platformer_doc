# KillPlayer

The KillPlayer script is responsible for detecting when the player enters a designated kill zone and triggers the respawn process.

## Methods

### `Start()`

This method is called before the first frame update. Currently, no functionality is implemented in this method.

### `Update()`

This method is called once per frame. Currently, no functionality is implemented in this method.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when the attached 2D collider detects a collision with another 2D collider. It checks if the other collider has a "Player" tag, and if so, it triggers the `RespawnPlayer()` method from the LevelManager instance.

## Usage

Attach this script to any game object that represents a kill zone, such as a pit or a spike trap. The game object should have a 2D collider with the "Is Trigger" option enabled. When the player enters the collider, the script will call the `RespawnPlayer()` method to respawn the player at the last checkpoint or the beginning of the level.
