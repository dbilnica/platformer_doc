# AudioManager

The AudioManager script is responsible for managing audio in the platformer game. It controls background music, level end music, boss music, and various sound effects.

## Properties

- `instance`: A static reference to the AudioManager instance.
- `soundEffects`: An array of AudioSource components representing various sound effects.
- `bgmusic`: An AudioSource component for the background music.
- `levelEndMusic`: An AudioSource component for the music played at the end of a level.
- `bossMusic`: An AudioSource component for the music played during a boss battle.

## Methods

### `Awake()`

This method is called when the script instance is being loaded. It initializes the AudioManager's `instance` property to the current script instance.

### `PlaySFX(int sound)`

This method takes an integer parameter `sound` representing the index of the sound effect to play. It stops the sound effect if it's already playing, adds a random pitch variation, and then plays the sound effect.

### `PlayLevelVictory()`

This method stops the background music and plays the level end music when a level is completed.

### `PlayBossMusic()`

This method stops the background music and starts the boss music during a boss battle.

### `StopBossMusic()`

This method stops the boss music and resumes the background music after a boss battle has ended.
