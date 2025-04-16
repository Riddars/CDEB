# Dataset #1: Cytotoxicity of Inorganic Nanoparticles

## Original Data

**Title:** Cytotoxicity dataset of inorganic nanoparticles
**Description:** The dataset contains information on the toxicity of inorganic nanoparticles on various normal and cancer cell lines.
**Total number of records:** 5535
**Number of features (columns):** 28
**Data type:** Mixed.
**Application:** Nanomaterials
**Automatic validation:** Yes

A complete data table can be found [link](https://docs.google.com/spreadsheets/d/1zKqCr8AxzeklouSQJ2-SZwB2Snmkpii3tYtIC1rmjE4/edit?gid=645671462#gid=645671462)

## Data Scheme

Below is a description of all the fields present in the dataset:

# Cytotoxicity Dataset – Column Descriptions

| **Column Name**             | **Description**                                                                 |
|----------------------------|---------------------------------------------------------------------------------|
| material                   | Composition of the nanoparticle/material tested (e.g., SiO₂, Ag).              |
| shape                      | Physical shape of the particle (e.g., Sphere, Rod).                            |
| coat/functional group      | Surface coating or functionalization (e.g., CTAB, PEG).                        |
| synthesis method           | Synthesis method (e.g., Precipitation, Commercial etc.).                       |
| surface charge             | Reported surface charge (e.g., Negative, Positive).                            |
| size in medium (nm)        | Hydrodynamic size in biological medium (nm).                                   |
| zeta in medium (mV)        | Zeta potential in medium (mV; blank if not measured).                          |
| no of cells (cells/well)   | Cell density per well in the assay.                                            |
| human/animal               | Origin of cells (A = Animal, H = Human).                                       |
| cell source                | Species/organism (e.g., Rat, Human).                                           |
| cell tissue                | Tissue origin of the cell line (e.g., Adrenal Gland, Lung).                    |
| cell morphology            | Cell shape (e.g., Irregular, Epithelial).                                      |
| cell age                   | Developmental stage of cells (e.g., Adult, Embryonic).                         |
| time (hr)                  | Exposure duration (hours).                                                     |
| concentration              | Tested concentration of the material (unit-specific, e.g., µg/mL).            |
| test                       | Cytotoxicity assay type (e.g., MTT, LDH).                                      |
| test indicator             | Reagent measured (e.g., TetrazoliumSalt for MTT).                              |
| viability (%)              | Cell viability percentage relative to control.                                 |
| doi                        | Digital Object Identifier (DOI) of the article.                                |
| article_list               | Identifier for the article in the dataset.                                     |
| core size (nm)             | Primary particle size (nm).                                                    |
| Hydrodynamic diameter (nm) | Size in solution including coatings (nm).                                      |
| Zeta potential (mV)        | Surface charge in solution (mV).                                               |
| Cell type                  | Specific cell line name (e.g., PC12, A549).                                    |

## Metadata

| **Column Name**   | **Description**                                                            |
|------------------|----------------------------------------------------------------------------|
| journal_name     | Name of the publishing journal.                                            |
| publisher        | Publisher of the article.                                                  |
| year             | Year of publication.                                                       |
| title            | Title of the article.                                                      |
| journal_is_oa    | Journal is Open Access (TRUE/FALSE).                                       |
| is_oa            | Article is Open Access (TRUE/FALSE; note typo "FASLE" in sample).          |
| oa_status        | Open Access status (e.g., hybrid, gold, closed).                           |

> **Key Notes:**
Data conventions:  
human/animal: "A" for Animal, "H" for Human.  
viability (%): Values >100% may indicate proliferation stimulation.  
Blanks: Missing values (e.g., zeta in medium) imply unreported data.  

## Text Description

Dataset contains experimental data on the effects of inorganic nanoparticles on human and animal cells. The main focus is on the assessment of cytotoxicity using standard tests (e.g. MTT) to understand how different nanoparticle characteristics (shape, size, charge, coating) affect cell survival.

Each entry includes:

- Nanoparticle characteristics (material, shape, size, charge, etc.)
- Cell line information (source, tissue, morphology, etc.)
- Experimental conditions (exposure time, concentration, etc.)
- Results of cell survival tests
- Publication metadata (DOI, journal, year, etc.)

The aim of the dataset is to contribute to the investigation of the patterns between nanoparticle parameters and their cytotoxic effects.

## Validation Results

Validation was performed manually using PDF versions of the publications. For each record, the following were checked:

- Data consistency with the original article
- Correctness of numerical values and units of measurement
- Presence and accuracy of fields such as "cell tissue", "cell morphology", "Hydrodynamic diameter", etc.

The validation table is available [link](https://docs.google.com/spreadsheets/d/17JoF-tsMeegV30Q7neU7LaseNscIFndcZjqsxANZzOg/edit?gid=645671462#gid=645671462).

## Benchmark Results
???
---
