# EnemyController

The EnemyController script is responsible for controlling the movement and behavior of an enemy in the game.

## Properties

### `moveSpeed`

This float variable determines the speed at which the enemy moves.

### `leftPoint` and `rightPoint`

These Transform variables define the left and right boundary points of the enemy's movement range.

### `movingRight`

This boolean variable determines if the enemy is moving to the right (`true`) or to the left (`false`).

### `RB`

This Rigidbody2D variable represents the Rigidbody2D component of the enemy.

### `SR`

This SpriteRenderer variable represents the SpriteRenderer component of the enemy.

### `anim`

This Animator variable represents the Animator component of the enemy.

### `moveTime` and `waitTime`

These float variables define the time the enemy spends moving and waiting between movements, respectively.

### `moveCount` and `waitCount`

These float variables are used as counters for the time the enemy spends moving and waiting.

## Methods

### `Start()`

This method is called before the first frame update. It initializes various components and variables, such as RB, anim, movingRight, and moveCount.

### `Update()`

This method is called once per frame. It handles the enemy's movement, switching between moving and waiting, and updates the Animator's "isMoving" parameter accordingly.

The enemy moves between the left and right boundary points, flipping its sprite when changing directions. The moveCount and waitCount are updated based on the moveTime and waitTime variables, and a random factor is applied to make the enemy's behavior less predictable.
