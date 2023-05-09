# BossBullet

The BossBullet script is responsible for controlling the behavior of the bullets fired by the boss during a boss battle.

## Properties

- `speed`: A float value representing the speed at which the bullet moves.

## Methods

### `Start()`

This method is called before the first frame update. It plays a sound effect using the `PlaySFX()` method from the AudioManager.

### `Update()`

This method is called once per frame. It updates the bullet's position based on its speed, local scale, and the elapsed time since the last frame.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when a Collider2D component enters the trigger area. It checks if the collider belongs to the player by verifying the "Player" tag. If the collider belongs to the player, it performs the following actions:

1. Calls the `DealDamage()` method from the PlayerHealthController to deal damage to the player.
2. Plays a sound effect using the `PlaySFX()` method from the AudioManager.
3. Destroys the BossBullet GameObject.
