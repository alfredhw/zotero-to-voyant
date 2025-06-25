# Zotero to Voyant Tools Plugin

A Zotero 7 plugin that allows you to send PDF and text attachments from your Zotero library directly to Voyant Tools for text analysis.

## Features

- 📚 Send single or multiple PDF/text files to Voyant Tools
- 🖱️ Right-click context menu integration
- 📋 Tools menu integration  
- 📊 Automatic corpus creation in Voyant
- 🔄 Supports PDF, TXT, and HTML attachments

## Installation

### Quick Install

1. Download the latest `.xpi` file from the [Releases](https://github.com/YOUR_USERNAME/zotero-to-voyant/releases) page
2. In Zotero, go to Tools → Add-ons
3. Click the gear icon (⚙️) → Install Add-on From File...
4. Select the downloaded `.xpi` file
5. Restart Zotero

### Requirements

- Zotero 7 or later
- Internet connection (for uploading to Voyant Tools)

## Usage

### Method 1: Right-Click
1. Select one or more items with PDF/text attachments in your Zotero library
2. Right-click → "Send to Voyant Tools"
3. Wait for upload to complete
4. Voyant Tools will open in your browser

### Method 2: Tools Menu
1. Select items with attachments
2. Tools → Send to Voyant Tools

## Supported File Types

- PDF files (`.pdf`)
- Text files (`.txt`)
- HTML files (`.html`)

## Building from Source

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/zotero-to-voyant.git
cd zotero-to-voyant

# Build the XPI
./build.sh
# Or manually:
zip -r zotero-to-voyant.xpi bootstrap.js manifest.json prefs.js icon*.png
```

## Troubleshooting

**"No supported attachments found"**
- Ensure you've selected items that have PDF or text attachments
- Check that attachment files exist and aren't broken links

**Upload fails**
- Check your internet connection
- Try with a smaller file first
- Voyant Tools may be temporarily unavailable

**Plugin doesn't appear in menus**
- Make sure you're using Zotero 7 (not Zotero 6)
- Try restarting Zotero
- Check Tools → Add-ons to verify the plugin is enabled

## Development

To modify this plugin:

1. Make changes to `bootstrap.js`
2. Update version in `manifest.json`
3. Run `./build.sh` to create new XPI
4. Test in Zotero

For debugging:
- Enable debug logging: Help → Debug Output Logging → Enable
- View logs: Help → Debug Output Logging → View Output
- Run JavaScript: Tools → Developer → Run JavaScript

## How It Works

The plugin:
1. Gets selected items from your Zotero library
2. Extracts PDF and text attachments
3. Uploads files to Voyant Tools using multipart/form-data
4. Opens the resulting corpus in your default browser

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [Voyant Tools](https://voyant-tools.org/) for providing the text analysis platform
- [Zotero](https://www.zotero.org/) for the excellent reference management software
- Based on Zotero's plugin development guidelines

## Author

Alfred Wallace - alfred.wallace@und.edu
Created with the assistance of Claude 4 Opus, as part of a series of experiments with "vibe coding" for librarians and information professionals

## Version History

- 1.0.0 (2025-06-15) - Initial release

---

If you find this plugin helpful, please give it a ⭐ on GitHub!
