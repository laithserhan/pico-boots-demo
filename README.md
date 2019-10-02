[![Build Status](https://travis-ci.org/hsandt/pico-boots-demo.svg?branch=master)](https://travis-ci.org/hsandt/pico-boots-demo)
[![codecov](https://codecov.io/gh/hsandt/pico-boots-demo/branch/master/graph/badge.svg)](https://codecov.io/gh/hsandt/pico-boots-demo)

# pico-boots demo

This project demonstrates the features of the [pico-boots framework for PICO-8](https://github.com/hsandt/pico-boots).

You can both try the demos directly by running the game (see "Build and run" section) and read the corresponding source code.

## Demos

* `main.lua` shows how to use the Flow system with gamestates. There is no specific demo for it, the whole app uses it, with 1 state for the main menu and 1 state per demo.
* `main_menu.lua` shows how to make a simple menu using the UI and Input modules. You will see the main menu when starting the app.
* `input_demo.lua` shows how to detect player input. In the main menu, select "INPUT DEMO", then press the different buttons (arrows and X/O in PICO-8) to see the input states change.

## Build

### Supported platforms

Mostly UNIX, and specifically Linux for some scripts.

See Supported platforms in [pico-boots](https://github.com/hsandt/pico-boots) README for more information.

### Build dependencies

See *Build dependencies* in [pico-boots](https://github.com/hsandt/pico-boots) README.

### Build and run

First, make sure the `pico8` executable is in your path.

The most straightforward way to build and run the game on Unix platforms is:

* `cd path/to/pico-boots-demo`
* `./build_game.sh`
* `./run_game.sh`

### Test dependencies

See *Test dependencies* in [pico-boots](https://github.com/hsandt/pico-boots) README.

### Run unit tests and headless integration tests

To run all the (non-#mute) unit tests:

* `cd path/to/pico-boots-demo`
* `./test.sh`

### Run rendered integration tests

Integration tests consists in actual game simulations in predetermined scenarios. Therefore, they are built with picotool and run directly in PICO-8. To build the integration test cartridge and run it:

* `cd path/to/pico-boots-demo`
* `./build_itest.sh`
* `./run_itest.sh`

## Coding conventions

Strings that are used as keys and are never shown to the user are written as `':key'` to imitate Ruby's symbol notation.
