# LevelExit

The LevelExit script is responsible for detecting when the player reaches the designated level exit and triggers the end of the level.

## Methods

### `Start()`

This method is called before the first frame update. Currently, no functionality is implemented in this method.

### `Update()`

This method is called once per frame. Currently, no functionality is implemented in this method.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when the attached 2D collider detects a collision with another 2D collider. It checks if the other collider has a "Player" tag, and if so, it triggers the `EndLevel()` method from the LevelManager instance.

## Usage

Attach this script to a game object that represents the level exit, such as a door or a portal. The game object should have a 2D collider with the "Is Trigger" option enabled. When the player enters the collider, the script will call the `EndLevel()` method to trigger the end of the level and transition to the next scene or display the end-of-level screen.
