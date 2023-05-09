# Slammer

The `Slammer` script controls an object (the slammer) that moves towards a target when the player character gets close to the slammer or enters its trigger area.

## Properties

- `theSlammer`, `slammerTarget` (Transform): The slammer and its target.
- `startPoint` (Vector3): The initial position of the slammer.
- `slamSpeed`, `waitAfterSlam`, `resetSpeed` (float): The speed at which the slammer moves towards its target, the time it waits after reaching its target, and the speed at which it returns to its initial position.
- `waitCounter` (float): A counter used to determine how long the slammer waits after reaching its target.
- `slamming`, `resetting` (bool): Flags to determine whether the slammer is moving towards its target or returning to its initial position.

## Methods

- `Start()`: This method is called before the first frame update. It sets the `startPoint` to the slammer's initial position.
- `Update()`: This method is called once per frame. It controls the slammer's movements.
- `OnTriggerEnter2D(Collider2D other)`: This method is called when the player character enters the slammer's trigger area. It initiates the slamming process if the slammer is not already slamming or resetting.