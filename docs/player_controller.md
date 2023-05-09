# PlayerController

The `PlayerController` script controls the player character's movement and handles interactions such as jumping, double-jumping, and knockback.

## Properties

- `moveSpeed` (float): The speed at which the player character moves horizontally.
- `RB` (Rigidbody2D): The Rigidbody2D component attached to the player character.
- `jumpForce` (float): The force applied when the player character jumps.
- `isGrounded` (bool): A flag indicating whether the player character is currently touching the ground.
- `groundCheckPoint` (Transform): The point at which to check if the player character is touching the ground.
- `whatIsGround` (LayerMask): A LayerMask indicating what layers should be considered as "ground".
- `canDoubleJump` (bool): A flag indicating whether the player character can currently double jump.
- `SR` (SpriteRenderer): The SpriteRenderer component attached to the player character.
- `knockBackLength`, `knockBackForce` (float): The duration and force of the knockback when the player character is hit.
- `knockBackCounter` (float): A counter used to determine how long to apply knockback.
- `anim` (Animator): The Animator component attached to the player character.
- `bounceForce` (float): The force applied when the player character bounces.
- `stopInput` (bool): A flag indicating whether to ignore player input.

## Methods

- `Awake()`: This method sets the static instance of the PlayerController class.
- `Start()`: This method is called before the first frame update. It initializes the `anim` and `SR` components.
- `Update()`: This method is called once per frame. It handles player input and updates the player character's state accordingly. This includes moving the character, making the character jump or double jump, flipping the character's sprite based on direction, and applying knockback.
- `KnockBack()`: This method applies knockback to the player character and plays the "hurt" animation.
- `Bounce()`: This method makes the player character bounce and plays a sound effect.