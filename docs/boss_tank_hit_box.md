# BossTankHitBox

The BossTankHitBox script is responsible for handling the behavior of the boss tank's hitbox during a boss battle.

## Properties

- `bossCont`: A reference to the BossTankController component associated with the boss tank.

## Methods

### `Start()`

This method is called before the first frame update.

### `Update()`

This method is called once per frame.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when a Collider2D component enters the hitbox's trigger area. It checks if the collider belongs to the player and if the player's position is above the hitbox. If both conditions are met, it performs the following actions:

1. Calls the `TakeHit()` method from the BossTankController to handle the hit.
2. Calls the `Bounce()` method from the PlayerController to make the player bounce.
3. Deactivates the hitbox GameObject.
