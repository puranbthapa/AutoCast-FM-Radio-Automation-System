# 🎙️ AutoCast FM Schedule Management Manual

## Professional Broadcasting Schedule System
**Version:** 2.0 Professional Edition  
**Company:** Eastlink Cloud Pvt. Ltd.  
**System:** AutoCast FM Radio Automation  

---

## Table of Contents

1. [Introduction](#introduction)
2. [System Overview](#system-overview)
3. [Getting Started](#getting-started)
4. [Schedule Management Interface](#schedule-management-interface)
5. [Creating Broadcast Schedules](#creating-broadcast-schedules)
6. [Content Management](#content-management)
7. [Advanced Features](#advanced-features)
8. [File Management](#file-management)
9. [Troubleshooting](#troubleshooting)
10. [Best Practices](#best-practices)
11. [Support Information](#support-information)

---

## Introduction

The AutoCast FM Schedule Management System is a professional broadcasting tool designed to create, edit, and manage weekly radio programming schedules. This comprehensive manual will guide you through every aspect of schedule management, from basic operations to advanced features.

### Key Features
- **Professional GUI Interface**: Windows-optimized design with ribbon-style toolbar
- **7-Day Schedule Management**: Complete weekly programming control
- **Real-time Validation**: Immediate feedback on schedule integrity
- **Multiple Content Types**: Support for 30+ broadcast content categories
- **Batch Operations**: Efficient management of multiple time slots
- **Professional Reporting**: Detailed schedule analysis and export
- **Auto-save Functionality**: Never lose your work
- **Encryption Support**: Secure schedule protection

---

## System Overview

### Architecture
The Schedule Manager operates as the central control hub for your AutoCast FM system:

```
Schedule Manager GUI ↔ Schedule Files (.txt) ↔ AutoCast Main System
                    ↓
              Content Directories
                    ↓
                Winamp Player
```

### File Structure
```
AutoCast_Demo/
├── schedule_manager_gui.py     # Main interface
├── mondayschedule.txt          # Monday schedule
├── tuesdayschedule.txt         # Tuesday schedule
├── wednesdayschedule.txt       # Wednesday schedule
├── thursdayschedule.txt        # Thursday schedule
├── fridayschedule.txt          # Friday schedule
├── saturdayschedule.txt        # Saturday schedule
├── sundayschedule.txt          # Sunday schedule
└── content/                    # Media content folders
    ├── MUSIC/
    ├── JINGLES/
    ├── ADS/
    └── [other content types]/
```

---

## Getting Started

### System Requirements
- **Operating System**: Windows 10/11
- **Python**: 3.8 or higher
- **Memory**: 4GB RAM minimum (8GB recommended)
- **Storage**: 2GB free space for schedules and logs
- **Display**: 1200x700 minimum resolution

### Launching the Schedule Manager

#### Method 1: Batch File (Recommended)
```batch
# Double-click: setup_and_start_schedule_manager.bat
```

#### Method 2: Command Line
```powershell
cd "D:\MyFMStation\AutoCast_Demo"
python schedule_manager_gui.py
```

#### Method 3: Direct Python Execution
```powershell
python -m schedule_manager_gui
```

### Initial Setup Verification
When the Schedule Manager opens, verify:
1. ✅ All 7 day tabs are visible
2. ✅ Content folders are accessible
3. ✅ No error messages in status bar
4. ✅ Professional interface theme loads correctly

---

## Schedule Management Interface

### Main Window Layout

#### 1. Menu Bar
- **File Menu**: New, Save, Save All, Export, Exit
- **Edit Menu**: Copy Day, Paste Day, Clear Day
- **Tools Menu**: Validate Schedules, Generate Reports
- **Help Menu**: User Guide, About

#### 2. Professional Toolbar
```
📁 File Section    | ✏️ Edit Section     | 🔧 Tools Section
- 📄 New          | - 📋 Copy          | - ✅ Validate
- 💾 Save         | - 📄 Paste         | - 🔐 Encrypt
- 💾 Save All     | - 🗑️ Clear         |
```

#### 3. Day Tabs
Each day has its own dedicated tab with professional icons:
- 📅 Monday
- 💼 Tuesday  
- 🎯 Wednesday
- ⚡ Thursday
- 🎉 Friday
- 🌅 Saturday
- 🌟 Sunday

#### 4. Two-Panel Layout

**Left Panel (70% width) - Schedule View**
- Professional treeview with columns:
  - 🕐 Time
  - 🎵 Content Actions
  - 📂 Type
  - ✅ Status

**Right Panel (30% width) - Schedule Editor**
- Time Input Card
- Content Actions Card
- Current Actions List
- Time Slot Management
- Batch Operations

#### 5. Status Bar
- Main status messages
- Unsaved changes indicator
- Completion counter (X/7 Days)
- Save status indicator

---

## Creating Broadcast Schedules

### Understanding Schedule Structure

Each schedule entry consists of:
```
TIME=ACTION1=PATH1=ACTION2=PATH2=...
```

Example:
```
06:00=TIME_CHECK=TIME CHECK=JINGLE=JINGLES=MUSIC=MUSIC
```

### Step-by-Step Schedule Creation

#### Step 1: Select Day Tab
Click on the desired day tab (Monday through Sunday)

#### Step 2: Set Time Slot
1. **Hour Selection**: Use spinbox (00-23)
2. **Minute Selection**: Use spinbox (00-59)
3. **Format**: Always 24-hour format (e.g., 14:30 for 2:30 PM)

#### Step 3: Add Content Actions

**Quick Add Method:**
Use preset buttons for common actions:
- ⏰ **Time Check**: Automated time announcement
- 🎵 **Jingle**: Station identification music
- 📢 **Ads**: Commercial advertisements
- 🎶 **Music**: Primary music content

**Manual Method:**
1. Select action type from dropdown (30+ options)
2. Specify content path
3. Click "➕ Add to Queue"

#### Step 4: Build Action Sequence
Continue adding actions to create your broadcast sequence:
```
Example sequence:
1. TIME_CHECK (time announcement)
2. JINGLE (station ID)
3. MUSIC (main content)
4. ADS (commercials)
```

#### Step 5: Finalize Time Slot
Click "➕ ADD SLOT" to save the complete time slot

### Content Action Types

#### Core Broadcasting Actions
- **TIME_CHECK**: Automated time announcements
- **JINGLE**: Station identification and branding
- **ADS**: Commercial advertisement blocks
- **MUSIC**: Primary music programming

#### Music Categories
- **BHAJANS**: Devotional music
- **OLD LOK GEET**: Traditional folk songs
- **OLD SAD NEPALI SONGS**: Classic emotional tracks
- **NEW NEPALI SONGS**: Contemporary Nepali music
- **HINDI SONGS**: Bollywood and Hindi music
- **ENGLISH SONGS**: International English tracks
- **CLASSICAL MUSIC**: Classical compositions
- **FOLK SONGS**: Regional folk music
- **DEVOTIONAL**: Religious/spiritual content

#### News & Information
- **NEWS**: News bulletins
- **WEATHER**: Weather reports
- **SPORTS UPDATE**: Sports news and scores
- **TRAFFIC UPDATE**: Traffic conditions

#### Talk Programming
- **TALK SHOW**: Hosted discussion programs
- **INTERVIEW**: Guest interviews
- **LIVE PROGRAM**: Live broadcasting
- **PHONE-IN**: Listener call-in shows

#### Station Operations
- **ANNOUNCEMENT**: General announcements
- **STATION ID**: Station identification
- **PROMO**: Program promotions
- **PSA**: Public service announcements
- **BIRTHDAY WISHES**: Listener birthday messages
- **DEDICATION**: Song dedications

#### Specialized Content
- **COMEDY**: Comedy shows/segments
- **DRAMA**: Radio dramas
- **DOCUMENTARY**: Documentary programs
- **PODCAST**: Podcast content
- **SPECIAL EVENT**: Special event coverage
- **NATIONAL ANTHEM**: National anthem
- **EMERGENCY BROADCAST**: Emergency information
- **TEST TONE**: Technical test signals
- **SILENCE**: Silent periods

---

## Content Management

### Content Path Structure

#### Primary Path (AutoCast)
```
D:\MyFMStation\AutoCast\[CONTENT_TYPE]\
```

#### Fallback Path (Legacy Automation)
```
D:\MyFMStation\Automation\Automation\[CONTENT_TYPE]\
```

### Content Folder Organization

Create folders matching your action types:
```
content/
├── MUSIC/
│   ├── song1.mp3
│   ├── song2.wav
│   └── song3.flac
├── JINGLES/
│   ├── station_id.mp3
│   └── morning_jingle.wav
├── ADS/
│   ├── commercial1.mp3
│   └── sponsor_ad.wav
├── NEWS/
│   ├── morning_news.mp3
│   └── evening_bulletin.wav
└── [other content types]/
```

### Supported Audio Formats
- **MP3**: Standard compressed format
- **WAV**: Uncompressed high quality
- **FLAC**: Lossless compression
- **WMA**: Windows Media Audio
- **AAC**: Advanced Audio Coding
- **OGG**: Open source format

### Content Path Rules
1. **Absolute paths** are supported
2. **Relative paths** from AutoCast directory
3. **Special paths**: "TIME CHECK", "SILENCE"
4. **Maximum 30 files** per music slot (randomized)

### Browse for Content
1. Click 📁 browse button next to path field
2. Navigate to your content folder
3. Select folder containing audio files
4. Path will auto-populate

---

## Advanced Features

### Time Slot Management

#### Editing Existing Slots
1. **Select slot** in schedule view (left panel)
2. **Double-click** or click "📝 EDIT"
3. **Modify** time and actions in editor
4. **Click "💾 UPDATE"** to save changes

#### Slot Operations
- **➕ ADD SLOT**: Create new time slot
- **📝 EDIT**: Load slot into editor
- **💾 UPDATE**: Save changes to existing slot  
- **🗑️ DELETE**: Remove time slot

### Batch Operations

#### Copy Operations
- **📋 Copy All**: Copy entire day schedule
- **📄 Paste**: Paste to current day
- **🧹 Clear All**: Remove all slots from day

#### Validation & Reports
- **✅ Validate**: Check schedule integrity
- **📊 Report**: Generate detailed analysis

### Professional Features

#### Schedule Validation
Automatic checks for:
- Time format correctness
- Path accessibility
- Content availability
- Logical sequence
- Overlap detection

#### Auto-Save Protection
- Tracks unsaved changes
- Prevents data loss
- Visual indicators for modified schedules

#### Professional Reporting
Generates comprehensive reports including:
- Total broadcast time
- Content type distribution
- Schedule completeness
- Path validation status
- Recommendations

---

## File Management

### Schedule File Format

Each day's schedule is saved as a text file:
```
# Monday Schedule File (mondayschedule.txt)
06:00=TIME_CHECK=TIME CHECK=JINGLE=JINGLES=MUSIC=MUSIC
07:00=NEWS=NEWS=WEATHER=WEATHER=MUSIC=MUSIC
08:00=TALK SHOW=TALK SHOWS=PHONE-IN=PHONE-IN
```

### Save Operations

#### Save Current Day
- **Keyboard**: Ctrl+S
- **Toolbar**: 💾 Save
- **Menu**: File → Save

#### Save All Days
- **Keyboard**: Ctrl+Shift+S
- **Toolbar**: 💾 Save All
- **Menu**: File → Save All

### File Locations
All schedule files are saved in the main AutoCast directory:
```
D:\MyFMStation\AutoCast_Demo\
├── mondayschedule.txt
├── tuesdayschedule.txt
├── wednesdayschedule.txt
├── thursdayschedule.txt
├── fridayschedule.txt
├── saturdayschedule.txt
└── sundayschedule.txt
```

### Backup & Recovery

#### Manual Backup
1. Copy all schedule files to safe location
2. Include content folders if modified
3. Store with date/version information

#### Recovery Process
1. Replace corrupted files with backups
2. Restart Schedule Manager
3. Verify schedule loading
4. Re-validate all schedules

---

## Troubleshooting

### Common Issues & Solutions

#### Interface Problems

**Problem**: Schedule Manager won't start
```
Solution:
1. Check Python installation (3.8+)
2. Verify all required files exist
3. Run from command line to see errors
4. Check Windows permissions
```

**Problem**: Tabs not displaying correctly
```
Solution:
1. Maximize window (Windows key + Up)
2. Check screen resolution (1200x700 minimum)
3. Reset window position
4. Restart application
```

#### Schedule Management Issues

**Problem**: Can't add time slots
```
Solution:
1. Verify time format (00:00 to 23:59)
2. Ensure actions list is not empty
3. Check for duplicate time slots
4. Validate content paths
```

**Problem**: Content paths not working
```
Solution:
1. Use absolute paths: D:\MyFMStation\AutoCast\MUSIC\
2. Check folder permissions
3. Verify audio files exist
4. Use supported file formats
```

#### Save/Load Problems

**Problem**: Schedules not saving
```
Solution:
1. Check write permissions
2. Ensure disk space available
3. Close other applications using files
4. Run as administrator if needed
```

**Problem**: Existing schedules not loading
```
Solution:
1. Check file format and syntax
2. Verify file paths are correct
3. Remove invalid characters
4. Recreate corrupted schedules
```

### Error Messages

#### Common Error Codes
- **"No actions to add"**: Add content actions before creating slot
- **"Invalid time format"**: Use HH:MM format (00:00-23:59)
- **"Path not found"**: Verify content folder exists
- **"Time slot exists"**: Choose different time or edit existing
- **"No slot selected"**: Select time slot before editing/deleting

### Performance Optimization

#### For Large Schedules
1. **Limit music folders** to reasonable sizes
2. **Use SSD storage** for better performance
3. **Close unused applications**
4. **Regular system maintenance**

#### For Slow Loading
1. **Check content path accessibility**
2. **Reduce network path usage**
3. **Optimize audio file sizes**
4. **Clear temporary files**

---

## Best Practices

### Schedule Planning

#### Daily Schedule Structure
```
Recommended pattern:
06:00 - Time Check + Station ID + Music
07:00 - News + Weather + Music
08:00 - Talk Show / Interview
12:00 - Time Check + Ads + Music
18:00 - News + Sports + Music
22:00 - Mellow Music + Station ID
```

#### Content Distribution
- **60%** Music content
- **20%** Talk/Information
- **15%** Advertising
- **5%** Station operations

### Professional Broadcasting

#### Time Slot Guidelines
1. **Every hour**: Time check and station ID
2. **News slots**: Consistent timing (7AM, 1PM, 7PM)
3. **Commercial breaks**: Natural program transitions
4. **Dead air prevention**: Always have content queued

#### Content Management
1. **Regular updates**: Fresh music rotation
2. **Quality control**: Audio level consistency
3. **Backup content**: Alternative files ready
4. **Legal compliance**: Licensed content only

### System Maintenance

#### Daily Tasks
- ☑️ Verify next day's schedule loaded
- ☑️ Check content accessibility
- ☑️ Review error logs
- ☑️ Test critical time slots

#### Weekly Tasks
- ☑️ Full schedule validation
- ☑️ Content folder cleanup
- ☑️ Performance review
- ☑️ Backup schedule files

#### Monthly Tasks
- ☑️ System optimization
- ☑️ Content library update
- ☑️ Hardware health check
- ☑️ Staff training review

---

## Support Information

### Technical Support

**Eastlink Cloud Pvt. Ltd.**
- **Email**: support@eastlinkcloud.com
- **Phone**: +977-XX-XXXXXX
- **Website**: www.eastlinkcloud.com
- **Support Hours**: 24/7 Professional Support


### Documentation & Resources

#### Online Resources
- User manuals and guides
- Video tutorials
- FAQ database
- Community forums

#### Training & Certification
- **Basic Operations**: 2-day course
- **Advanced Management**: 3-day intensive
- **System Administration**: 5-day certification
- **Custom Training**: On-site available

### Warranty & Maintenance

#### Software Support
- **Trial Version**: online support
- **Licensed Version**: 1 year comprehensive support
- **Extended Support**: Annual renewal available
- **Custom Development**: Professional services

#### Service Levels
- **Standard**: Business hours support
- **Professional**: Priority support with SLA
- **Enterprise**: 24/7 dedicated support
- **Managed Service**: Full system management

---

## Appendices

### Appendix A: Keyboard Shortcuts

| Function | Shortcut |
|----------|----------|
| Save Current | Ctrl+S |
| Save All | Ctrl+Shift+S |
| New Schedule | Ctrl+N |
| Copy Day | Ctrl+C |
| Paste Day | Ctrl+V |
| Help | F1 |
| Validate | Ctrl+R |
| Exit | Ctrl+Q |

### Appendix B: Content Type Reference

| Action Type | Default Path | Description |
|-------------|--------------|-------------|
| TIME_CHECK | TIME CHECK | Automated time announcement |
| JINGLE | JINGLES | Station identification music |
| ADS | ADS | Commercial advertisements |
| MUSIC | MUSIC | Primary music programming |
| NEWS | NEWS | News bulletins and updates |
| WEATHER | WEATHER | Weather reports |
| TALK SHOW | TALK SHOWS | Hosted discussion programs |

### Appendix C: File Format Specifications

#### Schedule File Syntax
```
HH:MM=ACTION1=PATH1=ACTION2=PATH2=ACTION3=PATH3
```

#### Time Format Rules
- 24-hour format only
- Leading zeros required (06:00, not 6:00)
- Minute increments supported
- No seconds specification

---

**Document Version**: 2.0  
**Last Updated**: September 2025  
**Created by**: Eastlink Cloud Pvt. Ltd.  
**Classification**: Professional Broadcasting System Manual  

---

© 2025 Eastlink Cloud Pvt. Ltd. All rights reserved. This manual is proprietary and confidential. Unauthorized reproduction or distribution is prohibited.