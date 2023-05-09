# Stompbox

The `Stompbox` script controls the behavior of an object that can be stomped on by the player. When stomped on, it has a chance to drop a collectible.

## Properties

- `deathEffect` (GameObject): The effect that is instantiated when the stompbox is stomped on.
- `collectible` (GameObject): The collectible that may be dropped when the stompbox is stomped on.
- `chanceToDrop` (float): The chance that a collectible will be dropped when the stompbox is stomped on.

## Methods

- `Start()`: This method is called before the first frame update. It currently does not perform any actions.
- `Update()`: This method is called once per frame. It currently does not perform any actions.
- `OnTriggerEnter2D(Collider2D other)`: This method is called when another object enters the stompbox's trigger area. If the other object is tagged as an "Enemy", the stompbox deactivates the enemy, instantiates the death effect, and makes the player bounce. It also has a chance to drop a collectible.