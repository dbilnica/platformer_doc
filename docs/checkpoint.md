# Checkpoint

The Checkpoint script is responsible for handling checkpoint activation and deactivation in the game. When a player reaches a checkpoint, the checkpoint is activated, and the spawn position is set to the checkpoint's position.

## Properties

- `SR`: The SpriteRenderer component of the checkpoint.
- `cpOn`: The Sprite representing the activated checkpoint.
- `cpOff`: The Sprite representing the deactivated checkpoint.

## Methods

### `Start()`

This method is called before the first frame update but is currently empty.

### `Update()`

This method is called once per frame but is currently empty.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when a 2D collider enters the checkpoint's trigger area. If the collider is tagged as "Player":

1. Deactivate all checkpoints using `CheckpointController.instance.DeactivateCheckpoints()`.
2. Set the checkpoint's sprite to the activated sprite (`cpOn`).
3. Set the spawn point of the player to the checkpoint's position using `CheckpointController.instance.SetSpawnPoint(transform.position)`.

### `ResetCheckpoint()`

This method resets the checkpoint to the deactivated state by setting the sprite to the deactivated sprite (`cpOff`).
