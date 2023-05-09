# LSUIController

The `LSUIController` script controls the UI on the level selection screen. This includes fading the screen to and from black and displaying level information.

## Properties

- `fadeScreen` (Image): The UI image used for screen fading.
- `fadeSpeed` (float): The speed at which the screen fades.
- `shouldFadeToBlack` (bool): A flag indicating whether the screen should fade to black.
- `shoudlFadeFromBlack` (bool): A flag indicating whether the screen should fade from black to clear.
- `levelInfoPanel` (GameObject): The UI panel displaying level information.
- `levelName` (Text): The UI text component displaying the level name.
- `gemsFound` (Text): The UI text component displaying the number of gems found.
- `gemsTarget` (Text): The UI text component displaying the target number of gems in the level.
- `bestTime` (Text): The UI text component displaying the player's best time.
- `timeTarget` (Text): The UI text component displaying the target time for the level.

## Methods

- `Awake()`: This method is called when the script instance is being loaded. It sets the static instance of LSUIController to this instance.
- `Start()`: This method is called before the first frame update. It initiates a fade from black.
- `Update()`: This method is called once per frame. It handles screen fading based on the `shouldFadeToBlack` and `shoudlFadeFromBlack` flags.
- `FadeToBlack()`: This method sets the screen to fade to black.
- `FadeFromBlack()`: This method sets the screen to fade from black to clear.
- `ShowInfo(MapPoint levelInfo)`: This method takes a MapPoint object and updates the level info panel with its data, then displays the panel.
- `HideInfo()`: This method hides the level info panel.
