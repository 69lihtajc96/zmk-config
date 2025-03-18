# 🟣 ZMK Keyboard Configuration for 69lihtajc96

Welcome to my personal ZMK firmware configuration repository! 🎉 This repository, hosted at [GitHub](https://github.com/69lihtajc96/zmk-config), contains my custom keyboard setup optimized for convenience and productivity.

---

## ⌨️ Base Layer

```css
/* Base Layer — Left Side */
┌─────┬─────┬─────┬─────┬─────┬─────┐
│ TAB │  Q  │  W  │  E  │  R  │  T  │
├─────┼─────┼─────┼─────┼─────┼─────┤
│CTRL │  A  │  S  │  D  │  F  │  G  │
├─────┼─────┼─────┼─────┼─────┼─────┤
│SHFT │  Z  │  X  │  C  │  V  │  B  │
└─────┴─────┴─────┴─────┴─────┴─────┘

/* Base Layer — Thumb Keys (Left Side) */
           ┌─────┬─────┬─────┐
           │ GUI │ LWR │ SPC │
           └─────┴─────┴─────┘

/* Base Layer — Right Side */
┌─────┬─────┬─────┬─────┬─────┬─────┐
│  Y  │  U  │  I  │  O  │  P  │ BSP │
├─────┼─────┼─────┼─────┼─────┼─────┤
│  H  │  J  │  K  │  L  │  ;  │  '  │
├─────┼─────┼─────┼─────┼─────┼─────┤
│  N  │  M  │  ,  │  .  │  /  │ ESC │
└─────┴─────┴─────┴─────┴─────┴─────┘

/* Base Layer — Thumb Keys (Right Side) */
           ┌─────┬─────┬─────┐
           │ ENT │ RSE │ ALT │
           └─────┴─────┴─────┘
```

---

## 🔢 Layer 1 — Numbers and Arrows

```css
/* Left Side */
┌─────┬─────┬─────┬─────┬─────┬─────┐
│  1  │  2  │  3  │  4  │  5  │  6  │
├─────┼─────┼─────┼─────┼─────┼─────┤
│LEFT │DOWN │ UP  │RIGHT│ BT1 │ BT2 │
├─────┼─────┼─────┼─────┼─────┼─────┤
│SHFT │     │     │     │     │     │
└─────┴─────┴─────┴─────┴─────┴─────┘

/* Thumb Keys (Layer 1) */
           ┌─────┬─────┬─────┐
           │ GUI │     │ SPC │
           └─────┴─────┴─────┘
```

---

## 🔠 Layer 2 — Symbols

```css
/* Left Side */
┌─────┬─────┬─────┬─────┬─────┬─────┐
│  !  │  @  │  #  │  $  │  %  │  ^  │
├─────┼─────┼─────┼─────┼─────┼─────┤
│  -  │  =  │  [  │  ]  │  \ │  `  │
├─────┼─────┼─────┼─────┼─────┼─────┤
│  _  │  +  │  {  │  }  │ "|" │  ~  │
└─────┴─────┴─────┴─────┴─────┴─────┘

/* Thumb Keys (Layer 2) */
           ┌─────┬─────┬─────┐
           │ GUI │     │ SPC │
           └─────┴─────┴─────┘
```

---

## 🔧 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/69lihtajc96/zmk-config.git
   ```
2. Configure `keymap` and `combos` in the `.dtsi` file to match your layout.
3. Build the firmware via GitHub Actions.
4. Transfer the `.uf2` file to your device.

---

## 📫 Contact

If you have questions or suggestions for improving the configuration — feel free to reach out! 😄

