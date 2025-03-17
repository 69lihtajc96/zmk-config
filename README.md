# ZMK Configuration for 69lihtajc96

Welcome to my personal ZMK firmware configuration repository! 🎉 This repo, hosted at [https://github.com/69lihtajc96/zmk-config](https://github.com/69lihtajc96/zmk-config), contains a custom setup for my keyboard, optimized for efficiency and convenience. Built on the open-source ZMK Firmware (licensed under MIT), this configuration allows me to tailor my keymap, macros, and combos to suit my workflow. Whether you're here to explore, fork, or contribute, let’s dive into the details! 🚀

## Overview

This repository defines a custom keymap and behavior configuration for my ZMK-based keyboard. It includes:
- **Multiple Layers**: Letters, numbers, symbols, function keys, and a manager layer for toggling.
- **Combos**: Quick shortcuts for launching applications like YouTube and social media platforms.
- **Macros**: Automated key sequences for streamlined actions.
- **Custom Keybindings**: Tailored to my daily use, with support for modifiers and special functions.

ZMK Firmware is a modern, wireless keyboard firmware built on the Zephyr RTOS, designed for flexibility and ease of use. This config leverages its power to create a personalized typing experience without needing a complex toolchain—thanks to GitHub Actions for automated builds!

## Getting Started

### Prerequisites
- A GitHub account.
- A ZMK-compatible keyboard (e.g., nice!nano or similar).
- Basic knowledge of Git for cloning and pushing changes.

### Setup Instructions
1. **Fork this Repository**:
   - Click the "Fork" button on the top right of this GitHub page to create your own copy.
2. **Clone the Repo**:
   - Run `git clone https://github.com/69lihtajc96/zmk-config.git` in your terminal.
3. **Configure Your Keyboard**:
   - Edit the `keymap` and `combos` sections in the `.dtsi` file (details below) to match your hardware (board and shield).
   - Update the `build.yaml` file with your target keyboard if needed.
4. **Build the Firmware**:
   - Push your changes to your forked repo. GitHub Actions will automatically build the firmware.
   - Check the "Actions" tab, download the `.uf2` file from the latest build, and flash it to your keyboard by double-clicking the reset button to enter bootloader mode, then dragging the `.uf2` file onto the device.
5. **Test and Customize**:
   - Test the keymap and adjust as needed. Submit a pull request if you’d like to contribute back!

For detailed ZMK setup instructions, visit the [official ZMK documentation](https://zmk.dev/docs/getting-started).

## Key Features

### Layers
This configuration includes multiple layers for different use cases:

- **Letters (Base Layer)**:
  - Standard QWERTY layout with modifiers (Ctrl, Shift, GUI, Alt).
  - Accesses numbers and symbols via layer switches (e.g., `MO(1)` for numbers, `MO(2)` for symbols).

- **Numbers Layer (Layer 1)**:
  - Maps 1-0, arrow keys, and Bluetooth controls (e.g., `BT1`-`BT5`).
  - Activated with `MO(1)`.

- **Symbols Layer (Layer 2)**:
  - Includes special characters (!, @, #, etc.) and additional symbols.
  - Activated with `MO(2)`.

- **Function Keys Layer (Layer 3)**:
  - Maps F1-F12 keys for quick access.
  - Activated with `MO(3)`.

- **Functionality Layer (Layer 4)**:
  - Includes utility keys like Print Screen, Delete, and Calculator.
  - Toggled with `TOG(4)`.

- **Layer Manager Layer (Layer 5)**:
  - Allows toggling layers 4 and 5.
  - Activated with `MO(5)`.

### Combos
Combos are multi-key shortcuts that trigger specific actions. Here are the defined combos:

| **Combo Name** | **Key Positions** | **Action**          | **Layer** | **Timeout (ms)** |
|----------------|-------------------|---------------------|-----------|------------------|
| `YouTube`      | 7, 9, 4, 2        | Launches YouTube    | 0         | 2                |
| `Social`       | 19, 21, 14, 16    | Launches Social Apps| 0         | Not specified    |

- **Key Positions**: Refer to the matrix positions in the `keymap` (e.g., 7 = Y, 9 = U, 4 = E, 2 = W for YouTube).
- **How to Use**: Press the four keys simultaneously (or within the timeout) to trigger the macro.

### Macros
Macros automate complex key sequences. Here are the defined macros:

| **Macro Name**  | **Sequence**                                                                 | **Label**      | **Wait (ms)** | **Tap (ms)** |
|-----------------|-------------------------------------------------------------------------------|----------------|---------------|--------------|
| `Start_Youtube` | `LEFT_GUI` + `1 F` + `LCTRL L` + `LS(LEFT_ALT) ENTER` + `Y T` + `ENTER`       | `START_ALL`    | 15            | 5            |
| `Start_Social`  | `LEFT_GUI` + `2 F` + `LS(LEFT_ALT) ENTER` + `D S` + `ENTER` + `LCTRL T` + `T G ENTER` + `LEFT_GUI A` + `LS(E L E M E N T ENTER)` | `START_SOCIAL` | 15            | 5            |

- **How to Use**: Triggered via the respective combo (e.g., YouTube combo runs `Start_Youtube`).
- **Purpose**: Opens YouTube or a social media app (e.g., Discord, Telegram) with a single combo press.

### Keymap Layout
Below is a textual representation of the base `letters` layer keymap:

```
-----------------------------------------------------------------------------------------
|  TAB |  Q  |  W  |  E  |  R  |  T  |   |  Y  |  U  |  I  |  O  |  P  | BKSP |
| CTRL |  A  |  S  |  D  |  F  |  G  |   |  H  |  J  |  K  |  L  |  ;  |  '   |
| SHFT |  Z  |  X  |  C  |  V  |  B  |   |  N  |  M  |  ,  |  .  |  /  | ESC  |
           | GUI | LWR | SPC |   | ENT | RSE | ALT |
-----------------------------------------------------------------------------------------
```
- **LWR**: Switches to the numbers layer (`MO(1)`).
- **RSE**: Switches to the symbols layer (`MO(2)`).

## Contributing
Feel free to fork this repo, tweak the keymap, or add new combos/macros! Here’s how:
1. Fork the repository.
2. Make your changes (e.g., update `keymap` or `combos`).
3. Submit a pull request with a description of your changes.
4. I’ll review and merge if it rocks! 🎸

## License
This project is licensed under the MIT License, as per the ZMK Contributors' copyright (see the header in the `.dtsi` file).

## Acknowledgements
- Thanks to the [ZMK Firmware community](https://zmk.dev) for the awesome framework!
- Inspired by the flexibility of ZMK’s user-configurable design.

## Feedback
Got questions or suggestions? Open an issue or drop me a message. Let’s make this config even better together! 😄

---

### Notes
- The README assumes the user has basic familiarity with ZMK but provides enough detail for newcomers.
- Key positions (e.g., 7, 9, 4, 2) are based on the matrix defined in your `keymap` and may need adjustment if your keyboard’s layout differs.
- The macros are interpreted as launching YouTube and social media apps (e.g., Discord, Telegram) based on the key sequences, but you can clarify their exact purpose if needed.
