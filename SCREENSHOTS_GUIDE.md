# Terminal Usage Screenshots Guide

## Overview
This document provides guidance on capturing and documenting terminal screenshots for the Linux tutorial. Since actual screenshots cannot be embedded in this text repository, this guide describes what screenshots should be taken and how to capture them.

---

## How to Take Screenshots

### Windows (WSL/Terminal)
- **Full Screen**: `Windows Key + PrtScn` (saves to Pictures/Screenshots)
- **Snipping Tool**: `Windows Key + Shift + S` (select area)
- **Alt + PrtScn**: Capture active window only

### Linux (Native)
- **Full Screen**: `PrtScn` or `Print Screen`
- **Selection**: `Shift + PrtScn`
- **Screenshot Tool**: Use `gnome-screenshot` or `flameshot`

### macOS (Terminal)
- **Full Screen**: `Cmd + Shift + 3`
- **Selection**: `Cmd + Shift + 4`
- **Window**: `Cmd + Shift + 4`, then `Space`

---

## Required Screenshots

### 1. Installation and Setup

#### Screenshot 1.1: WSL Installation
**Command**: `wsl --install -d Ubuntu-22.04`
**What to capture**:
- PowerShell window showing installation progress
- Success message
**Filename**: `01_wsl_installation.png`

#### Screenshot 1.2: First Login
**What to capture**:
- Ubuntu terminal window
- Username creation prompt
- Welcome message
**Filename**: `02_first_login.png`

#### Screenshot 1.3: System Information
**Commands**:
```bash
whoami
pwd
uname -a
```
**What to capture**:
- Terminal showing all three commands and outputs
**Filename**: `03_system_info.png`

---

### 2. Directory Navigation

#### Screenshot 2.1: Home Directory Listing
**Commands**:
```bash
pwd
ls -la
```
**What to capture**:
- Current directory path
- Detailed file listing with permissions
- Hidden files visible (.bashrc, .profile, etc.)
**Filename**: `04_home_directory.png`

#### Screenshot 2.2: Root Directory Structure
**Commands**:
```bash
cd /
ls -l
```
**What to capture**:
- Root directory contents
- System folders (bin, etc, home, usr, var)
**Filename**: `05_root_directory.png`

#### Screenshot 2.3: Directory Tree
**Commands**:
```bash
tree projects
```
**What to capture**:
- Visual tree structure of nested directories
**Filename**: `06_directory_tree.png`

---

### 3. File and Directory Creation

#### Screenshot 3.1: Creating Directories
**Commands**:
```bash
mkdir practice_folder
mkdir -p projects/web/frontend/src
ls -l
```
**What to capture**:
- Commands executed
- Directory creation confirmation
- Directory listing showing new folders
**Filename**: `07_creating_directories.png`

#### Screenshot 3.2: Creating Files
**Commands**:
```bash
touch file1.txt file2.txt file3.txt
ls -lh
```
**What to capture**:
- Multiple files created with touch
- Detailed listing showing file permissions and timestamps
**Filename**: `08_creating_files.png`

#### Screenshot 3.3: File Content Creation
**Commands**:
```bash
echo "Hello Linux" > greeting.txt
cat greeting.txt
```
**What to capture**:
- Echo command creating file
- Cat displaying content
**Filename**: `09_file_content.png`

#### Screenshot 3.4: Removing Files
**Commands**:
```bash
rm -i file1.txt
ls
```
**What to capture**:
- Interactive removal prompt
- User's response (y/n)
- Updated file listing
**Filename**: `10_removing_files.png`

---

### 4. File Viewing and Editing

#### Screenshot 4.1: Viewing with Cat
**Commands**:
```bash
cat sample.txt
cat -n sample.txt
```
**What to capture**:
- File contents displayed
- Line-numbered output
**Filename**: `11_cat_command.png`

#### Screenshot 4.2: Head and Tail
**Commands**:
```bash
head -5 sample.txt
tail -3 sample.txt
```
**What to capture**:
- First 5 lines
- Last 3 lines
**Filename**: `12_head_tail.png`

#### Screenshot 4.3: Nano Editor
**What to capture**:
- Nano interface with text
- Bottom menu showing shortcuts (^O, ^X, etc.)
**Filename**: `13_nano_editor.png`

#### Screenshot 4.4: Vim Editor
**What to capture**:
- Vim interface in insert mode
- Text being edited
- Mode indicator at bottom
**Filename**: `14_vim_editor.png`

