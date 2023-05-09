# BouncePad

The BouncePad script is responsible for handling the behavior of bounce pads in the game, which launch the player into the air when they come into contact with them.

## Properties

- `anim`: A reference to the Animator component associated with the bounce pad.
- `bounceForce`: The force with which the player is launched into the air when they touch the bounce pad.

## Methods

### `Start()`

This method is called before the first frame update. It initializes the `anim` property with the Animator component attached to the bounce pad.

### `Update()`

This method is called once per frame.

### `OnTriggerEnter2D(Collider2D other)`

This method is called when a Collider2D component enters the bounce pad's trigger area. It checks if the collider belongs to the player. If so, it performs the following actions:

1. Updates the player's Rigidbody2D velocity with the specified `bounceForce` in the vertical direction, while keeping the horizontal velocity unchanged.
2. Triggers the "Bounce" animation on the bounce pad.
