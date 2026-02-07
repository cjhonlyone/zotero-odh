# Zotero ODH (Online Dictionary Helper with Anki)

[![Using Zotero Plugin Template](https://img.shields.io/badge/Using-Zotero%20Plugin%20Template-blue?style=flat-square&logo=github)](https://github.com/windingwind/zotero-plugin-template)
![GitHub License](https://img.shields.io/github/license/cjhonlyone/zotero-odh)
![](https://img.shields.io/badge/Zotero-7%20%7C%208-red)
![Version](https://img.shields.io/badge/version-0.4.0-green)

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
- **Display Anki card content** - Show existing card content instead of online dictionary (NEW in v0.4.0)
- **Move existing cards** between decks
- **Smart card detection** with flexible matching:
  - Case-insensitive search (NEW in v0.4.0)
  - Word form detection (plurals, verb forms, etc.) (NEW in v0.4.0)
  - Finds "run" when searching "running", "ran", or "Running"
- **Customizable note fields** - map dictionary data to your Anki note type
- **Audio attachment** - automatically attach pronunciation audio to cards

### Card Management
- **Deck-to-deck card moving** - Move cards from one deck to another when you encounter words
- **One-click moving** - No confirmation needed, instant feedback
- **Visual feedback** - See success/failure status immediately
- **Perfect for spaced repetition** - Move words you've encountered in context to a focused study deck
- **Inline move button** - Compact button placed next to word definition (NEW in v0.4.0)

### Anki Card Content Display (NEW in v0.4.0)
- **Skip online dictionary** - Display content directly from your Anki cards
- **Faster lookup** - No waiting for online dictionary queries
- **Customizable fields** - Choose which card fields to display
- **Field ordering** - Display fields in your preferred order
- **Perfect for review** - See your own card content while reading

## 🚀 Quick Start

### Prerequisites

1. **Zotero 7.0 or 8.x** - [Download Zotero](https://www.zotero.org/download/)
2. **Anki** - [Download Anki](https://apps.ankiweb.net/)
3. **AnkiConnect** - [Install from AnkiWeb](https://ankiweb.net/shared/info/2055492159)

### Installation

1. Download the latest `.xpi` file from [Releases](https://github.com/cjhonlyone/zotero-odh/releases)
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

### Using Anki Card Content (NEW in v0.4.0)

**Use Case**: You want to see your own Anki card content instead of waiting for slow online dictionaries.

**Setup**:
1. Go to **Edit → Preferences → ODH → Anki Settings**
2. Configure:
   - **Source Deck**: Your vocabulary deck (e.g., `COCA20000::lowfrequency`)
   - **Word Field**: Field to search on (e.g., `expression`, `Front`)
   - ✅ **Use Anki card content**: Enable this option
   - **Display Fields**: Fields to show (e.g., `sentence,glossary,definition`)

**Workflow**:
1. Select a word in a PDF
2. If the word exists in your Anki deck, it shows your card content immediately
3. No waiting for online dictionary
4. Fields are displayed in the order you specified

**Example Configuration**:
```
Source Deck: COCA20000::lowfrequency
Word Field: expression
Display Fields: sentence,glossary,phonetic,definition
```
This will show sentence first, then glossary, phonetic, and definition.

### Moving Cards Between Decks

**Use Case**: You have a large vocabulary deck (e.g., 20,000 words) and want to focus on words you actually encounter while reading.

**Setup**:
1. Go to **Edit → Preferences → ODH → Anki Settings**
2. Configure your decks:
   - **Source Deck**: Your main vocabulary deck (e.g., `COCA20000::lowfrequency`)
   - **Target Deck**: Your focused study deck (e.g., `COCA20000::plan`)
   - **Word Field**: The field to match words on (e.g., `expression`, `Front`)

**Workflow**:
1. Select a word in a PDF
2. If the word exists in your source deck, a green **"Move"** button appears next to the word
3. Click the button to instantly move the card
4. The card is moved to your target deck for focused study
5. Works with different word forms (running → run, books → book)

### Smart Word Matching (NEW in v0.4.0)

The plugin now intelligently matches words using multiple strategies:

1. **Exact match**: Tries the word as-is first
2. **Case-insensitive**: `Running` finds `running`
3. **Word forms**: Uses 82,000+ word form rules
   - Plurals: `books` → `book`
   - Verb forms: `running`, `ran` → `run`
   - Comparatives: `bigger` → `big`
   - Third person: `goes` → `go`

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

#### Anki Card Settings (NEW in v0.4.0)
- **Source Deck**: Deck to search for existing cards (e.g., `COCA20000::lowfrequency`)
- **Target Deck**: Deck to move cards to (e.g., `COCA20000::plan`)
- **Word Field**: Field name to match words on (e.g., `expression`, `Front`)
- **Use Anki content**: Enable to show card content instead of online dictionary
- **Display Fields**: Comma-separated field names to display (e.g., `sentence,glossary`)
  - Fields are shown in the order specified
  - Leave empty to show all fields

## 🎯 Use Cases

### 1. Academic Reading with Personal Notes
- Look up technical terms while reading research papers
- See your own Anki card notes instead of generic dictionary definitions
- Move encountered terms to an active study deck
- Focus on vocabulary you actually encounter in your field

### 2. Language Learning Immersion
- Read foreign language articles in Zotero
- Display your custom card content with personal mnemonics
- Create flashcards with context from real texts
- Study words in context rather than arbitrary lists

### 3. Advanced Vocabulary Management
- Maintain a master vocabulary deck (e.g., 20,000 words)
- Show personal notes and context from your cards
- Move words to a focused deck as you encounter them
- Works with all word forms (no need to search for exact form)

### 4. Fast Review Workflow (NEW)
- Skip slow online dictionary lookups
- See your Anki content instantly
- Choose which card fields to display
- Perfect for quick review while reading

## 🛠️ Build from Source

### Requirements
- Node.js 20 or higher
- npm

### Build Steps

```bash
# Clone the repository
git clone https://github.com/cjhonlyone/zotero-odh.git
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

| Status | Feature                                 |
| ------ | --------------------------------------- |
| ✅     | Anki Connect Service                    |
| ✅     | Dictionary lookup in PDFs               |
| ✅     | 25+ dictionary sources                  |
| ✅     | Audio pronunciation                     |
| ✅     | Create Anki cards                       |
| ✅     | Move cards between decks                |
| ✅     | Display Anki card content               |
| ✅     | Smart word matching (case, word forms)  |
| ✅     | Customizable field display              |
| ✅     | Zotero 7 & 8 support                    |
| ⏳     | Anki Web Service                        |
| ⏳     | User-defined dictionary scripts         |
| ⏳     | Batch card operations                   |

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
- Verify the word exists in your source deck (tries multiple forms automatically)
- Check that the word field name matches exactly (case-sensitive)
- Ensure AnkiConnect service is selected in preferences
- Make sure source and target deck names are correct

### Card not found in source deck
- The plugin now tries multiple word forms automatically
- Check the word field name in preferences (e.g., `expression`, `Front`)
- Verify the deck name includes parent decks (e.g., `Parent::Child`)
- Check Zotero debug logs: Help → Debug Output Logging → View Output

### Anki content not showing
- Verify "Use Anki card content" is enabled in preferences
- Check that the source deck and word field are configured
- Make sure the word exists in your deck
- Verify Display Fields configuration (e.g., `sentence,glossary`)

## 🆕 What's New in v0.4.0

- **Anki Card Content Display**: Show your Anki card content instead of online dictionaries
- **Customizable Field Display**: Choose which fields to display and in what order
- **Smart Word Matching**: Case-insensitive search + 82,000+ word form rules
- **Improved UI**: Compact move button placed inline with definitions
- **Better Performance**: Skip slow online dictionary when using Anki content

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

