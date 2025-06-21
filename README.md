# RF-200

**RF-200 (ru-facts-200)**: A benchmark for fact extraction from Russian tabular data.

## Version

1.0

## Preliminaries

Source tabular data are vertically oriented tables in which the data are systematically aligned in columnar sequences. Each sequence may incorporate a descriptive label (header) to clarify its content.

**Assumption 1.** *Table headings can be multi-level and placed anywhere in the table.*

**Assumption 2.** *Source tables may not be normalized (non-relational tables).*

**Assumption 3.** *All tables are presented in Russian.*

**Assumption 4.** *All tables are manually labeled using [the Talisman framework](http://talisman.ispras.ru).*

## Directory Structure

* `csv` contains an original set of tables in the CSV format, selected from a large-scale [Russian Web Tables (RWT)](https://gitlab.com/unidata-labs/ru-wiki-tables-dataset) corpus;
* `docx` contains an original set of tables in the DOCX format;
* `json` contains labeled tables in the JSON format;
* `jsonline` contains labeled tables in the JSONL (JSON Lines) format (each table separately and collected together).

## Usage

**RF-200 (ru-facts-200)** can be used to test the performance of systems for extracting facts (entities, their characteristics, relationships between entities, and relationship characteristics) from tabular data. Precision, recall and F1-score are used as evaluation metrics.

## Author

* [Nikita O. Dorodnykh](mailto:tualatin32@mail.ru)