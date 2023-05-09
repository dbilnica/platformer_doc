# FlyingEnemyController

The FlyingEnemyController script is responsible for controlling the movement and behavior of a flying enemy in the game.

## Properties

### `points`

This Transform array represents the waypoints that the flying enemy moves between.

### `moveSpeed`

This float variable determines the speed at which the enemy moves between waypoints.

### `currentPoint`

This int variable keeps track of the current waypoint the enemy is moving towards.

### `SR`

This SpriteRenderer variable represents the SpriteRenderer component of the enemy.

### `distanceToAttackPlayer`

This float variable defines the distance at which the enemy will start attacking the player.

### `chaseSpeed`

This float variable determines the speed at which the enemy chases the player when attacking.

### `attackTarget`

This Vector3 variable represents the position the enemy is targeting during an attack.

### `waitAfterAttack`

This float variable determines the time the enemy waits after completing an attack.

### `attackCounter`

This float variable is used as a counter for the time the enemy spends waiting after an attack.

## Methods

### `Start()`

This method is called before the first frame update. It detaches the waypoints from the enemy's transform hierarchy.

### `Update()`

This method is called once per frame. It handles the enemy's movement between waypoints and attacking the player when in range.

If the attackCounter is greater than 0, the enemy is waiting after an attack. If the enemy is not within the attack range of the player, the enemy moves between waypoints. When the enemy is within attack range, it moves towards the player's position to attack. After reaching the attack target, the enemy waits for a duration determined by the `waitAfterAttack` variable.
