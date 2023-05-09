# DestroyOverTime

The DestroyOverTime script is responsible for destroying a game object after a specified amount of time has passed.

## Properties

### `lifeTime`

This float variable determines the time (in seconds) the game object should exist before being destroyed.

## Methods

### `Start()`

This method is called before the first frame update, but it is currently empty.

### `Update()`

This method is called once per frame. It calls the `Destroy()` method on the game object, passing in the `lifeTime` variable as an argument. The game object will be destroyed after the specified `lifeTime` duration.
