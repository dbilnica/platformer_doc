# CheckpointController

The CheckpointController script manages checkpoints in the game. It's responsible for deactivating checkpoints and setting the spawn point when a player reaches a new checkpoint.

## Properties

- `instance`: The singleton instance of the CheckpointController class.
- `checkpoints`: An array of Checkpoint objects in the scene.
- `spawnPoint`: The current spawn point in the game.

## Methods

### `Awake()`

This method initializes the singleton instance of the CheckpointController.

### `Start()`

This method is called before the first frame update. It initializes the following properties:

- `checkpoints`: Find all Checkpoint objects in the scene using `FindObjectsOfType<Checkpoint>()`.
- `spawnPoint`: Set the initial spawn point to the player's starting position using `PlayerController.instance.transform.position`.

### `Update()`

This method is called once per frame but is currently empty.

### `DeactivateCheckpoints()`

This method deactivates all checkpoints in the scene by calling the `ResetCheckpoint()` method on each checkpoint in the `checkpoints` array.

### `SetSpawnPoint(Vector3 newSpawnPoint)`

This method sets the spawn point to the specified position, `newSpawnPoint`.
