# 🍎 Open Vocabularies

Open-source, community-driven vocabulary datasets for major language proficiency exams (TOEIC, JLPT, HSK, etc.). Our mission is to take high-quality base word lists and transform them into refined, multi-locale datasets contributed by the community. These datasets power the vocabulary features in the [Ringoo](https://ringoo.ai) app.

## 🚀 Goal

The mission of this repository is to provide **highly accurate, high-quality, and machine-readable** word lists for language learners. By open-sourcing these lists, we aim to:
1. **Ensure Accuracy:** Allow teachers and native speakers to audit and fix terminology.
2. **Standardization:** Provide a consistent JSON schema for linguistic data.
3. **Accessibility:** Support exports to popular formats like Anki, CSV, and more.
4. **Multi-locale Support:** Provide high-quality translations and localized versions to help learners from all backgrounds.

---

## 📂 Repository Structure

The data is organized by language and exam type under the `data/` directory:

```text
open-vocabularies/
├── data/                # Vocabulary datasets
│   ├── ja/              # Japanese Exam Datasets
│   │   ├── jlpt-n5.json         # Master JSON dataset
│   │   ├── jlpt-n5.csv          # Upstream Source
│   │   ├── jlpt-n5_{locale}.csv # Localized Dataset
│   │   └── ...
│   └── en/              # English Exam Datasets
│       ├── toeic.json           # Master JSON dataset
│       ├── toeic.csv            # Upstream Source
│       └── toeic_{locale}.csv   # Localized Dataset
├── schema.json          # The master data structure definition
└── scripts/             # Data validation and export tools
```

## 📜 Sources & Credits

We stand on the shoulders of giants. The base datasets are derived from high-quality educational resources and refined by the community:

- **TOEIC Vocabulary:** Base word lists sourced from [Pass the TOEIC Test](https://www.pass-the-toeic-test.com/toeic-word-list.php).
- **JLPT Vocabulary:** Base word lists sourced from [Open Anki JLPT Decks](https://github.com/jamsinclair/open-anki-jlpt-decks).
- **Maintenance:** These lists are actively reviewed, corrected, and expanded by **Ringoo app users** and community contributors to ensure they reflect modern usage and bridge exam-specific nuances.

---

## 🛠 Data Format

We provide datasets in both **JSON** and **CSV** formats to balance rich metadata with ease of use.

### CSV (Distribution)
Anki-compatible format for quick import and basic study.

```csv
expression,reading,meaning,tags,guid
innovation,,a new method, idea, or product,TOEIC,unique-id-001
```

---

## 🗃 Exporting and Usage

While we provide pre-generated CSVs in the `data/` directory, you can also use our scripts to generate custom exports:
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
