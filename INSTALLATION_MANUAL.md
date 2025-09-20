# AutoCast FM - Installation Manual

## 📋 System Overview
AutoCast FM is a professional radio automation system developed by **Eastlink Cloud Pvt. Ltd.** for complete broadcasting solutions.

**Company**: Eastlink Cloud Pvt. Ltd.  
**Address**: Tripureshwor, Kathmandu, Nepal  
**Website**: eastlink.net.np  
**Support**: 9801901140 | Business: 9851079362 | 9851191235 | 9801901141

---

## 🖥️ System Requirements

### Minimum Requirements
- **Operating System**: Windows 10 (64-bit) or Windows 11
- **Processor**: Intel Core i3 or AMD equivalent (2.0 GHz)
- **Memory**: 4 GB RAM
- **Storage**: 2 GB free disk space
- **Audio**: Built-in audio or dedicated sound card
- **Network**: Internet connection (for license activation)

### Recommended Requirements
- **Operating System**: Windows 11 (64-bit)
- **Processor**: Intel Core i5 or AMD equivalent (3.0 GHz)
- **Memory**: 8 GB RAM or higher
- **Storage**: SSD with 10 GB free space
- **Audio**: Professional audio interface
- **Network**: Stable broadband connection

---

## 📥 Installation Steps

### Step 1: Download Required Software

#### 1.1 Python Installation
1. Download Python 3.8 or later from: https://python.org/downloads/
2. **IMPORTANT**: Check "Add Python to PATH" during installation
3. Choose "Custom Installation" and select:
   - ✅ pip (package installer)
   - ✅ Add to PATH
   - ✅ Install for all users

#### 1.2 Winamp Installation
1. Download Winamp from: https://winamp.com/
2. Install to default location: `C:\Program Files (x86)\Winamp\`
3. Complete the setup wizard
4. Test Winamp by playing an audio file

### Step 2: AutoCast FM Installation

#### 2.1 Extract Files
1. Extract AutoCast FM files to: `D:\MyFMStation\AutoCast_Demo\`
2. Ensure all files are extracted properly
3. Verify the following core files exist:
   - `Auto.py` (Main program)
   - `fmcore.py` (License system)
   - `trial_license.py` (Trial generator)
   - `license_info.py` (Hardware detection)

#### 2.2 Install Python Dependencies
1. Open Command Prompt as Administrator
2. Navigate to AutoCast directory:
   ```bash
   cd "D:\MyFMStation\AutoCast_Demo"
   ```
3. Install required packages:
   ```bash
   pip install mutagen
   ```

### Step 3: Hardware Information & Licensing

#### 3.1 Generate Hardware Information
1. Run hardware detection:
   ```bash
   python license_info.py
   ```
2. This creates `license_info.txt` with your system details
3. **Keep this file safe** - needed for all license operations

#### 3.2 Generate Trial License (Recommended for First-Time Users)
1. Generate 15-day FREE trial:
   ```bash
   python trial_license.py
   ```
2. Or use the batch file (Windows):
   ```bash
   generate_trial.bat
   ```
3. This creates `.fmconfig.dat` license file

### Step 4: Content Setup

#### 4.1 Create Content Directories
Create the following folders in your AutoCast directory:
```
content/
├── MUSIC/          # Your music files
├── ADS/            # Advertisement files
├── JINGLES/        # Station jingles
├── TIME_CHECKS/    # Time announcement files
└── BBC/            # News or external feeds (optional)
```

#### 4.2 Add Audio Content
1. **Music Files**: Add MP3, WAV, OGG files to `content/MUSIC/`
2. **Advertisements**: Add ad files to `content/ADS/`
3. **Jingles**: Add station jingles to `content/JINGLES/`
4. **Supported Formats**: `.mp3`, `.wav`, `.ogg`, `.mpeg`, `.m3u8`, `.mp4`, `.m3u`, `.pls`

### Step 5: Schedule Configuration

#### 5.1 Daily Schedule Files
The system uses daily schedule files:
- `mondayschedule.txt`
- `tuesdayschedule.txt`
- `wednesdayschedule.txt`
- `thursdayschedule.txt`
- `fridayschedule.txt`
- `saturdayschedule.txt`
- `sundayschedule.txt`

#### 5.2 Schedule Format
Each line follows this format:
```
HH:MM=ACTION=FOLDER=ACTION=FOLDER...
```

Example:
```
06:00=TIME_CHECK=time_checks=JINGLE=jingles=MUSIC=music
09:00=JINGLE=jingles=ADS=ads=MUSIC=music
12:00=TIME_CHECK=time_checks=ADS=ads=JINGLE=jingles=MUSIC=music
```

#### 5.3 Available Actions
- **TIME_CHECK**: Time announcements
- **JINGLE**: Station identification
- **ADS**: Advertisement blocks
- **MUSIC**: Music playback
- **JINGLE_2**: Secondary jingles

---

## 🚀 First Launch

### Step 1: Start AutoCast FM
1. **Method 1 - Batch File** (Recommended):
   ```bash
   start_automation.bat
   ```


### Step 2: Verify Operation
The system should display:
```
===========================================================================
                    AutoCast Broadcasting System Pro
                 Developed by: Eastlink Cloud Pvt. Ltd.
                Address: Tripureshwor, Kathmandu, Nepal
                        Website: eastlink.net.np
