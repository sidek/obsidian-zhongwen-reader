# Zhongwen Reader
Zhongwen Reader is a lightweight hover dictionary plugin for Obsidian (https://obsidian.md) that makes it easy to read Chinese text and build your vocabulary, all from within your notes. Originally based on obsidian-sample-plugin by the Obsidian team.

> ⚠️ **Warning:** If cloning this repository, make sure the folder inside your .obsidian/plugins is .obsidian/plugins/zhongwen-reader and not .obsidian/plugins/obsidian-zhongwen-reader.

# ✨ Features
- 🔍 Hover lookup: When this plugin is enabled, instantly see simplified, traditional, pinyin, and definitions (from CC-CEDICT dictionary) in a tooltip popup when hovering over Chinese words in your markdown editor or preview mode.
- 💡 HSK Highlighting: Use the command palette to toggle document-wide color-coded highlighting of vocabulary words from any of the HSK exams
- 📥 Save vocab: Select "Save Hovered Word to Vocab List" in the command palette while hovering to save a word to your personal vocab list
- 🧠 Example sentence capture: If the setting is enabled, automatically saves the sentence where you found the word into your vocab list as an example sentence. If you find the same vocab entry within a different sentence/context, the command "Save Hovered Word to Vocab List" will add the sentence as an additional example to the existing vocab entry.
- 📋 Sidebar view: See a list of vocab words used in the current note and navigate to the word within the note with a click.
- 🗃️ Spaced repetitions deck generation: Generate flashcards for the obsidian spaced repetitions plugin from your vocab list.

> ⚠️ **Warning:** As of now, the example sentences are saved into vocab.json but are not used in flashcard generation or shown in the plugin sidebar. Upcoming features will make use of them.

[![Buy me a coffee!](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/natipt)

# 🐛 Reporting Bugs
If you encounter a bug or something isn't working as expected:
1. Open an [Issue on GitHub](https://github.com/natipt/obsidian-zhongwen-reader/issues)
2. Include the following details:
  - A clear description of the issue
  - Steps to reproduce it, if possible
  - Your system info (Obsidian version, OS, plugin version)
  - Any relevant screenshots or error messages
This helps me investigate and fix things faster—thank you!

# 🧾 Data & Storage
If you install this plugin through Obsidian or BRAT, you must be connected to wifi **the first time you activate the plugin** so that it can download the open source Chinese-English dictionary CEDICT and the file hsk-vocab.json containing the vocabulary from each HSK exam. You can view both files in the github repository. After this initial download, the plugin will work entirely offline and can be deactivated and reactivated at will without wifi. Installing the plugin downloads and stores the CC-CEDICT dictionary (https://cc-cedict.org/wiki/) as a `.u8` file with path `.obsidian/plugins/zhongwen-reader/cedict_ts.u8`. This file is 9.7MB.

Saved vocab is stored in `.obsidian/plugins/zhongwen-reader/vocab.json`.
Each entry includes:
```json
{
  "simplified": "弯月",
  "traditional": "彎月",
  "pinyin": "wan1 yue4",
  "definitions": [
    "crescent moon",
    "crescent shape"
  ],
  "addedAt": "2025-04-07T17:29:18.497Z",
  "exampleSentences": [
    "弯月相同弯刀刺上林端。"
  ]
}
```
You can manually delete these files at any time. A future release will add the option to clean up these files from the Settings menu.
# 🛠️ Usage
- Hover over any Chinese word in edit or preview mode to view its meaning.
- Use the command palette to save the word (and its surrounding sentence) to your vocab list.
- Click the 📘 icon in the sidebar to view all saved words in the current note.
- Use the command palette to run “Export Vocab to Flashcards” and generate an .md deck.
- Use the command palette to toggle highlighting of HSK words in a given note.

# ⚙️ Settings
- Save sentence: Automatically capture the sentence a word appears in when saving vocab.

# 📦 Coming soon
- [ ] Export to Anki .apkg
- [ ] Better vocab highlights when scrolling to a vocab word from the sidebar
- [ ] Toggle vocab sidebar on/off
- [ ] Database view of vocab list
- [x] HSK data for vocab words, highlighting similar to du-chinese app
- [ ] Native spaced repetitions within Zhongwen Reader with cloze support
- [ ] Better tooltip sizing/positioning
- [ ] User customizability in tooltip layout/contents and sidebar layout/contents