#### Screenshot 4.5: Grep Search
**Commands**:
```bash
grep "Linux" sample.txt
grep -n "practice" sample.txt
```
**What to capture**:
- Search results highlighted
- Line numbers with -n option
**Filename**: `15_grep_search.png`

---

### 5. File Permissions

#### Screenshot 5.1: Viewing Permissions
**Commands**:
```bash
ls -l
```
**What to capture**:
- Long listing showing permission strings
- Owner and group information
- File sizes and dates
**Filename**: `16_file_permissions.png`

#### Screenshot 5.2: Permission Denied Error
**Commands**:
```bash
./script.sh
```
**What to capture**:
- "Permission denied" error message
**Filename**: `17_permission_denied.png`

#### Screenshot 5.3: Adding Execute Permission
**Commands**:
```bash
chmod u+x script.sh
ls -l script.sh
./script.sh
```
**What to capture**:
- Permission change command
- Updated permissions (-rwxr--r--)
- Script executing successfully
**Filename**: `18_chmod_execute.png`

#### Screenshot 5.4: Numeric Permissions
**Commands**:
```bash
chmod 755 script.sh
chmod 644 document.txt
ls -l
```
**What to capture**:
- Both chmod commands
- Different permission patterns (755 vs 644)
**Filename**: `19_numeric_permissions.png`

#### Screenshot 5.5: Changing Ownership
**Commands**:
```bash
ls -l testfile.txt
sudo chown root:root testfile.txt
ls -l testfile.txt
```
**What to capture**:
- Original ownership (user:user)
- Chown command with sudo
- New ownership (root:root)
**Filename**: `20_chown_command.png`

---

### 6. System Monitoring

#### Screenshot 6.1: System Uptime
**Commands**:
```bash
uptime
uptime -p
```
**What to capture**:
- Current time
- Uptime duration
- Load averages
**Filename**: `21_uptime.png`

#### Screenshot 6.2: Disk Usage
**Commands**:
```bash
df -h
```
**What to capture**:
- Filesystem names
- Sizes, used, available space
- Usage percentages
- Mount points
**Filename**: `22_disk_usage.png`

#### Screenshot 6.3: Memory Usage
**Commands**:
```bash
free -h
```
**What to capture**:
- Total, used, free memory
- Buffer/cache information
- Swap usage
- Available memory
**Filename**: `23_memory_usage.png`

#### Screenshot 6.4: Top Command
**Command**: `top`
**What to capture**:
- Header with load average
- CPU and memory statistics
- Process list with PID, USER, %CPU, %MEM
- Top 10 processes visible
**Filename**: `24_top_command.png`

#### Screenshot 6.5: Htop Command
**Command**: `htop`
**What to capture**:
- Color-coded CPU bars
- Memory and swap bars
- Process tree view
- Function key menu at bottom
**Filename**: `25_htop_command.png`

#### Screenshot 6.6: Process Listing
**Commands**:
```bash
ps aux | head -10
```
**What to capture**:
- Process list with details
- Columns: USER, PID, %CPU, %MEM, COMMAND
**Filename**: `26_ps_command.png`

#### Screenshot 6.7: CPU Information
**Commands**:
```bash
lscpu
```
**What to capture**:
- Architecture (x86_64)
- CPU cores and threads
- Model name
- CPU frequencies
**Filename**: `27_cpu_info.png`

#### Screenshot 6.8: System Information
**Commands**:
```bash
uname -a
lsb_release -a
```
**What to capture**:
- Kernel version
- Distribution information
- Ubuntu version
**Filename**: `28_system_info.png`

---

## Screenshot Organization

### Recommended Folder Structure
```
screenshots/
├── 01_installation/
│   ├── 01_wsl_installation.png
│   ├── 02_first_login.png
│   └── 03_system_info.png
├── 02_navigation/
│   ├── 04_home_directory.png
│   ├── 05_root_directory.png
│   └── 06_directory_tree.png
├── 03_file_operations/
│   ├── 07_creating_directories.png
│   ├── 08_creating_files.png
│   ├── 09_file_content.png
│   └── 10_removing_files.png
├── 04_viewing_editing/
│   ├── 11_cat_command.png
│   ├── 12_head_tail.png
│   ├── 13_nano_editor.png
│   ├── 14_vim_editor.png
│   └── 15_grep_search.png
├── 05_permissions/
│   ├── 16_file_permissions.png
│   ├── 17_permission_denied.png
│   ├── 18_chmod_execute.png
│   ├── 19_numeric_permissions.png
│   └── 20_chown_command.png
└── 06_monitoring/
    ├── 21_uptime.png
    ├── 22_disk_usage.png
    ├── 23_memory_usage.png
    ├── 24_top_command.png
    ├── 25_htop_command.png
    ├── 26_ps_command.png
    ├── 27_cpu_info.png
    └── 28_system_info.png
```

