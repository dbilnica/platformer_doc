# PlayerHealthController

The `PlayerHealthController` script controls the player character's health and handles damage and healing events.

## Properties

- `currentHealth`, `maxHealth` (int): The current and maximum health of the player character.
- `invincibleLength` (float): The duration for which the player character is invincible after taking damage.
- `invincibleCounter` (float): A counter used to determine how long the player character remains invincible.
- `SR` (SpriteRenderer): The SpriteRenderer component attached to the player character.
- `deathEffect` (GameObject): The effect displayed when the player character dies.

## Methods

- `Awake()`: This method sets the static instance of the PlayerHealthController class.
- `Start()`: This method is called before the first frame update. It initializes the player character's health and the `SR` component.
- `Update()`: This method is called once per frame. It handles the invincibility timer and the player character's sprite transparency.
- `DealDamage()`: This method decreases the player character's health, handles the player character's death, initiates the invincibility timer, and updates the health display.
- `HealPlayer()`: This method increases the player character's health and updates the health display.
- `OnCollisionEnter2D(Collision2D other)`: This method is called when the player character starts colliding with another object. If the other object is a platform, it sets the player character's parent to the platform.
- `OnCollisionExit2D(Collision2D other)`: This method is called when the player character stops colliding with another object. If the other object is a platform, it removes the player character's parent.
