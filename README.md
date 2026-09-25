# Logitech G HUB Operator Recoil Automation Tool

SETUP GUIDE HERE. https://www.youtube.com/watch?v=OXSRYlvN44A

A high-performance **Lua script** engineered for Logitech G HUB (and compatible programmable peripheral environments) that automates hardware-level mouse cursor correction. The script contains predefined offset parameters calibrated for weapon handling profiles in competitive tactical shooters.

> ⚠️ **Disclaimer:** This software is provided strictly for educational purposes, input telemetry research, and private development testing. Use of input automation macros in public multiplayer environments may violate the Terms of Service (ToS) of specific video games and lead to account restrictions.

## ⚡ Core Engine Features

* **Dynamic Profile Cycling:** Quickly cycle forward or backward through predefined operator profiles utilizing side mouse buttons (Mouse 4 and Mouse 5) with real-time log feedback.
* **Caps Lock Safety Toggle:** Built-in hardware switch verification (`IsKeyLockOn`) ensures the script only executes macro loops when Caps Lock is toggled on.
* **Humanized Randomization Engine:** Integrates a pseudo-random mathematical modifier (`math.random`) to break up rigid geometric mouse travel lines and simulate natural micro-adjustments.
* **Progressive Bullet-Based Ramping:** Features optional initial timing dampening configurations (`ENABLE_RAMPING`) to apply extra weight to high-recoil initial shots.

## ⚙️ Configuration Variables

| Variable | Default Value | Description |
| :--- | :--- | :--- |
| `ADS_REQUIRED` | `true` | Requires right-click or middle-mouse input to trigger tracking loops. |
| `RECOIL_SLEEP` | `10` | The frequency (in milliseconds) of the cursor position update loop. |
| `LEGIT_MODE` | `true` | Activates input variance generation to alter uniform paths. |
| `RANDOMNESS` | `0.30` | Scaling coefficient applied to the randomization offsets. |

## 🚀 Deployment Instructions

1. Open your peripheral management platform (e.g., **Logitech G HUB**).
2. Navigate to your active profile and open the **Scripting** configuration window.
3. Clear any existing template data and paste the script into the text editor.
4. Save the profile changes (`Ctrl + S`).
5. Toggle your keyboard's **Caps Lock** key to enable or disable execution behavior on-the-fly.

## 📊 Profiles Matrix Sample

The script includes calibrated vectors mapping to specific tracking criteria:
* **Vertical Compensation (`vert`):** Sets the strict downward downward pull strength required to cancel vertical weapon drift.
* **Horizontal Correction (`horizontal`):** Positive integers pull right; negative integers pull left to cancel horizontal sway.
