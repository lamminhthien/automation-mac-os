# macOS Automation Scripts

A collection of shell aliases and automation scripts to enhance productivity on macOS. These utilities provide quick shortcuts for common development and system tasks.

## Overview

This repository contains three main automation tools designed to streamline your workflow on macOS:

1. **auto_optimize** - System and cache cleanup utilities
2. **automation_finder** - Quick access to common directories
3. **chrome_auto** - Browser shortcuts for frequently visited sites

## Installation

### Setup

1. Clone this repository or copy the script files
2. Add the content of the desired script to your shell configuration file:
   - For **Bash**: `~/.bashrc`
   - For **Zsh**: `~/.zshrc`

3. Reload your shell configuration:
   ```bash
   source ~/.zshrc
   # or
   source ~/.bashrc
   ```

## Scripts

### 1. auto_optimize

Optimizes system performance by clearing caches and temporary files from development tools and applications.

**Available Commands:**

- `clean` - Comprehensive cleanup command that removes:
  - Yarn and npm caches
  - System npm cache
  - Local npm and yarn directories
  - macOS system caches
  - Application Support caches
  - Logs

- `clean_dev()` - Development tool cleanup function that clears caches from:
  - **Chrome**: Browser cache
  - **VS Code**: Cached data and crash dumps
  - **Postman**: Cache and indexed data
  - **DBeaver**: Workspace metadata
  - **Android Studio**: Build caches
  - **OrbStack**: Docker/container storage (via CLI if available)

**Usage:**
```bash
clean                # Run full cleanup
clean_dev()          # Run development tools cleanup
```

### 2. automation_finder

Quick access aliases for navigating to common directories.

**Available Aliases:**

- `code_folder` - Opens your ~/code directory
- `downloads` - Opens your Downloads folder
- `desktop` - Opens your Desktop folder
- `documents` - Opens your Documents folder

**Usage:**
```bash
code_folder    # Open ~/code in Finder
downloads      # Open ~/Downloads in Finder
desktop        # Open ~/Desktop in Finder
documents      # Open ~/Documents in Finder
```

### 3. chrome_auto

Browser shortcuts that open Chrome with predefined sets of URLs for different workflows.

**Available Aliases:**

- `relax` - Opens entertainment sites:
  - YouTube
  - TikTok
  - Facebook

- `login_microsoft` - Opens Microsoft Outlook for email access

- `work` - Opens work-related sites:
  - GitHub
  - Jira
  - Microsoft MyApps
  - OneDrive
  - Outlook

- `music_relax` - Opens a relaxing music video on YouTube

**Usage:**
```bash
relax              # Open entertainment sites
login_microsoft    # Open Microsoft Outlook
work               # Open work-related sites
music_relax        # Open relaxing music
```

## Requirements

- macOS with Bash or Zsh
- Google Chrome (for chrome_auto scripts)
- Optional: OrbStack CLI (for advanced Docker cleanup)

## Contributing

Feel free to fork this repository and add more automation scripts! Here are some ideas:

- Additional application cleanup routines
- More browser workflows
- System performance monitoring aliases
- Development environment setup shortcuts

## License

This project is open source and available under the MIT License.

## Tips & Best Practices

- **Before running `clean` or `clean_dev`**: Make sure no development tools are actively using cache
- **Backup Important Data**: While these scripts target cache/temp files, always ensure you have backups before running system cleanup
- **Customize Aliases**: Feel free to modify the URLs and commands to match your personal workflow
- **Reload Configuration**: After editing your shell config file, remember to run `source ~/.zshrc` (or .bashrc) to apply changes

## Troubleshooting

**Aliases not working after adding to shell config?**
- Ensure the file is sourced correctly in your shell startup file
- Restart your terminal or run `source ~/.zshrc`

**Permission Denied errors?**
- Make sure you have proper permissions for the directories being accessed
- Some operations might require `sudo` privileges

**Chrome not opening with multiple URLs?**
- Chrome usually opens multiple tabs automatically when given multiple URLs
- If this doesn't work, ensure Chrome is set as your default browser

