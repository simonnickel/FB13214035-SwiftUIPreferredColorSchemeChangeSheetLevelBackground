# FB13214035 - Setting PreferredColorScheme to .dark in .sheet does not properly shade the background behind the sheet


## Scenario

An app opens a sheet to show a toggle to override the preferredColorScheme of the app.
The device is in .light colorScheme.
When the toggle is enabled it is set to .dark via preferredColorScheme.


## Issue

The update to dark color scheme does not properly shade the background behind the sheet. Only after the sheet is moved down a bit, the background is colored correctly. See screenshots for better understanding:

Right after the preferredColorScheme is set: The background does not show the level below the sheet, its all black.
![A](./A.png)

As soon as the sheet moves a bit, the background shows.
![B](./B.png)

Sheet drag is released, the right background color is maintained.
![C](./C.png)


## Example Code

The example shows a Button to open the sheet.
The sheet contains a toggle to override to dark mode.

Device: Any iPhone Simulator.

1. Make sure the device is in light mode.
2. Open the sheet.
3. Enable the toggle.
-> The background is wrong
4. Drag the sheet a few pixel.
-> The background appears.
 

## Tested on

 - Xcode Version 15.0 (15A240d): iPhone 15 Pro (iOS 17.0 (21A328)) Simulator
