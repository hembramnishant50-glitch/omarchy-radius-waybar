<div align="center">

# ⭕ Omarchy Radius Waybar
**A minimalist, modular Waybar theme built for modern Linux setups.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Waybar](https://img.shields.io/badge/Status-Stable-16AB2A)](https://github.com/Alexays/Waybar)
[![Platform](https://img.shields.io/badge/Platform-Wayland-39515A)](https://wayland.freedesktop.org/)

<img width="100%" alt="Omarchy Radius Preview" src="https://github.com/user-attachments/assets/e505d542-1859-4458-abd9-5cd61c622a88" />

---

[Features](#-features) • [Weather Setup](#-weather-setup) • [Installation](#-installation) • [Colors](#-color-palette)

</div>

## ✨ Features
* **Modular Island Design:** Clean separation between bar elements.
* **Dynamic Battery:** Smart color shifting (**#16AB2A** discharging, **#F58E27** charging).
* **Weather Integration:** Live temperature updates via `wttr.in`.
* **Minimalist Aesthetic:** High transparency with subtle borders for a modern glass look.

---

## ⛅ Weather Setup
Update your `config.jsonc` with the following block:

```json
"custom/weather": {
    "format": "󰖐 {}°C",
    "interval": 3600,
    "exec": "curl -s 'wttr.in/CITY_NAME?format=%t' | grep -oE '[0-9]+'",
    "on-click": "xdg-open '[https://www.google.com/search?q=weather+CITY_NAME](https://www.google.com/search?q=weather+CITY_NAME)'"
}



- Install
```bash
omarchy-theme-install https://github.com/hembramnishant50-glitch/omarchy-radius.git
   ```

## 🚀 Installation
1. Backup your current configuration
Rename your existing waybar folder to waybarback to keep it as a backup:

Bash

mv ~/.config/waybar ~/.config/waybarback
2. Install Omarchy Radius
Bash

# Clone the repository
git clone [https://github.com/YOUR_USERNAME/omarchy-radius-waybar.git](https://github.com/YOUR_USERNAME/omarchy-radius-waybar.git)

# Create the directory and copy files
mkdir -p ~/.config/waybar
cp -r omarchy-radius-waybar/* ~/.config/waybar/
3. Apply Changes
Reload Waybar to see the new theme:

Bash

killall waybar && waybar &
<div align="center"> <br /> <sub>Built with ❤️ for the Linux Ricing community</sub> </div>
