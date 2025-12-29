Omarchy Radius Waybar
A minimalist, modular Waybar theme designed for clarity and aesthetics.

🌦️ Weather Module Configuration
The custom/weather module uses a simple curl fetch from wttr.in. Use the template below in your config.jsonc:

JSON

"custom/weather": {
    "format": "󰖐 {}°C",
    "interval": 3600,
    "exec": "curl -s 'wttr.in/CITY_NAME?format=%t' | grep -oE '[0-9]+'",
    "on-click": "xdg-open 'https://www.google.com/search?q=weather+CITY_NAME'"
}
🛠️ How to Customize Your Location
1. Update the Fetch Command (exec)
This line retrieves the temperature.

Find: wttr.in/CITY_NAME

Change: Replace CITY_NAME with your city.

Note: If your city name has a space (e.g., San Francisco), use a + instead: San+Francisco.

2. The Filter (grep)
The pipe command | grep -oE '[0-9]+' acts as a filter. It strips symbols like + or °C from the raw data, leaving only the digits. This ensures the Waybar format string handles the styling consistently.

3. Interaction (on-click)
Update the URL at the end of the on-click line to ensure clicking the module opens the correct local forecast in your browser:

Example: ?q=weather+london

🎨 Styling Note
If you are using the Omarchy Radius color palette, remember to check your style.css for consistent padding and border-radius to match the modular "island" look.
