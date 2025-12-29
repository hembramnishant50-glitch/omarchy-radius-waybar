# omarchy-radius-waybar
The Omarchy Radius is a minimalist, modular Waybar theme

<img width="1920" height="76" alt="Image" src="https://github.com/user-attachments/assets/e505d542-1859-4458-abd9-5cd61c622a88" />


Note :- 
custom/weather

"custom/weather": {
    "format": "󰖐 {}°C",
    "interval": 3600, // Updates every hour (3600 seconds)
    "exec": "curl -s 'wttr.in/CITY_NAME?format=%t' | grep -oE '[0-9]+'",
    "on-click": "xdg-open 'https://www.google.com/search?q=weather+CITY_NAME'"
} 


Step-by-Step Guide to Changing Location
1. The exec Line (The Display)
This is what fetches the temperature you see on your bar.

Find: wttr.in/New+York

Change: Replace New+York with any city name.

Rule: If the city name has a space (like San Francisco), use a + sign instead of a space: San+Francisco.


2. The grep Command (The Cleanup)
The | grep -oE '[0-9]+' part is a filter.

Why it's there: By default, wttr.in might return +22°C. This command strips away the + and the °C so that only the number (22) is passed to Waybar. This allows your format string to handle the styling.

3. The on-click Line (The Interaction)
This determines what happens when you click the weather icon.

Change: Update the query at the end of the URL: ?q=weather+city+name.

This ensures that when you click, your browser opens the full forecast for the correct city.
