# <div align="center"> :rocket: Russian-Facts-200 (RF-200) </div>

**Russian-Facts-200 (RF-200)**: A novel benchmark for fact extraction from Russian tabular data.

## Version

1.0

## Preliminaries

Source tabular data are vertically oriented tables in which the data are systematically aligned in columnar sequences. Each sequence may incorporate a descriptive label (header) to clarify its content.

**Assumption 1.** *Table headings can be multi-level and placed anywhere in the table.*

**Assumption 2.** *Source tables may not be normalized (non-relational tables).*

**Assumption 3.** *All tables cover 26 domains (music, films, sports, locations, etc.) and are presented in Russian.*

**Assumption 4.** *Tables are manually labeled using [the Talisman framework](http://talisman.ispras.ru).*

## Dataset statistics

| **No. source tables** | **No. labeled tables** | **No. columns** | **Average No. columns per table** | **No. cells** | **No. empty cells** |
|-----------------------|------------------------|-----------------|-----------------------------------|---------------|---------------------|
| 225                   | 200                    | 979             | 4.8                               | 19490         | 1719                |

## Directory Structure

* `annotations` includes: 
  * `fact_extraction_task` contains semantic annotations for the task of extraction of new facts from table cells. All annotations are made on the basis of a target Talisman knowledge base, and are presented in the form of dictionaries (type id - type name);
  * `columnn_type_annotation_task` contains semantic annotations for the task of column type annotation (matching between columns and semantic or data types from a target knowledge graph). Annotations include 170 source semantic types from the DBpedia knowledge graph, and column labelings.
* `config` contains config files with labeled table headers for each domain;
* `csv` contains an original set of tables in the CSV format, selected from a large-scale [Russian Web Tables (RWT)](https://gitlab.com/unidata-labs/ru-wiki-tables-dataset) corpus. All tables are divided into *26* domains and placed in separate folders. The `all-tables` folder contains all *225* tables;
* `documentations` contains reports with the description of created dataset and evaluation results;
* `docx` contains an original set of tables in the DOCX format. All tables are also divided into *26* domains and placed in separate folders;
* `json` contains labeled tables in the JSON format. Only *200* tables out of *225* are labeled up;
* `jsonline` contains labeled tables in the JSONL (JSON Lines) format (each table separately and collected together).

**NOTE 1:** *Not all source tables could be labeled up! List of unlabeled tables from which facts cannot be extracted:*

| **Unlabeled Tables**                                                                     |
|------------------------------------------------------------------------------------------|
| `7_cinema_table`, `7_cinema_table`                                                       |
| `14_cinema_table`                                                                        |
| `3_film_awards_table`, `5_film_awards_table`, `10_film_awards_table`                     |
| `8_locations_table`                                                                      |
| `3_music_table`, `5_music_table`, `6_music_table`                                        |
| `5_politics_table`                                                                       |
| `3_sports_table`, `5_sports_table`, `6_sports_table`                                     |
| `1_tv_shows_table`, `2_tv_shows_table`, `3_tv_shows_table`                               |
| `2_finance_table`, `3_finance_table`, `4_finance_table`, `5_finance_table`               |
| `1_energy_table`, `2_energy_table`, `3_energy_table`, `4_energy_table`, `6_energy_table` |

**NOTE 2:** *Some tables may contain columns with empty or garbage cells! List of tables with empty or garbage cells:*

| **Table Name**          | **Column Index** |
|-------------------------|------------------|
| `7_motorsports_table`   | 0                |
| `1_buildings_table`     | 4                |
| `2_buildings_table`     | 7                |
| `4_buildings_table`     | 1                |
| `5_buildings_table`     | 1                |
| `7_buildings_table`     | 1                |
| `6_measurements_table`  | 1                |
| `6_history_table`       | 1                |
| `8_history_table`       | 2                |
| `9_history_table`       | 3                |
| `4_locations_table`     | 1, 8             |
| `18_locations_table`    | 9                |
| `22_locations_table`    | 3, 4, 9, 10      |
| `31_locations_table`    | 5                |
| `5_media_table`         | 2                |
| `3_nationalities_table` | 1                |
| `1_organizations_table` | 6                |
| `5_books_table`         | 3                |
| `1_politics_table`      | 0                |
| `4_politics_table`      | 0                |
| `6_politics_table`      | 2                |
| `10_politics_table`     | 0                |
| `13_politics_table`     | 0                |
| `16_politics_table`     | 1                |
| `1_wrestling_table`     | 2                |
| `8_sports_table`        | 5                |
| `10_sports_table`       | 6                |
| `11_sports_table`       | 5, 11, 14, 17    |
| `14_sports_table`       | 5                |
| `16_sports_table`       | 4                |
| `17_sports_table`       | 4                |
| `25_sports_table`       | 2                |
| `26_sports_table`       | 2                |
| `28_sports_table`       | 2                |
| `28_sports_table`       | 5                |

## Usage

**RF-200** can be used to test the performance of systems for extracting facts (entities, their characteristics, relationships between entities, and relationship characteristics) from tabular data. *Precision*, *Recall* and *F1 score* are used as main evaluation metrics.

## Author

* [Nikita O. Dorodnykh](mailto:tualatin32@mail.ru)

## References

- Дородных Н.О., Юрин А.Ю. Набор табличных данных RF-200 и тестирование производительности извлечения фактов из русскоязычных таблиц // *Труды Института системного программирования РАН*. 2025. Том 37, Вып. 5. С. 205-224. DOI: *10.15514/ISPRAS-2025-37(5)-16*