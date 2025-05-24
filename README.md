# Hadith Translations JSONL

This repository contains a newline-delimited JSON file (`.jsonl`) of hadith translations with versioning. Each line is a standalone JSON object representing one hadith, with metadata and three language versions.

---

## File Format

- **Type**: JSONL (newline-delimited JSON)

Each line looks like:

```json
{
  "hadith_number":  0000,
  "arabic_number":  0000,
  "translation_version": 1,
  "reference": {
    "book":   00,
    "hadith": 00
  },
  "arabic":  "حَدَّثَنَا …",  
  "english": "Narrated …",
  "french":  "Rapporté par …"
}
````

* `hadith_number` (num): unique sequential identifier
* `arabic_number` (num): original Arabic numbering
* `translation_version` (int): increments whenever a new French correction is applied
* `reference` (object):

  * `book`   (num): which book of the collection
  * `hadith` (num): position within that book
* `arabic`  (string): original Arabic text
* `english` (string): reliable English rendering
* `french`  (string): current French translation

---

## Preview example

```jsonl
{"hadith_number":  123, "arabic_number":  123, "translation_version": 1, "reference": {"book":  1, "hadith":  5}, "arabic": "حَدَّثَنَا أَبُو...", "english": "Narrated Abu ...", "french": "Rapporté par ..."}
{"hadith_number":  124, "arabic_number":  124, "translation_version": 1, "reference": {"book":  1, "hadith":  6}, "arabic": "عَنْ عَائِشَةَ...", "english": "Narrated Aisha ...", "french": "Rapporté par Aïcha ..."}
{"hadith_number":  125, "arabic_number":  125, "translation_version": 1, "reference": {"book":  1, "hadith":  7}, "arabic": "قَالَ النَّبِيُّ...", "english": "The Prophet ﷺ said ...", "french": "Le Prophète ﷺ a dit ..."}
````
---

> *“Seeking knowledge is an obligation upon every Muslim.”*
> — Hadith (Ibn Mājah)


```
