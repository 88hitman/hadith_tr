

```markdown
# Hadith Collections — Multi-Language JSONL Dataset

This repository contains machine-readable files of major hadith collections, in multiple languages, using open standards (JSONL and JSON).  
Each collection is stored in its own folder, with clear versioning and structure.

---

## 📂 Repository Structure

```

sahih\_bukhari/
├── bukhari\_hadiths.jsonl   # All hadiths, newline-delimited JSON
├── bukhari\_sections.json   # All section info, grouped by chapter/subject
└── metadata.json           # Version, language, and file information
sahih\_muslim/
├── muslim\_hadiths.jsonl
├── muslim\_sections.json
└── metadata.json
...
README.md
LICENSE

````

---

## 📚 File Descriptions

### **Hadiths File** (`*_hadiths.jsonl`)

- **Type:** JSONL (newline-delimited JSON)
- **One hadith per line** (see example below)
- **Languages:** Arabic, English, French (extendable)

Each line:
```json
{
  "hadith_number": 123,
  "arabic_number": 123,
  "translation_version": 2,
  "reference": {
    "book": 1,
    "hadith": 5
  },
  "arabic":  "حَدَّثَنَا ...",  
  "english": "Narrated ...",
  "french":  "Rapporté par ..."
}
````

| Field                 | Description                                        |
| --------------------- | -------------------------------------------------- |
| `hadith_number`       | Unique sequential identifier for this dataset      |
| `arabic_number`       | Original Arabic numbering (as in print edition)    |
| `translation_version` | Increments on any translation change               |
| `reference.book`      | Book number in the collection (section - ex: 1 )   |
| `reference.hadith`    | Position within the book                           |
| `arabic`              | Original Arabic text                               |
| `english`             | Reliable English rendering                         |
| `french`              | Current French translation                         |

**Preview example:**

```jsonl
{"hadith_number":123,"arabic_number":123,"translation_version":1,"reference":{"book":1,"hadith":5},"arabic":"حَدَّثَنَا أَبُو...","english":"Narrated Abu ...","french":"Rapporté par ..."}
{"hadith_number":124,"arabic_number":124,"translation_version":1,"reference":{"book":1,"hadith":6},"arabic":"عَنْ عَائِشَةَ...","english":"Narrated Aisha ...","french":"Rapporté par Aïcha ..."}
{"hadith_number":125,"arabic_number":125,"translation_version":1,"reference":{"book":1,"hadith":7},"arabic":"قَالَ النَّبِيُّ...","english":"The Prophet ﷺ said ...","french":"Le Prophète ﷺ a dit ..."}
```

---

### **Sections File** (`*_sections.json`)

* **Type:** JSON array
* **One object per section/chapter**

```json
[
  {
    "section_number": 1,
    "name": {
      "en": "Revelation",
      "fr": "La Révélation",
      "ar": "...",
    },
    "first_hadith_number": 1,
    "last_hadith_number": 7,
    "first_arabic_number": 1,
    "last_arabic_number": 7
  },
  ...
]
```

| Field                 | Description                                |
| --------------------- | ------------------------------------------ |
| `section_number`      | Sequential number for this section/chapter |
| `name.en` / `name.fr` | Name of the section in each language       |
| `first_hadith_number` | The hadith number starting this section    |
| `last_hadith_number`  | The hadith number ending this section      |
| `first_arabic_number` | Arabic numbering for the first hadith      |
| `last_arabic_number`  | Arabic numbering for the last hadith       |

---

### **Metadata File** (`_metadata.json`)

* Version and context for each collection.
* Example:

```json
{
  "collection": "Sahih Bukhari",
  "languages": ["ar", "en", "fr"],
  "version": 999,
  "...": "...",
}
```

---

## 📜 License

See [LICENSE](LICENSE) for details.

---

## ✉️ Contact

For questions, contributions, or corrections:
[jannaty.app@gmail.com](mailto:jannaty.app@gmail.com)

---

> *“Seeking knowledge is an obligation upon every Muslim.”*
> — Hadith (Ibn Mājah)

```


```
