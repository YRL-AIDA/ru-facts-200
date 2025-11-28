# <center> :rocket: RF-200 </center>

**RF-200 (ru-facts-200)**: A benchmark for fact extraction from Russian tabular data.

## Version

1.0

## Preliminaries

Source tabular data are vertically oriented tables in which the data are systematically aligned in columnar sequences. Each sequence may incorporate a descriptive label (header) to clarify its content.

**Assumption 1.** *Table headings can be multi-level and placed anywhere in the table.*

**Assumption 2.** *Source tables may not be normalized (non-relational tables).*

**Assumption 3.** *All tables are presented in Russian.*

**Assumption 4.** *Tables are manually labeled using [the Talisman framework](http://talisman.ispras.ru).*

## Directory Structure

* `annotations` contains all semantic annotations from a target knowledge base in the form of dictionaries (type id - type name);
* `config` contains config files with labeled table headers for each domain;
* `csv` contains an original set of tables in the CSV format, selected from a large-scale [Russian Web Tables (RWT)](https://gitlab.com/unidata-labs/ru-wiki-tables-dataset) corpus. All tables are divided into *26* domains and placed in separate folders. The `all-tables` folder contains all *225* tables;
* `documentations` contains reports with the description of created dataset and evaluation results;
* `docx` contains an original set of tables in the DOCX format. All tables are also divided into *26* domains and placed in separate folders;
* `json` contains labeled tables in the JSON format. Only *200* tables out of *225* are labeled up;
* `jsonline` contains labeled tables in the JSONL (JSON Lines) format (each table separately and collected together).

**NOTE:** *Not all source tables could be labeled up. List of unlabeled tables from which facts cannot be extracted:*

* `7_cinema_table`;
* `14_cinema_table`;
* `3_film_awards_table`;
* `5_film_awards_table`;
* `10_film_awards_table`;
* `8_locations_table`;
* `3_music_table`;
* `5_music_table`;
* `6_music_table`;
* `5_politics_table`;
* `3_sports_table`;
* `5_sports_table`;
* `6_sports_table`;
* `1_tv_hows_table`;
* `2_tv_hows_table`;
* `3_tv_hows_table`;
* `2_finance_table`;
* `3_finance_table`;
* `4_finance_table`;
* `5_finance_table`;
* `1_energy_table`;
* `2_energy_table`;
* `3_energy_table`;
* `4_energy_table`;
* `6_energy_table`.

## Usage

**RF-200 (ru-facts-200)** can be used to test the performance of systems for extracting facts (entities, their characteristics, relationships between entities, and relationship characteristics) from tabular data. *Precision*, *Recall* and *F1 score* are used as main evaluation metrics.

## Author

* [Nikita O. Dorodnykh](mailto:tualatin32@mail.ru)

## References

- Дородных Н.О., Юрин А.Ю. Набор табличных данных RF-200 и тестирование производительности извлечения фактов из русскоязычных таблиц // Труды Института системного программирования РАН. 2025. Том 37, Вып. 5. С. 205-224. DOI: 10.15514/ISPRAS-2025-37(5)-16