# PauseMenu

The `PauseMenu` script allows players to pause the game at any time by pressing the Escape key. It also provides options to navigate to the Level Select screen or the Main Menu.

## Properties

- `instance` (static PauseMenu): A singleton instance of the PauseMenu. This allows other scripts to access the public members of PauseMenu.
- `levelSelect` (string): The name of the Level Select scene.
- `mainMenu` (string): The name of the Main Menu scene.
- `pauseScreen` (GameObject): The UI object that is displayed when the game is paused.
- `isPaused` (bool): A flag indicating whether the game is currently paused.

## Methods

- `Awake()`: This method sets the singleton instance of the PauseMenu.
- `Start()`: This method is called before the first frame update, but it's not used in this script.
- `Update()`: This method is called once per frame. It listens for the Escape key, and if pressed, it triggers the `PauseUnpause()` method.
- `PauseUnpause()`: This method toggles the pause state of the game. If the game is currently paused, it unpauses the game, hides the pause screen, and resumes the game time. If the game is not paused, it pauses the game, shows the pause screen, and stops the game time.
- `LevelSelect()`: This method saves the current level to player preferences and then loads the Level Select scene. It also resumes the game time.
- `MainMenu()`: This method loads the Main Menu scene and resumes the game time.