> [!CAUTION]
> This project is currently under active development. Expect breaking changes and potential backward incompatibility as we evolve.

# 🍎 exam-vocabularies

Open-source, community-driven vocabulary datasets for major language proficiency exams (TOEIC, JLPT, HSK, etc.). These datasets are used to power the vocabulary features in the [Ringoo](https://ringoo.ai) app.

## 🚀 Goal

The mission of this repository is to provide **highly accurate, high-quality, and machine-readable** word lists for language learners. By open-sourcing these lists, we aim to:
1. **Ensure Accuracy:** Allow teachers and native speakers to audit and fix terminology.
2. **Standardization:** Provide a consistent JSON schema for linguistic data.
3. **Accessibility:** Support exports to popular formats like Anki, CSV, and more.

---

## 📂 Repository Structure

The data is organized by language and exam type to keep things clean:

```text
exam-vocabularies/
├── schema.json          # The master data structure definition
├── en/                  # English Exam Datasets
│   └── toeic.json       # TOEIC Essential Vocabulary
├── ja/                  # Japanese Exam Datasets
│   ├── jlpt-n5.json
│   ├── jlpt-n4.json
│   └── ...
└── scripts/             # Data validation and export tools
```

## 📜 Sources & Credits

We stand on the shoulders of giants. The base datasets are derived from high-quality educational resources and refined by the community:

- **TOEIC Vocabulary:** Base word lists provided by [Pass the TOEIC Test](https://www.pass-the-toeic-test.com/toeic-word-list.php).
- **JLPT Vocabulary:** Base word lists provided by [Open Anki JLPT Decks](https://github.com/jamsinclair/open-anki-jlpt-decks).
- **Maintenance:** These lists are actively reviewed, corrected, and expanded by **Ringoo app users** and community contributors to ensure they reflect modern usage and bridge exam-specific nuances.

---

## 🛠 Data Format (JSON)

We use **JSON** as our primary format to support complex linguistic metadata (e.g., furigana, parts of speech, and multiple translations).

```json
{
  "id": "toeic-001",
  "word": "innovation",
  "meaning": "a new method, idea, or product",
  "pos": "noun",
  "example": "Technical innovation is the key to business success."
}
```

---

## 🗃 Exporting to Anki

While JSON is our source of truth, we provide scripts to generate Anki-compatible formats:
1. Clone the repo.
2. Run `npm run export:anki`.
3. Import the generated `.csv` or `.apkg` files into your Anki app.

---

## 🤝 How to Contribute

We welcome contributions! If you find a typo, a wrong translation, or want to add a new exam list:
1. **Fork** the repository.
2. Make your changes and ensure they match the `schema.json`.
3. **Submit a Pull Request** with a brief description of your changes.

---

## 📱 Interactive Practice

Want to practice these words with real-time feedback? Use the [Ringoo App](https://ringoo.ai) to:
- Learn words via immersive AI conversations.
- Trace your progress with smart spaced repetition.
- Listen to natural AI-generated pronunciations.

## ⚖️ License

All datasets in this repository are available under the **MIT License**. Feel free to use them for your own projects, apps, and research.
