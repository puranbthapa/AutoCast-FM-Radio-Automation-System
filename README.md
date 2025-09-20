# AutoCast FM Radio Automation System

## Overview

AutoCast is a complete automation solution for FM radio stations, providing scheduled playback of music, jingles, advertisements, and time checks. The system uses Winamp as the underlying player and supports various audio formats.

## Features

- **Scheduled Programming**: Detailed schedule management by day of week
- **Content Management**: Organized playback of different content types
- **Automatic Time Checks**: Time announcements at configurable intervals
- **Advertisement Blocks**: Scheduled advertisement playback
- **Jingle Rotation**: Random selection from jingle libraries
- **Music Scheduling**: Smart music selection with shuffle capabilities
- **Logging System**: Comprehensive action and error logging
- **User Interface**: Status display showing current and upcoming content

## System Requirements

- **Operating System**: Windows 10 or newer
- **Dependencies**:
  - Python 
  - Winamp media player
  - library
- **Hardware**: 
  - Minimum 4GB RAM
  - 1GB free disk space for application
  - Additional space for media files

## Installation

1. **Setup Python Environment**:
  
2. **Install Winamp**:
   - Download and install Winamp from [winamp.com](https://www.winamp.com)

3. **Organize Content Directories**:
   - Create folders for your content types (music, jingles, ads, time checks)
   - Follow the folder structure documented in the Configuration section

4. **Configure Schedules**:
   - Edit the schedule files for each day of the week
   - Use the Schedule Editor tool (see "Schedule Management" section)

## Quick Start

1. **Start the system**:
   ```
   start_automation
   ```

2. **Monitor Operation**:
   - The application window shows current playback status
   - Check logs in the `logs` directory for detailed operation information

## Content Organization

AutoCast looks for content in the following directories:

- **Music**: 
- **Jingles**: 
- **Advertisements**: 
- **Time Checks**: 

Supported file formats:
- Audio: `.mp3`, `.wav`, `.ogg`, `.mpeg`
- Playlists: `.m3u8`, `.m3u`, `.pls`
- Video with audio: `.mp4` (audio only is played)

## Schedule Management

### Schedule File Format
Schedule files are named by day: `monschedule.txt`, `tueschedule.txt`, etc.
Each line follows this format:
```
HH:MM=ACTION=PATH=ACTION=PATH...
```
### Content Types (Actions)

1. **TIME_CHECK**: Time announcements
2. **JINGLE**: Station jingles
3. **ADS**: Advertisements
4. **MUSIC**: Music tracks
5. **BHAJANS**: Religious content
6. **OLD LOK GEET**: Traditional songs

### Using the Schedule Editor

For detailed instructions on using the Schedule Editor, see [SCHEDULE_MANAGEMENT_MANUAL.md](SCHEDULE_MANAGEMENT_MANUAL.md).

## Logging System

The system maintains comprehensive logs to help monitor operation and troubleshoot issues:

- **Action Log**: Records all system actions with timestamps
  - Location: `logs/action_log.txt`
  - Contents: Program starts, schedule parsing, file playback, etc.

- **Error Log**: Records errors and exceptions
  - Location: `logs/error_log.txt`
  - Contents: File access issues, playback problems, etc.

Logs use automatic rotation to prevent excessive file sizes (5MB limit with 5 backup files).

## Advanced Configuration

### Schedule Templates

The system supports schedule templates for easier management. Templates are defined in:
```
templates/schedule_templates.json
```

Schedule patterns (repeated hourly formats) are defined in:
```
templates/schedule_patterns.json
```

### Content Selection Rules

- **Random Selection**: Jingles and similar content are selected randomly
- **Shuffle Play**: Music files are shuffled before playback
- **Duplication Avoidance**: The system tries to avoid recently played tracks
- **File Limits**: Maximum of 30 music files per slot to prevent overruns

## Troubleshooting

### Common Issues

1. **No Sound**:
2. **Missed Schedules**:
3. **Playback Problems**:

### Log Analysis

When troubleshooting:
1. Check `logs/action_log.txt` for system actions
2. Check `logs/error_log.txt` for specific errors
3. Review the application console output for immediate issues

## License Information

AutoCast uses a hardware-locked licensing system:
- License is verified at startup through multiple security layers

## License and Vendor Protection

AutoCast incorporates multiple layers of security to protect against unauthorized modifications:

- **Vendor Information Verification**: Ensures authenticity of the software provider
- **License Validation**: Checks license expiration and hardware binding
- **Tamper Protection**: Detects unauthorized changes to system files
- **Secure Storage**: Uses encryption to protect sensitive information

If the system detects any unauthorized changes to vendor information or licensing data, it will:
1. Display a warning message
2. Log the security issue
3. Prevent the software from running

## File Structure

- `start_automation`: Easy startup script
- `*schedule.txt`: Daily schedule files
- `license.json`: License information (do not modify manually)
- `logs/`: System and error logs
- `templates/`: Schedule templates and patterns
- `vendor`: Vendor information management utility (admin use only)
- `setup_vendor`: Batch file for vendor setup (admin use only)

## Support and Updates

For support, bug reports, or feature requests:
1. Check the logs for specific error information
2. Contact the vendor directly using the information below
3. Keep your system and dependencies updated

## Vendor Information
**License Information:**
- This software is licensed only to the original purchaser
- License is hardware-locked and non-transferable
- Unauthorized modification or redistribution is strictly prohibited
- License validity can be checked in license.json

## Administration

### Vendor Management Utility
For system administrators only, AutoCast includes a vendor information management utility:
```
setup_vendor
```

This utility allows authorized administrators to:
- Verify the integrity of vendor information
- Update license information
- Validate system security settings

**Note:** This utility requires administrative access and should only be used by authorized personnel.

---

© 2025 Eastlink Cloud Pvt. Ltd. All rights reserved. 
