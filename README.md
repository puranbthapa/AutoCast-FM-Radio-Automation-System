# AutoCast FM Radio Automation System

## Overview

AutoCast is a complete automation solution for FM radio stations, providing scheduled playback of music, jingles, advertisements, and time checks. The system uses Winamp as the underlying player and supports various audio formats.

![AutoCast FM Automation System](https://eastlink.com.np/FM+Radio+Automation+System)

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
  - Python 3.8 or newer
  - Winamp media player
  - Mutagen library (`pip install mutagen`)
- **Hardware**: 
  - Minimum 4GB RAM
  - 1GB free disk space for application
  - Additional space for media files

## Installation

1. **Setup Python Environment**:
  
2. **Install Winamp**:
   - Download and install Winamp from [winamp.com](https://www.winamp.com)
   - Default path should be `C:\Program Files (x86)\Winamp\winamp.exe`

3. **Organize Content Directories**:
   - Create folders for your content types (music, jingles, ads, time checks)
   - Follow the folder structure documented in the Configuration section

4. **Configure Schedules**:
   - Edit the schedule files for each day of the week
   - Use the Schedule Editor tool (see "Schedule Management" section)

## Quick Start

1. **Start the system**:
   ```
   ```
   start_automation.bat
   ```

2. **Monitor Operation**:
   - The application window shows current playback status
   - Check logs in the `logs` directory for detailed operation information

## Content Organization

AutoCast looks for content in the following directories:

- **Music**: `D:\MyFMStation\Automation\MUSIC\`
- **Jingles**: `D:\MyFMStation\Automation\JINGLES\`
- **Advertisements**: `D:\MyFMStation\Automation\ADS\`
- **Time Checks**: `D:\MyFMStation\Automation\TIME CHECK\`

Supported file formats:
- Audio: `.mp3`, `.wav`, `.ogg`, `.mpeg`
- Playlists: `.m3u8`, `.m3u`, `.pls`
- Video with audio: `.mp4` (audio only is played)

## Schedule Management

### Schedule File Format

Schedule files are named by day: `mondayschedule.txt`, `tuesdayschedule.txt`, etc.

Each line follows this format:
```
HH:MM=ACTION=PATH=ACTION=PATH...
```

Example:
```
06:00=TIME_CHECK=time_checks=JINGLE=jingles=ADS=ads=MUSIC=music
17:30=JINGLE=jingles=ADS=ads=JINGLE_2=jingles=MUSIC=music
```

### Content Types (Actions)

1. **TIME_CHECK**: Time announcements
2. **JINGLE**: Station jingles
3. **ADS**: Advertisements
4. **JINGLE_2**: Secondary jingles
5. **MUSIC**: Music tracks
6. **BHAJANS**: Religious content
7. **OLD LOK GEET**: Traditional songs
8. **OLD SAD NEPALI SONGS**: Evening content

### Using the Schedule Editor

For detailed instructions on using the Schedule Editor, see [SCHEDULE_EDITOR_MANUAL.md](SCHEDULE_EDITOR_MANUAL.md).

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
   - Check Winamp is installed correctly
   - Verify audio device settings
   - Check if files exist in the specified paths

2. **Missed Schedules**:
   - Check schedule file format
   - Verify system time is correct
   - Look for errors in the error log

3. **Playback Problems**:
   - Check file formats are supported
   - Verify file paths are correct
   - Look for specific errors in logs/error_log.txt

### Log Analysis

When troubleshooting:
1. Check `logs/action_log.txt` for system actions
2. Check `logs/error_log.txt` for specific errors
3. Review the application console output for immediate issues

## License Information

AutoCast uses a hardware-locked licensing system:
- Current license expiry: See license.json
- For renewals contact: Mr. Puran Thapa (details below)
- System will cease operation after license expiration
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

- `start_automation.bat`: Easy startup script
- `*schedule.txt`: Daily schedule files
- `license.json`: License information (do not modify manually)
- `logs/`: System and error logs
- `templates/`: Schedule templates and patterns
- `vendor_setup`: Vendor information management utility (admin use only)
- `setup_vendor`: Batch file for vendor setup (admin use only)

## Support and Updates

For support, bug reports, or feature requests:
1. Check the logs for specific error information
2. Contact the vendor directly using the information below
3. Keep your system and dependencies updated

## Vendor Information

**Developer and Support:**
- **Name:** Mr. Puran Thapa
- **Company:** Eastlink Cloud Pvt. Ltd.
- **Support Contact:** +977-9801901140
- **Email:** support@eastlink.net.np
- **Address:** Kathmandu, Nepal

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

### License Renewal

When your license is approaching expiration:

1. Contact Mr. Puran Bahadur Thapa at Eastlink Cloud Pvt. Ltd.
2. Provide your system's hardware information (available in license.json)
3. After payment, you'll receive an updated license file
4. Run the vendor setup utility to verify the new license

> **IMPORTANT:** Do not attempt to modify vendor information or license settings manually. Doing so will disable the software. For any license or support needs, contact Mr. Puran Bahadur Thapa at Eastlink Cloud Pvt. Ltd. using the contact information provided above.

---

© 2025 Eastlink Cloud Pvt. Ltd. All rights reserved. 
Developed by Mr. Puran Bahadur Thapa.
