# Onion-Arduino-Library

Onion library for use with the Arduino IDE and the Arduino Dock. 

Combine the ease of use of Arduino with the flexibility and power of Linux with the Onion Omega!

![Arduino Dock R2](./extras/arduino-dock-r2.jpg)

## Arduino Dock Documentation

Full and up-to-date documentation can be found in our docs site:

* https://docs.onion.io
* https://docs.onion.io/omega2-docs/arduino-dock-2.html
* https://docs.onion.io/omega2-docs/flash-arduino-dock-wirelessly.html#flash-arduino-dock-wirelessly

## Requirements

* Arduino IDE 1.8.0 or later
* [Arduino Dock R2](https://onion.io/store/arduino-dock-r2/)
    * The Arduino Dock R1 model is no longer in production, but still compatible with this library (see "Preparing to Flash" below).
* An Onion Omega board to flash sketches to the Dock:
    * [Omega2](https://onion.io/store/omega2/)
    * [Omega2+](https://onion.io/store/omega2p/)
    * Omega 1 - no longer in production, but still compatible

If you want to buy Onion products outside of the US, you can also find a [local distributor near you](https://onion.io/where-to-buy).

## Installation

1. Open the Arduino IDE and click `Sketch -> Include Library -> Manage Libraries...`
1. Search for `Onion Arduino Library`
1. Click `Install`
1. Close the Library Manager and you're ready to go!

## Contents

This library contains code needed to flash the Arduino Dock R1 model, as well as example sketches that showcase how the Atmel microcontroller and Omega can exchange data and commands.

### Classes

#### `Onion`

* Required for flashing Model R1 units. See "Preparing to Flash" for full instructions.

More information coming soon!

### Example Sketches

You can find example sketches by clicking on `File -> Examples -> Onion`.

### Preparing to Flash

The flashing process will depend if you are using the first model of the Dock (R1) or the second (R2).

Arduino Dock R1:

![Arduino Dock R1](./extras/arduino-dock.png)

Arduino Dock R2 (note the Expansion Header in the left corner of the board):

![Arduino Dock R2](./extras/arduino-dock-r2.jpg)

See the sections below for how to use the library for each model.

#### Model R1

In your sketch, add the Onion Library by clicking in the top menu bar: `Sketch -> Include Library -> Onion`.

![Add the Onion Library](https://i.imgur.com/MjYaLTO.png)

Once the library has been added, create a global instance of the Onion object. Add the following line on the global scope:

```
Onion* onionSetup;
```

To initialize and activate the library functions, add the following line to the `setup()` function in the sketch:

```
onionSetup = new Onion();
```

#### Model R2

We've made sweeping improvements in this revision, so you don't have to include the library to flash it; no additional steps are needed! :)

### Flashing the Arduino Dock

Follow the instructions in our Arduino Dock documentation: 

https://docs.onion.io/omega2-docs/flash-arduino-dock-wirelessly.html
