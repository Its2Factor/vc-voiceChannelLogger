# Voice Channel Logger

A lightweight Vencord plugin that tracks voice channel joins and leaves in real-time with timestamps and user details.

## Features

- 📊 **Real-time Logging**: Track voice channel activity as it happens
- 🔍 **Advanced Search**: Search logs by user, channel, or action type
- 📱 **Toast Notifications**: Get notified when users join/leave (configurable)
- ⏱️ **Session Duration Tracking**: See how long users stay in voice channels
- 🎨 **Modern UI**: Beautiful modal interface with filtering and pagination
- 💾 **Persistent Storage**: Logs are saved and persist across Discord restarts
- 🔧 **Highly Configurable**: Extensive settings to customize behavior

## Installation

### Using Vencord Plugin Manager

1. Open Vencord Settings
2. Go to the Plugins tab
3. Search for "VoiceChannelLogger"
4. Enable the plugin

### Manual Installation

1. Clone this repository or download the files
2. Copy the `voiceChannelLogger` folder to your Vencord userplugins directory:
   - **Windows**: `%appdata%\Vencord\plugins\userplugins\`
   - **Linux/Mac**: `~/.config/Vencord/plugins/userplugins/`
3. Restart Discord or reload Vencord

## Usage

### Opening the Logs Modal

- Click the voice logger button in the Discord header
- Or use the context menu on any user → "View Voice Logs"

### Features in the Modal

- **Filter by Action**: Filter logs by Join, Leave, or Move actions
- **Search**: Search by username, channel name, or user ID
- **Pagination**: Navigate through logs with page controls
- **Export**: Export logs as JSON (via console command)
- **Statistics**: View summary statistics in the header

### Console Commands

The plugin exposes several console commands for advanced usage:

```javascript
// Export logs as JSON
Vencord.Plugins.plugins.VoiceChannelLogger.exportLogs()

// Clear all logs
Vencord.Plugins.plugins.VoiceChannelLogger.clearLogs()

// Display logs in console
Vencord.Plugins.plugins.VoiceChannelLogger.openLogsInConsole()

// Open logs GUI modal
Vencord.Plugins.plugins.VoiceChannelLogger.openLogsGUI()
```

## Settings

### Core Logging Behavior
- **Enable File Logging**: Save logs to persistent storage
- **Track Session Duration**: Track how long users stay in channels
- **Max Log Entries**: Maximum number of entries to keep (0 = unlimited)

### Filtering Options
- **Log Own Actions**: Log your own voice channel actions
- **Only Log Joins**: Only log when users join (ignore leaves)
- **User Filter**: Only log specific users (comma-separated user IDs)

### Notification Settings
- **Show Toast Notifications**: Show notifications when users join/leave
- **Suppress Toasts for Existing Users**: Don't show toasts for users already in channel
- **Toast Duration**: How long to show toast notifications (seconds)

### UI & Display Settings
- **Logs Per Page**: Number of logs to display per page
- **Use Relative Time**: Show relative timestamps (e.g., "2 minutes ago")

## Requirements

- [Vencord](https://vencord.dev/) Discord client mod
- Discord desktop app

## License

This project is licensed under the GPL-3.0-or-later License - see the [LICENSE](LICENSE) file for details.

## Author

**kylie** (ID: 624679903068946454)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

If you encounter any issues or have questions, please open an issue on GitHub.

---

**Note**: This plugin is part of the Vencord ecosystem. Make sure you have Vencord installed and properly configured before using this plugin.

