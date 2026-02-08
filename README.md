# Zotero ODH (Online Dictionary Helper with Anki)

[![Using Zotero Plugin Template](https://img.shields.io/badge/Using-Zotero%20Plugin%20Template-blue?style=flat-square&logo=github)](https://github.com/windingwind/zotero-plugin-template)
![GitHub License](https://img.shields.io/github/license/cjhonlyone/zotero-odh)
![](https://img.shields.io/badge/Zotero-7%20%7C%208-red)
![Version](https://img.shields.io/badge/version-0.4.0-green)

A dictionary lookup plugin for Zotero that integrates with Anki. Look up words while reading PDFs and manage Anki flashcards seamlessly.

![example](https://github.com/user-attachments/assets/3b4f267a-1bde-469b-8c34-fd354d703e7a)

## ✨ Features

- **Instant word lookup** in PDFs with 25+ dictionary sources
- **Create Anki flashcards** from definitions with audio
- **Display Anki card content** instead of online dictionary (fast, no network delay)
- **Move cards between decks** with one click
- **Customizable field display**: choose which fields to show and in what order

## 🚀 Installation

**Requirements**: Zotero 7+, Anki, [AnkiConnect](https://ankiweb.net/shared/info/2055492159)

1. Download `.xpi` from [Releases](https://github.com/cjhonlyone/zotero-odh/releases)
2. Zotero → **Tools → Add-ons** → gear icon → **Install Add-on From File**
3. Restart Zotero

## 📖 Usage

### Basic Lookup
1. Select text in a PDF → popup shows definitions
2. Click **+** button to create Anki card

### Show Anki Card Content (v0.4.0)
Display your own card content instead of querying online dictionaries.

**Setup** (Edit → Preferences → ODH → Anki Settings):
- **Source Deck**: e.g., `COCA20000::lowfrequency`
- **Word Field**: e.g., `expression`, `Front`
- ✅ **Use Anki card content**
- **Display Fields**: e.g., `sentence,glossary` (comma-separated, displayed in order)

**Result**: Select a word → shows your card content instantly (no network wait).

### Move Cards Between Decks
Move words from a large deck to a focused study deck when you encounter them.

**Setup** (Edit → Preferences → ODH → Anki Settings):
- **Source Deck**: e.g., `COCA20000::lowfrequency`
- **Target Deck**: e.g., `COCA20000::plan`
- **Word Field**: e.g., `expression`

**Result**: Select a word → green **Move** button appears → click to move card instantly. Works with word forms: `running`/`ran`/`Running` all match `run`.

## ⚙️ Configuration

**Anki Settings** (Edit → Preferences → ODH → Anki):
- **Service**: AnkiConnect
- **Deck/Note Type/Field Mapping**: For creating new cards
- **Source/Target Deck + Word Field**: For moving cards
- **Use Anki content + Display Fields**: For showing card content

**Dictionary Settings**: Choose from 25+ dictionaries, audio sources

## 🆕 v0.4.0 Changes

- Display Anki card content (skip online dictionary)
- Smart word matching (case-insensitive + word forms)
- Customizable field display with ordering
- Improved UI (inline move button)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Claude/CJH** - Development and enhancements

## 🙏 Acknowledgments

- Original author: [1ywan](https://github.com/1ywan/zotero-odh)
- Based on [ODH (Online Dictionary Helper)](https://github.com/ninja33/ODH) for Chrome/Firefox
- Built with [Zotero Plugin Template](https://github.com/windingwind/zotero-plugin-template)
- Inspired by the Zotero and Anki communities

## 📧 Support

- **Issues**: [GitHub Issues](https://github.com/cjhonlyone/zotero-odh/issues)
- **Discussions**: [GitHub Discussions](https://github.com/cjhonlyone/zotero-odh/discussions)
- **Zotero Forums**: [Zotero Forums](https://forums.zotero.org/)

## 🔗 Related Projects

- [Anki](https://apps.ankiweb.net/) - Spaced repetition flashcard program
- [AnkiConnect](https://ankiweb.net/shared/info/2055492159) - Anki plugin for external applications
- [ODH](https://github.com/ninja33/ODH) - Original Online Dictionary Helper browser extension
- [Zotero](https://www.zotero.org/) - Reference management software

---

**Star ⭐ this repository if you find it helpful!**

