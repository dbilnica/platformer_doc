# UIController

The `UIController` script manages the User Interface (UI) elements in the game, including health display, gem count, screen fade, and level completion text.

## Properties

- `instance` (UIController): A static instance of UIController, allowing other scripts to access its public methods and properties.
- `heart1`, `heart2`, `heart3` (Image): Image UI components representing the player's health.
- `heartFull`, `heartHalf`, `heartEmpty` (Sprite): Sprites representing full, half, and empty heart states.
- `gemText` (Text): Text UI component that displays the number of collected gems.
- `fadeScreen` (Image): Image UI component that is used to fade the screen to and from black.
- `fadeSpeed` (float): The speed at which the screen fades.
- `shouldFadeToBlack`, `shouldFadeFromBlack` (bool): Booleans controlling whether the screen should fade to or from black.
- `levelCompleteText` (GameObject): GameObject representing the text displayed when a level is completed.

## Methods

- `Awake()`: Initializes the `instance`.
- `Start()`: Updates the gem count and fades in from black at the start of the game.
- `Update()`: Handles the screen fading to or from black.
- `UpdateHealthDisplay()`: Updates the heart images based on the player's current health.
- `UpdateGemCount()`: Updates the displayed gem count based on the current number of collected gems.
- `FadeToBlack()`: Initiates the screen fade to black.
- `FadeFromBlack()`: Initiates the screen fade from black.
