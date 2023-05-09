# BossTankController

The BossTankController script is responsible for controlling the behavior of the boss tank during a boss battle. It manages the boss's states, movement, shooting, and health.

## Enumerations

- `states`: An enumeration representing the possible states of the boss tank (shooting, hurt, moving, ended).

## Properties

- `currentState`: A variable to store the current state of the boss tank, using the `states` enumeration.
- `boss`: A Transform component representing the boss tank.
- `anim`: An Animator component for controlling boss tank animations.

### Movement

- `moveSpeed`: A float value representing the movement speed of the boss tank.
- `leftPoint`, `rightPoint`: Transform components representing the left and right boundaries for the boss tank's movement.
- `moveRight`: A boolean value indicating whether the boss tank is moving right.

### Mine

- `mine`: A GameObject representing the mine prefab.
- `minePoint`: A Transform component representing the position where mines are instantiated.
- `timeBetweenMines`: A float value representing the time interval between dropping mines.
- `mineCounter`: A float value for counting down to the next mine drop.

### Shooting

- `bullet`: A GameObject representing the bullet prefab.
- `firePoint`: A Transform component representing the position where bullets are instantiated.
- `timeBetweenShots`: A float value representing the time interval between shooting bullets.
- `shotCounter`: A float value for counting down to the next bullet shot.

### Hurt

- `hurtTime`: A float value representing the duration of the hurt state.
- `hurtCounter`: A float value for counting down the remaining hurt time.
- `hitBox`: A GameObject representing the hitbox of the boss tank.

### Health

- `health`: An integer representing the health of the boss tank.
- `explosion`: A GameObject representing the explosion effect when the boss tank is defeated.
- `winPlatform`: A GameObject representing the platform that appears when the boss tank is defeated.
- `isDefeated`: A boolean value indicating whether the boss tank is defeated.
- `shotSpeedUp`, `mineSpeedUp`: Float values representing the rate at which the boss tank's shot and mine dropping speeds increase after each hit.

## Methods

### `Start()`

This method initializes the boss tank's state to `shooting`.

### `Update()`

This method updates the boss tank's behavior based on its current state. It handles shooting bullets, dropping mines, moving between points, taking hits, and transitioning between states.

### `TakeHit()`

This method is called when the boss tank takes a hit. It reduces the boss tank's health, updates its state to `hurt`, and increases the difficulty of the battle by speeding up bullet and mine dropping.

### `EndMovement()`

This method is called when the boss tank reaches the left or right boundary of its movement. It updates the boss tank's state to `shooting` and starts shooting immediately.

