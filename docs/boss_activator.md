# BossActivator

The BossActivator script is responsible for activating a boss battle when the player enters a specific trigger area.

## Properties

- `bossBattle`: A GameObject representing the boss battle that will be activated when the player enters the trigger area.

## Methods

### `OnTriggerEnter2D(Collider2D other)`

This method is called when a Collider2D component enters the trigger area. It checks if the collider belongs to the player by verifying the "Player" tag. If the collider belongs to the player, it performs the following actions:

1. Activates the boss battle by setting the `bossBattle` GameObject to active.
2. Deactivates the BossActivator GameObject.
3. Calls the `PlayBossMusic()` method from the AudioManager to play the boss music.
