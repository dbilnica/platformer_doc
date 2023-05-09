# MainMenu

The `MainMenu` script controls the behavior of the main menu in the game, including the start, continue, and quit functions.

## Properties

- `startScene` (string): The name of the scene that should be loaded when the player starts a new game.
- `continueScene` (string): The name of the scene that should be loaded when the player continues an existing game.
- `continueButton` (GameObject): The continue button in the main menu.

## Methods

- `Start()`: This method is called before the first frame update. It checks whether the start scene has been unlocked, and if so, it enables the continue button. Otherwise, it disables the continue button.
- `Update()`: This method is called once per frame, but it's not used in this script.
- `StartGame()`: This method starts a new game by loading the start scene and deleting all player preferences.
- `ContinueGame()`: This method continues an existing game by loading the continue scene.
- `QuitGame()`: This method quits the game.
