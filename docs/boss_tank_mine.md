# BossTankMine

The BossTankMine script is responsible for controlling the behavior of the mines dropped by the boss tank during a boss battle.

## Properties

- `explosion`: A GameObject representing the explosion effect when the mine is triggered.

## Methods

### `Start()`

This method is called before the first frame update.

### `Update()`

This method is called once per frame.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when a Collider2D component enters the mine's trigger area. It checks if the collider belongs to the player. If so, it performs the following actions:

1. Destroys the mine GameObject.
2. Instantiates the explosion effect at the mine's position.
3. Calls the `DealDamage()` method from the PlayerHealthController to deal damage to the player.
4. Calls the `PlaySFX()` method from the AudioManager to play the explosion sound effect.

### `Explode()`

This method is called when the mine needs to be destroyed without player interaction (e.g., when the boss tank is hit). It performs the following actions:

1. Destroys the mine GameObject.
2. Calls the `PlaySFX()` method from the AudioManager to play the explosion sound effect.
3. Instantiates the explosion effect at the mine's position.
