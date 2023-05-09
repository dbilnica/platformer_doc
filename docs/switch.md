# Switch

The `Switch` script controls the behavior of a switch object in the game. The switch can be activated by the player to toggle the active state of another object.

## Properties

- `objectToSwitch` (GameObject): The object that the switch will toggle the active state of.
- `SR` (SpriteRenderer): The SpriteRenderer component attached to the switch object. This is used to change the sprite of the switch when it is activated.
- `downSprite` (Sprite): The sprite that the switch will change to when it is activated.
- `hasSwitched` (bool): A boolean that keeps track of whether the switch has already been activated.
- `deactivateOnSwitch` (bool): A boolean that determines whether the switch deactivates or activates the `objectToSwitch` when activated.

## Methods

- `Start()`: This method is called before the first frame update. It initializes the `SR` variable with the SpriteRenderer component attached to the switch object.
- `Update()`: This method is called once per frame. It currently does not perform any actions.
- `OnTriggerEnter2D(Collider2D other)`: This method is called when another object enters the switch's trigger area. If the other object is tagged as "Player" and the switch has not already been activated, it toggles the active state of the `objectToSwitch` and changes the sprite of the switch to `downSprite`.