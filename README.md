# Break Reminder Application

## Overview
This Python script provides a simple break reminder system that notifies the user every hour to take a break. It's designed to promote healthy work habits by preventing prolonged periods of uninterrupted work, which can lead to eye strain, fatigue, and decreased productivity.

## Features
- **Hourly notifications**: Reminds the user to take a break every 60 minutes
- **System notifications**: Uses the native notification system of your operating system
- **Non-intrusive**: Notifications appear briefly (10 seconds) without interrupting workflow
- **Lightweight**: Runs in the background with minimal resource usage

## Requirements
- Python 3.x
- plyer library (for cross-platform notifications)

## Installation
1. Ensure you have Python 3 installed on your system
2. Install the required dependencies using pip:
   ```bash
   pip install plyer
   ```

## Usage
1. Run the script:
   ```bash
   python break_reminder.py
   ```
2. The script will run in the background and display a notification every hour
3. To stop the reminder, simply terminate the script (Ctrl+C in the terminal)

## Customization
You can easily modify the script to suit your preferences:

### Change the notification interval
Edit the `time.sleep(3600)` line:
- 3600 seconds = 1 hour
- 1800 seconds = 30 minutes
- 2700 seconds = 45 minutes

### Modify notification content
Edit the `notification.notify()` parameters:
```python
notification.notify(
    title="YOUR CUSTOM TITLE",
    message="Your custom message here",
    timeout=10  # Duration in seconds
)
```

## Platform Support
The script works on:
- Windows
- macOS
- Linux (with notification server like libnotify)

## Troubleshooting
1. **Notifications not appearing**:
   - Ensure your system supports notifications
   - On Linux, install libnotify (`sudo apt install libnotify-bin` for Debian/Ubuntu)
   - Check if other applications can display notifications

2. **Script termination issues**:
   - Use `Ctrl+C` to stop the script
   - On some systems, you may need to use `Ctrl+Z` followed by `kill %1`

## Best Practices
- Consider running this script when starting your work session
- Pair with other health practices like the 20-20-20 rule (every 20 minutes, look at something 20 feet away for 20 seconds)
- Adjust the interval based on your personal productivity rhythms

## License
This script is open-source and free to use under the MIT License. Feel free to modify and distribute it as needed.

## Contribution
Contributions are welcome! Please fork the repository and submit a pull request for any improvements.

## Version
Current version: 1.0.0
