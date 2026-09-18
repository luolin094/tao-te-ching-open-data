# Tao Te Ching Open Data

This repository contains a clean, chapter-indexed bilingual dataset for the 81 chapters of the *Tao Te Ching*. It is meant to be useful to researchers, educators, independent developers, language learners, and people building careful reading tools.

## Included

- `data/chapters.json`: all 81 chapters, with the Chinese text, James Legge's 1891 translation, and aligned display pairs.
- `data/topics.json`: ten practical reading paths. These are editorial navigation aids, not claims about the original text.
- `schema/chapter.schema.json`: a JSON Schema for validating chapter records.
- `metadata.json`: machine-readable provenance and file information.

The data is intentionally small and inspectable. There is no API key, tracking code, generated user profile, or hidden network call.

## Example

```js
import chapters from './data/chapters.json' with { type: 'json' };

const chapterEight = chapters.find((chapter) => chapter.n === 8);
console.log(chapterEight.leggeTitle);
console.log(chapterEight.pairs[0]);
```

## Provenance and responsible use

The Chinese text is a classical received text shown in simplified characters. The English source is James Legge's 1891 translation, which is public domain. `pairs` are presentation-oriented alignments; they should not be treated as a claim that each English sentence is a literal one-to-one translation of each Chinese line.

If you publish an interpretation, label it as an interpretation. Do not present a generated summary as an ancient quotation. See [`docs/DATA_DICTIONARY.md`](docs/DATA_DICTIONARY.md) and [`docs/SOURCES.md`](docs/SOURCES.md).

The companion reading site is [asklaotzu.com/tao](https://asklaotzu.com/tao).

For an AI-client integration, see the companion [Ask Lao Tzu MCP server](https://github.com/luolin094/ask-lao-tzu-mcp).
