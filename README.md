# Zhongwen Reader
Zhongwen Reader is a lightweight hover dictionary plugin for Obsidian that makes it easy to read Chinese text and build your vocabulary, all from within your notes.

> ⚠️ **Installation Note:** If cloning this repo, the folder in `.obsidian/plugins` must be named `zhongwen-reader`, not `obsidian-zhongwen-reader`.

[![Buy me a coffee!](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/natipt)

# ✨ Features
- 🔍 **Hover Dictionary:** Instantly see simplified, traditional, pinyin, and definitions (from CC-CEDICT) on hover.
  - 🗣️ **Bopomofo Support (注音):** Contributed by [@wongjustin99](https://github.com/wongjustin99). (Coming to Community Plugins soon!)
- 💡 **HSK Highlighting:** Toggle color-coded vocab highlighting by HSK level.
- 📥 **Save Words:** Use the command palette to save hovered words to a vocab list.
  - 🧠 **Sentence Capture:** Optionally save example sentences when adding vocab.
- 📋 **Sidebar View:** See vocab from the current note and jump to word locations.
- 🗃️ **Flashcard Export:** Export saved vocab as markdown flashcards for the Spaced Repetition plugin.

> ⚠️ **Note:** Example sentences are saved to `vocab.json` but not yet used in flashcards or sidebar. Support coming soon.

# 🛠️ How to Use
- Hover over any Chinese word (in Edit or Preview mode) to see a popup.
- Save a word from the hover popup using the command palette.
- Open the 📘 Sidebar View to browse words in the current note.
- Use the palette to Export Vocab to Flashcards or toggle HSK highlights.
- For Anki export, use the palette to Export Vocab to CSV. Anki can import this CSV file with field separator set to semicolon. 

# ⚙️ Settings
- Save Sentence: Automatically capture the sentence where the word appears.
  
# 🧾 Data & Storage
- Must be connected to wifi on first activation **only**, the plugin downloads the following files and subsequently functions offline:
  - `cedict_ts.u8` – Chinese-English dictionary (9.7MB, from CC-CEDICT)
  - `hsk-vocab.json` – HSK word lists (54KB)
- Saved vocab is stored in `/plugins/zhongwen-reader/vocab.json`
- Example entry
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
You can delete these files manually anytime. If you delete `vocab.json` your saved vocab will be lost. A future release will add cleanup options in settings.

# 🐛 Bugs & ⭐ Feature Requests
Found a bug?
1. Open a [GitHub issue](https://github.com/natipt/obsidian-zhongwen-reader/issues)
2. Include:
  - What happened
  - How to reproduce it
  - Your system info (Obsidian version, OS, plugin version)
  - Screenshots or errors (if applicable)

Want a feature?
1. Open a GitHub issue with a title starting with Feature Request: and a short summary. In the description:
2. Explain the functionality you'd like to see
3. Include your use case and why it would help

# 📦 Coming soon
- [ ] Export to Anki .apkg
- [ ] Toggle vocab sidebar
- [ ] Database-style vocab view
- [ ] Built-in spaced repetition with cloze support
- [ ] Improved tooltip layout and customization
- [x] HSK word data with highlights (like Du Chinese)
