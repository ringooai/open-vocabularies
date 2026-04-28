# 🍎 Open Vocabularies (開放詞彙數據集)

主要語言能力考試（TOEIC、JLPT、HSK 等）的開源、社群驅動詞彙數據集。我們的使命是獲取高品質的基礎詞彙表，並透過社群的貢獻，將其轉化為精煉的多語言數據集。這些數據集目前用於支援 [Ringoo](https://ringoo.ai) 應用程式中的詞彙功能。

## 🚀 目標

本存儲庫的使命是為語言學習者提供**高度準確、高品質且機器可讀**的單語表。透過開源這些列表，我們旨在：

1. **確保準確性：** 讓教師和母語人士能夠審核並修正術語。
2. **標準化：** 為語言數據提供一致的 JSON 模式（Schema）。
3. **可訪問性：** 支援導出到 Anki、CSV 等常用格式。
4. **多語言支援：** 提供高品質的翻譯和本地化版本，以幫助來自各種背景的學習者。

---

## 📂 專案結構

數據按語言和考試類型整理在 `data/` 目錄下：

```text
open-vocabularies/
├── data/                # 詞彙數據集
│   ├── ja/              # 日語考試數據集
│   │   ├── jlpt-n5.json         # Master JSON 數據集
│   │   ├── jlpt-n5.csv          # 上游源文件 (Upstream Source)
│   │   ├── jlpt-n5_{locale}.csv # 本地化數據集 (Localized Dataset)
│   │   └── ...
│   └── en/              # 英語考試數據集
│       ├── toeic.json           # Master JSON 數據集
│       ├── toeic.csv            # 上游源文件 (Upstream Source)
│       └── toeic_{locale}.csv   # 本地化數據集 (Localized Dataset)
├── schema.json          # Master 數據結構定義
└── scripts/             # 數據驗證與導出工具
```

## 📜 來源與致謝

我們站在巨人的肩膀上。基礎數據集源自高品質的教育資源，並由社群進一步精煉：

- **TOEIC 詞彙：** 基於 [Pass the TOEIC Test](https://www.pass-the-toeic-test.com/toeic-word-list.php) 提供的基礎列表。
- **JLPT 詞彙：** 基於 [Open Anki JLPT Decks](https://github.com/jamsinclair/open-anki-jlpt-decks) 提供的基礎列表。
- **維護：** 這些列表由 **Ringoo App 用戶**和社群貢獻者積極審核、修正和擴展，以確保它們反映現代用法並彌補特定考試的細微差別。

---

## 🛠 數據格式

我們提供 **JSON** 和 **CSV** 兩種格式的數據集，以平衡豐富的元數據與易用性。

### CSV (發佈版本)
Anki 兼容格式，用於快速導入和基礎學習。

```csv
expression,reading,meaning,tags,guid
innovation,,a new method, idea, or product,TOEIC,unique-id-001
```

---

## 🗃 導出與使用

雖然我們在 `data/` 目錄中提供了預生成的 CSV，您也可以使用我們的腳本生成自定義導出：
1. 複製 (Clone) 此存儲庫。
2. 執行 `npm run export:anki`。
3. 將生成的 `.csv` 或 `.apkg` 文件導入您的 Anki 應用程式。

---

## 🤝 如何貢獻

我們歡迎各種貢獻！如果您發現錯別字、錯誤翻譯，或想添加新的考試列表：
1. **Fork** 此存儲庫。
2. 進行更改並確保它們符合 `schema.json`。
3. 提交 **Pull Request** 並簡要說明您的更改。

---

## 📱 互動練習

想透過即時回饋練習這些單詞嗎？使用 [Ringoo App](https://ringoo.ai) 可以：
- 透過沉浸式 AI 對話學習單詞。
- 利用智能間隔重複 (SRS) 追蹤您的進度。
- 聆聽自然流暢的 AI 生成發音。

## ⚖️ 授權條款

本存儲庫中的所有數據集均根據 **MIT 授權條款** 提供。您可以自由地將它們用於自己的專案、應用程式和研究。
