# Zotero ODH (Online Dictionary Helper with Anki)

[![Using Zotero Plugin Template](https://img.shields.io/badge/Using-Zotero%20Plugin%20Template-blue?style=flat-square&logo=github)](https://github.com/windingwind/zotero-plugin-template)
![GitHub License](https://img.shields.io/github/license/1ywan/zotero-odh)
![](https://img.shields.io/badge/Zotero-7%20%7C%208-red)

A powerful dictionary lookup plugin for Zotero that integrates with Anki for vocabulary learning. Look up words while reading PDFs in Zotero and manage your Anki flashcards seamlessly.

![example](https://github.com/user-attachments/assets/3b4f267a-1bde-469b-8c34-fd354d703e7a)

## ✨ Features

### Dictionary Lookup
- **Instant word lookup** while reading PDFs in Zotero
- **25+ dictionary sources** including Collins, Cambridge, Oxford, Youdao, and more
- **Audio pronunciation** support
- **Context-aware definitions** with example sentences
- **Bilingual support** for multiple language pairs

### Anki Integration
- **Create flashcards** directly from dictionary definitions
- **Move existing cards** between decks (NEW!)
- **Smart card detection** - automatically finds existing cards in your deck
- **Customizable note fields** - map dictionary data to your Anki note type
- **Audio attachment** - automatically attach pronunciation audio to cards

### Card Management (NEW in v0.3.2)
- **Deck-to-deck card moving** - Move cards from one deck to another when you encounter words
- **Confirmation dialog** - Review before moving cards
- **Visual feedback** - See success/failure status immediately
- **Perfect for spaced repetition** - Move words you've encountered in context to a focused study deck

## 🚀 Quick Start

### Prerequisites

1. **Zotero 7.0 or 8.x** - [Download Zotero](https://www.zotero.org/download/)
2. **Anki** - [Download Anki](https://apps.ankiweb.net/)
3. **AnkiConnect** - [Install from AnkiWeb](https://ankiweb.net/shared/info/2055492159)

### Installation

1. Download the latest `.xpi` file from [Releases](https://github.com/1ywan/zotero-odh/releases)
2. In Zotero, go to **Tools → Add-ons**
3. Click the gear icon ⚙️ → **Install Add-on From File...**
4. Select the downloaded `.xpi` file
5. Restart Zotero

## 📖 Usage

### Basic Dictionary Lookup

1. Open a PDF in Zotero
2. Select any word or phrase
3. A popup will appear with dictionary definitions
4. Click the **+** button to add the word to Anki

### Moving Cards Between Decks

**Use Case**: You have a large vocabulary deck (e.g., 20,000 words) and want to focus on words you actually encounter while reading.

**Setup**:
1. Go to **Edit → Preferences → ODH**
2. Configure your decks:
   - **Source Deck**: Your main vocabulary deck (e.g., `COCA20000::lowfrequency`)
   - **Target Deck**: Your focused study deck (e.g., `COCA20000::plan`)
   - **Word Field**: The field to match words on (e.g., `Front`)

**Workflow**:
1. Select a word in a PDF
2. If the word exists in your source deck, a green **"Move to Plan Deck"** button appears
3. Click the button to move the card
4. Confirm the action in the dialog
5. The card is moved to your target deck for focused study

### Configuration

#### Anki Connection
- **Service**: Choose `AnkiConnect` (AnkiWeb support coming soon)
- **Deck Name**: Default deck for new cards
- **Note Type**: Anki note type to use
- **Field Mapping**: Map dictionary data to note fields
  - Expression → Front
  - Definition → Back
  - Sentence → Example
  - Audio → Audio field

#### Dictionary Settings
- **Dictionary Selection**: Choose from 25+ available dictionaries
- **System Scripts**: Built-in dictionary scripts
- **User Scripts**: Add custom dictionary scripts (coming soon)
- **Audio Preference**: Select preferred audio source

#### Card Moving Settings (NEW)
- **Source Deck**: Deck to search for existing cards
- **Target Deck**: Deck to move cards to
- **Word Field**: Field name to match words on (exact match)

## 🎯 Use Cases

### 1. Academic Reading
- Look up technical terms while reading research papers
- Build a specialized vocabulary deck for your field
- Move encountered terms to an active study deck

### 2. Language Learning
- Read foreign language articles in Zotero
- Create flashcards with context from real texts
- Focus on vocabulary you actually encounter

### 3. Vocabulary Management
- Maintain a master vocabulary deck (e.g., 20,000 words)
- Move words to a focused deck as you encounter them
- Study words in context rather than arbitrary lists

## 🛠️ Build from Source

### Requirements
- Node.js 20 or higher
- npm

### Build Steps

```bash
# Clone the repository
git clone https://github.com/1ywan/zotero-odh.git
cd zotero-odh

# Install dependencies
npm install

# Build the plugin
npm run build

# The built plugin will be in build/zotero-odh.xpi
```

### Development

```bash
# Start development server with hot reload
npm start

# Build for production
npm run build

# Create a release
npm run release
```

## 📋 Feature Status

| Status             | Feature                          |
| ------------------ | -------------------------------- |
| ✅                 | Anki Connect Service             |
| ✅                 | Dictionary lookup in PDFs        |
| ✅                 | 25+ dictionary sources           |
| ✅                 | Audio pronunciation              |
| ✅                 | Create Anki cards                |
| ✅                 | Move cards between decks         |
| ✅                 | Zotero 7 & 8 support             |
| ⏳                 | Anki Web Service                 |
| ⏳                 | User-defined dictionary scripts  |
| ⏳                 | Batch card operations            |

## 🔧 Troubleshooting

### Dictionary popup doesn't appear
- Check that the plugin is enabled in Tools → Add-ons
- Verify you're selecting text in a PDF (not in the library view)
- Try restarting Zotero

### Can't connect to Anki
- Make sure Anki is running
- Verify AnkiConnect is installed and enabled
- Check that AnkiConnect is listening on port 8765
- Try restarting Anki

### Move button doesn't appear
- Verify the word exists in your source deck
- Check that the word field name matches exactly (case-sensitive)
- Ensure AnkiConnect service is selected in preferences
- Make sure source and target deck names are correct

### Card not found in source deck
- The plugin uses exact word matching
- Check the word field contains the exact word (not lemmatized)
- Verify the deck name includes parent decks (e.g., `Parent::Child`)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Based on [ODH (Online Dictionary Helper)](https://github.com/ninja33/ODH) for Chrome/Firefox
- Built with [Zotero Plugin Template](https://github.com/windingwind/zotero-plugin-template)
- Inspired by the Zotero and Anki communities

## 📧 Support

- **Issues**: [GitHub Issues](https://github.com/1ywan/zotero-odh/issues)
- **Discussions**: [GitHub Discussions](https://github.com/1ywan/zotero-odh/discussions)
- **Zotero Forums**: [Zotero Forums](https://forums.zotero.org/)

## 🔗 Related Projects

- [Anki](https://apps.ankiweb.net/) - Spaced repetition flashcard program
- [AnkiConnect](https://ankiweb.net/shared/info/2055492159) - Anki plugin for external applications
- [ODH](https://github.com/ninja33/ODH) - Original Online Dictionary Helper browser extension
- [Zotero](https://www.zotero.org/) - Reference management software

---

**Star ⭐ this repository if you find it helpful!**
