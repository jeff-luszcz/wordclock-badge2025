# Word Clock for GitHub Universe 2025 Badge

This app displays the current time using easy-to-read words on the badge screen. Designed for the GitHub Universe 2025 badge, the Word Clock automatically sets the time using NTP and WiFi connectivity.

## Features

- **Word-based time display:** Shows the current time in words (e.g., “It is ten past five”).
- **Automatic time sync:** Fetches the exact time from an NTP server.
- **WiFi-enabled:** Connects to your local WiFi network for accurate timekeeping.

## Installation

1. **Copy the app:** Copy the `wordclock` directory to your badge’s `apps` folder.
2. **Configure WiFi:**  
   - Edit the `secrets.py` file in the badge’s root directory.
   - Add your WiFi SSID and password as shown:
     ```python
     WIFI_SSID = "YourNetworkSSID"
     WIFI_PASSWORD = "YourPassword"
     ```
3. **Set your timezone:**  
   - Edit `wordclock/__init__.py`.
   - Set your location’s offset from UTC. For example:
     ```python
     UTC_OFFSET = -8  # California (PST)
     ```
   - Use your own offset (e.g., 1 for Berlin, -5 for New York).

## Usage

1. Put the badge into app mode and select “Word Clock” from the apps list.
2. The app will initialize, enabling WiFi and connecting to the NTP server. This takes approximately **5-10 seconds** on first run.
3. The screen will show the current time in words once setup is complete.

## Troubleshooting

- **WiFi not connecting?**
  - Double-check your SSID and password in `secrets.py`.
  - Make sure your badge is within range of your WiFi network. 
  
- **Time incorrect?**
  - Ensure your UTC offset in `wordclock/__init__.py` is set for your local time zone.

## Contributing

Pull requests, bug reports, and improvements welcome!  
Feel free to submit issues or suggestions via GitHub.


## Info

https://github.com/jeff-luszcz/wordclock-badge2025

## License

This repository is licensed under the terms of the MIT license