---

## Screenshot Best Practices

### 1. Terminal Settings for Clear Screenshots
- **Font Size**: Use 12-14pt for readability
- **Color Scheme**: Use high contrast (dark background, light text)
- **Window Size**: Make terminal window large enough to show full outputs
- **Zoom**: If needed, zoom to 125% or 150%

### 2. Content Guidelines
- **Clear Commands**: Ensure commands are fully visible
- **Complete Output**: Capture entire output, not truncated
- **Prompt Visible**: Include command prompt (user@hostname:~$)
- **No Personal Info**: Avoid showing sensitive data

### 3. Image Quality
- **Format**: PNG for crisp text (not JPG)
- **Resolution**: At least 1920x1080 or higher
- **File Size**: Optimize but keep readable (compress if > 2MB)

### 4. Annotation (Optional)
Use tools like:
- **Windows**: Paint, Snagit, ShareX
- **Linux**: GIMP, Shutter, Flameshot
- **Mac**: Preview, Skitch

Annotations can highlight:
- Important command parts with arrows
- Output sections with boxes
- Error messages with circles

---

## Creating a Screenshots Archive for GitHub

### Option 1: Direct Upload to Repository
1. Create `screenshots/` directory in your repo
2. Upload all PNG files
3. Reference in README.md:
```markdown
![WSL Installation](screenshots/01_installation/01_wsl_installation.png)
```

### Option 2: Use GitHub Issues
1. Create an issue titled "Terminal Screenshots"
2. Drag and drop images into issue comment
3. Copy generated URLs
4. Use in README

### Option 3: Use External Image Host
- **Imgur**: Free, anonymous
- **GitHub Wiki**: Create wiki with images
- **Google Drive**: Share public links

---

## Markdown Example for README

```markdown
## Tutorial Screenshots

### Installation
![WSL Installation](screenshots/01_installation/01_wsl_installation.png)
*Installing WSL with Ubuntu 22.04*

### Directory Navigation
![Home Directory](screenshots/02_navigation/04_home_directory.png)
*Listing home directory with hidden files*

### File Permissions
![Chmod Command](screenshots/05_permissions/18_chmod_execute.png)
*Making script executable with chmod*

### System Monitoring
![Htop Command](screenshots/06_monitoring/25_htop_command.png)
*Interactive process viewer with htop*
```

---

## Video Alternative

Instead of static screenshots, consider recording:
- **Windows**: Xbox Game Bar (Windows+G), OBS Studio
- **Linux**: SimpleScreenRecorder, Kazam, OBS Studio
- **Mac**: QuickTime, ScreenFlow

Upload to YouTube and link in README:
```markdown
[Watch Full Tutorial Video](https://youtube.com/...)
```

---

## Checklist

Use this checklist when capturing screenshots:

- [ ] All 28 required screenshots captured
- [ ] Files named according to convention
- [ ] Organized in folder structure
- [ ] Image quality verified (clear, readable)
- [ ] No sensitive information visible
- [ ] File sizes reasonable (<2MB each)
- [ ] Screenshots uploaded to repository
- [ ] README updated with image references
- [ ] Images display correctly on GitHub

---

## Additional Resources

### Screenshot Tools
- **ShareX** (Windows): https://getsharex.com/
- **Flameshot** (Linux): https://flameshot.org/
- **Spectacle** (Mac): Built-in

### Image Optimization
- **TinyPNG**: https://tinypng.com/
- **ImageOptim**: https://imageoptim.com/
- **Squoosh**: https://squoosh.app/

### Video Recording
- **OBS Studio**: https://obsproject.com/
- **Asciinema**: https://asciinema.org/ (terminal recorder)

---

## Notes

Since this is a text-based repository, actual screenshot files should be:
1. Captured during your practice sessions
2. Saved with appropriate filenames
3. Uploaded to a `screenshots/` folder in the repository
4. Referenced in the main README.md file

If you need to demonstrate terminal sessions without screenshots, consider using:
- **Asciinema**: Records terminal sessions as text (can be replayed)
- **Carbon**: Creates beautiful code screenshots (carbon.now.sh)
- **Code snippets**: In README with proper formatting

---

**Last Updated**: January 31, 2026
**Version**: 1.0
