# Cytotoxicity Dataset

## About Dataset
This dataset contains information on the cytotoxicity of inorganic nanoparticles tested on various normal and cancer cell lines. It covers a wide range of nanoparticle characteristics, experimental conditions, and biological responses.

## Source Data  
Data were collected from scientific publications followed by manual feature extraction and verification.
Each record contains not only values for key experimental characteristics, but is also accompanied by extensive metadata about the sources.


## Field Descriptions

The dataset contains **5535 samples** and **28 extracted features**. Below is a list of key columns and their descriptions:

| Column Name                  | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| `material`                  | Composition of the nanoparticle/material tested (e.g., SiO₂, Ag).          |
| `shape`                     | Physical shape of the particle (e.g., Sphere, Rod).                        |
| `coat/functional group`     | Surface coating or functionalization (e.g., CTAB, PEG).                    |
| `synthesis method`          | Synthesis method (e.g., Precipitation, Commercial etc.).                   |
| `surface charge`            | Reported surface charge (e.g., Negative, Positive).                        |
| `size in medium (nm)`       | Hydrodynamic size in biological medium (nm).                               |
| `zeta in medium (mV)`       | Zeta potential in medium (mV; blank if not measured).                      |
| `no of cells (cells/well)`  | Cell density per well in the assay.                                        |
| `human/animal`              | Origin of cells (A = Animal, H = Human).                                   |
| `cell source`               | Species/organism (e.g., Rat, Human).                                       |
| `cell tissue`               | Tissue origin of the cell line (e.g., Adrenal Gland, Lung).               |
| `cell morphology`           | Cell shape (e.g., Irregular, Epithelial).                                  |
| `cell age`                  | Developmental stage of cells (e.g., Adult, Embryonic).                     |
| `time (hr)`                 | Exposure duration (hours).                                                 |
| `concentration`             | Tested concentration of the material (unit-specific, e.g., µg/mL).         |
| `test`                      | Cytotoxicity assay type (e.g., MTT, LDH).                                  |
| `test indicator`            | Reagent measured (e.g., TetrazoliumSalt for MTT).                          |
| `viability (%)`             | Cell viability percentage relative to control.                             |
| `doi`                       | Digital Object Identifier (DOI) of the article.                            |
| `article_list`              | Identifier for the article in the dataset.                                 |
| `core size (nm)`            | Primary particle size (nm).                                                |
| `Hydrodynamic diameter (nm)`| Size in solution including coatings (nm).                                  |
| `Zeta potential (mV)`       | Surface charge in solution (mV).                                           |
| `Cell type`                 | Specific cell line name (e.g., PC12, A549).                                |
| `journal_name`              | Name of the publishing journal.                                            |
| `publisher`                 | Publisher of the article.                                                  |
| `year`                      | Year of publication.                                                       |
| `title`                     | Title of the article.                                                      |
| `journal_is_oa`             | Journal is Open Access (TRUE/FALSE).                                       |
| `is_oa`                     | Article is Open Access (TRUE/FALSE; note typo "FASLE" in sample).          |
| `oa_status`                 | Open Access status (e.g., hybrid, gold, closed).                           |

!!! note "Key Notes"
    - `human/animal`: `"A"` indicates animal-derived cells, `"H"` indicates human-derived cells.  
    - `viability (%)`: Values greater than 100% may indicate **proliferation stimulation** rather than toxicity.  
    - Blank or missing values (e.g., for `zeta in medium (mV)`) indicate that the measurement was **not reported** in the original source.

---



### Example data
```json
{
  "material": "SiO2",
  "shape": "Sphere",
  "coat/functional group": "CTAB",
  "synthesis method": "Precipitation",
  "surface charge": "Negative",
  "size in medium (nm)": 90.09,
  "zeta in medium (mV)": null,
  "no of cells (cells/well)": 5000,
  "human/animal": "A",
  "cell source": "Rat",
  "cell tissue": "Adrenal Gland",
  "cell morphology": "Irregular",
  "cell age": "Adult",
  "time (hr)": 12,
  "concentration": 1.95,
  "test": "MTT",
  "test indicator": "TetrazoliumSalt",
  "viability (%)": 113.67,
  "doi": "10.3109/15376516.2015.1070229",
  "Cell type": "PC12",
  "journal_name": "Toxicology Mechanisms and Methods",
  "publisher": "Taylor & Francis",
  "year": 2015,
  "title": "Effect of mesoporous silica nanoparticles on cell viability and markers of oxidative stress",
  "journal_is_oa": false,
  "is_oa": false,
  "oa_status": "hybrid"
}
```
## Validation results
Валидация проводилась вручную. Также была выполнена перекрёстная проверка с оригинальными публикациями, указанными по DOI.
Численные метрики или процент ошибок не предоставлены.

## Результаты бенчмаркинга
[Производительность моделей на этом датасете]
