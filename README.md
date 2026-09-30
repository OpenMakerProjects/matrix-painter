# Matrix Painter

Control a chain of MAX7219 8×8 LED matrices from a Processing desktop application or an optional iOS client.

## Provenance and licence

- Original source: [`matrix-painter` in mattiasjahnke/arduino-projects](https://github.com/mattiasjahnke/arduino-projects/tree/master/matrix-painter)
- Reviewed upstream revision: [`45373bc`](https://github.com/mattiasjahnke/arduino-projects/tree/45373bc41f01b8a12860bd6de89f43958e0c71e9/matrix-painter)
- Original author and copyright holder: Mattias Jähnke
- Licence: MIT; see [LICENSE](LICENSE)

Generated Carthage build products and dependency checkouts were removed. The iOS project retains its dependency lock file so dependencies can be restored from their original sources and licences.

## Supported boards

- Arduino Uno or a compatible AVR board exposing hardware SPI

## Parts list

- 1 × Arduino Uno-compatible board
- 5 × MAX7219-based 8×8 LED matrix modules (the sketch is configured for five horizontal displays)
- Regulated 5 V supply sized for the display chain
- Jumper wires and USB cable
- Optional macOS computer running Processing
- Optional iOS device and Mac with Xcode

## Required libraries and tools

### Arduino

- Arduino `SPI` library
- Adafruit GFX Library
- Max72xxPanel library

### Desktop and iOS

- Processing with its Serial and Network libraries
- Xcode for the optional iOS client
- SwiftSocket and Flow, restored using the iOS project's dependency configuration

## Wiring

| Matrix signal | Arduino Uno |
| --- | --- |
| VCC | Regulated 5 V |
| GND | GND |
| DIN | D11 / MOSI |
| CS | D10 |
| CLK | D13 / SCK |

## Schematic status

No dedicated schematic file is present. The wiring table above is preserved from the upstream documentation. Confirm supply current, grounding, signal direction and the pinout printed on each matrix module before powering the chain.

## Review status

Source, provenance and licence were checked for publication. Generated binaries and vendored dependency trees were excluded. Hardware and iOS builds have not been independently reproduced by OpenMakerProjects.