===========================================================================
```

### Step 3: Monitor Status
- Current time and date
- Currently playing track
- Next scheduled program
- System status information

---

## 🔧 Configuration Options

### Winamp Path Configuration
If Winamp is installed in a different location, edit `Auto.py`:
```python
winamp_path = r"C:\Your\Custom\Path\winamp.exe"
```

### Log File Location
Logs are automatically created in:
- `logs/autocast.log` - Activity logs
- `logs/error.log` - Error logs

### Content Path Configuration
Content paths are relative to the AutoCast directory:
- Default: `content/MUSIC/`
- Custom paths can be specified in schedule files

---

## 🛠️ Troubleshooting

### Common Issues

#### Issue 1: "License file not found"
**Solution**:
1. Run: `python license_info.py`
2. Restart AutoCast FM

#### Issue 2: "Winamp not found"
**Solution**:
1. Install Winamp to: `C:\Program Files (x86)\Winamp\`
2. Or update path in `Auto.py`

#### Issue 3: "No schedule found"
**Solution**:
1. Create schedule files for each day
2. Use proper format: `HH:MM=ACTION=FOLDER`
3. Ensure schedule files are in main directory

#### Issue 4: "Python not recognized"
**Solution**:
1. Reinstall Python with "Add to PATH" checked
2. Restart Command Prompt
3. Test with: `python --version`

#### Issue 5: "ModuleNotFoundError: mutagen"
**Solution**:
```bash
pip install mutagen
```

#### Issue 6: "Hardware mismatch"
**Solution**:
1. Run: `python license_info.py`
2. Generate new license: `python trial_license.py`

### Performance Optimization

#### For Better Performance:
1. **Use SSD storage** for faster file access
2. **Close unnecessary programs** while running
3. **Use professional audio interface** for better sound
4. **Regular system maintenance** and disk cleanup

#### Memory Usage:
- Normal operation: 50-100 MB RAM
- With large playlists: 200-500 MB RAM
- Monitor via Task Manager if needed

---

## 📞 Support & Licensing

### Technical Support
- **Support Hotline**: 9801901140
- **Business Inquiries**: 9851079362 | 9851191235 | 9801901141
- **Company**: Eastlink Cloud Pvt. Ltd.
- **Website**: eastlink.net.np

### License Options After Trial
1. **Monthly License**: 30 days validity
2. **Quarterly License**: 90 days validity
3. **Half-Yearly License**: 180 days validity
4. **Annual License**: 365 days validity
5. **Multi-Year License**: 730 days validity

---

## 📚 Quick Reference

### Essential Commands
```bash
# Generate hardware info
python license_info.py

# Generate trial license
python trial_license.py

# Start AutoCast FM
python Auto.py
# OR
start_automation.bat

# Check license status
python trial_license.py --status

# Generate full license
python generate_license.py
```

### Important Files
- `Auto.py` - Main program
- `fmcore.py` - License system
- `.fmconfig.dat` - License file (created automatically)
- `license_info.txt` - Hardware info (created automatically)
- `[day]schedule.txt` - Daily schedules (create manually)

### Directory Structure
```
AutoCast_Demo/
├── Auto.py                 # Main program
├── fmcore.py              # License system
├── trial_license.py       # Trial generator
├── license_info.py        # Hardware detection
├── .fmconfig.dat          # License file (auto-created)
├── license_info.txt       # Hardware info (auto-created)
├── mondayschedule.txt     # Monday schedule
├── tuesdayschedule.txt    # Tuesday schedule
├── ... (other day schedules)
├── logs/                  # Log files (auto-created)
├── content/               # Media content
│   ├── MUSIC/
│   ├── ADS/
│   ├── JINGLES/
│   └── TIME_CHECKS/
└── *.bat                  # Batch files for easy operation
```

---

## ✅ Installation Checklist

- [ ] Windows 10/11 installed
- [ ] Python 3.8+ installed with PATH
- [ ] Winamp installed and tested
- [ ] AutoCast files extracted to `D:\MyFMStation\AutoCast_Demo\`
- [ ] Python dependencies installed (`pip install mutagen`)
- [ ] Hardware info generated (`python license_info.py`)
- [ ] Trial license generated (`python trial_license.py`)
- [ ] Content folders created and populated
- [ ] At least one daily schedule file created
- [ ] System tested with `python Auto.py`
- [ ] Winamp integration verified
- [ ] Audio output confirmed

---

**© 2025 Eastlink Cloud Pvt. Ltd.**  
**Professional Radio Automation Solutions**  
**Tripureshwor, Kathmandu, Nepal**  
**Website**: eastlink.net.np

For technical support and business inquiries:  
📞 **Support**: 9801901140  
💼 **Business**: 9851079362 | 9851191235 | 9801901141