# Pickup

The `Pickup` script is attached to objects in the game world that the player can collect. These objects can be gems or health pickups.

## Properties

- `isGem` (bool): A flag indicating whether the pickup is a gem.
- `isHeal` (bool): A flag indicating whether the pickup is a health item.
- `isCollected` (bool): A flag indicating whether the pickup has been collected.
- `pickupEffect` (GameObject): A reference to the effect that should be instantiated when the pickup is collected.

## Methods

- `Start()`: This method is called before the first frame update, but it's not used in this script.
- `Update()`: This method is called once per frame, but it's not used in this script.
- `OnTriggerEnter2D(Collider2D other)`: This method is called when the 2D collider on the pickup enters a trigger. It checks if the object that entered the trigger is the player and if the pickup has not been collected yet. If the pickup is a gem, it increments the gem count in `LevelManager`, marks the pickup as collected, destroys the pickup object, instantiates the pickup effect, updates the gem count in the UI, and plays a sound effect. If the pickup is a health item and the player's health is not already at maximum, it heals the player, marks the pickup as collected, destroys the pickup object, instantiates the pickup effect, and plays a sound effect.