# Data dictionary

Each object in `data/chapters.json` has:

| Field | Meaning |
| --- | --- |
| `n` | Integer chapter number, 1–81. |
| `leggeTitle` | The chapter title used in the 1891 Legge edition. It is historical metadata, not a title supplied by Lao Tzu. |
| `chinese` | Classical Chinese chapter text in simplified display characters, preserving line breaks. |
| `english` | James Legge's 1891 English translation. |
| `pairs` | Display-friendly Chinese/English pairings. They are editorial alignment units and can combine several classical lines. |

`data/topics.json` contains practical reading routes. A topic's chapter list is a navigation suggestion created for modern readers; it is not part of the classical text.
