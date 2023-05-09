# DamagePlayer

The DamagePlayer script is responsible for damaging the player when the player enters the trigger area of an object with this script attached.

## Methods

### `Start()`

This method is called before the first frame update, but it is currently empty.

### `Update()`

This method is called once per frame but is also currently empty.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when the collider attached to the object with this script (typically a hazard or enemy) comes into contact with another collider. If the other collider has a "Player" tag, the `DealDamage()` method of the `PlayerHealthController` instance is called to apply damage to the player.
