# Dataset #6: Oxazolidinone antibiotics

## Original Data

**Title:**  
Oxazolidinone antibiotics

**Description:**  
The dataset contains oxazolidinone antibiotics represented in SMILES format, along with their corresponding inhibitory concentrations (MIC or pMIC) against various bacterial strains. The data was extracted from scientific publications and includes detailed metadata about each measurement's origin, such as source (text, table, figure, or image) and exact location in the article (page, section, subsection).

**Total number of records:**  
3103

**Number of features (columns):**  
34

**Data type:**  
Mixed (text, numeric, chemical structures)

**Application:**  
Extraction of chemical structures and biological activity data for QSAR modeling and analysis of antibiotic effectiveness.

**Automatic validation:**  
Yes

[Link to full data table: `oxazo_dataset.xlsx`]

---

## Data Scheme

### Dataset – Column Descriptions

| **Column Name**      | **Description**                                                                 |
|----------------------|---------------------------------------------------------------------------------|
| smiles               | Extracted chemical structure in isomeric SMILES format                         |
| doi                  | DOI of the source article                                                      |
| title                | Title of the article                                                           |
| publisher            | Publisher of the article                                                       |
| year                 | Publication year                                                               |
| access               | Access type (1 = open access, 0 = not open access)                             |
| compound_id          | ID of the chemical compound in the article                                     |
| target_type          | Extracted target type (e.g., MIC, pMIC)                                        |
| target_relation      | Symbol preceding the target value (e.g., =, >, <)                              |
| target_value         | Numerical value of the target measurement                                      |
| target_units         | Units of the target value (e.g., mol/l)                                        |
| bacteria             | Bacterial species related to the measurement                                   |
| bacteria_name_unified| Unified name of the bacteria (normalized nomenclature)                         |
| bacteria_info        | Additional information about the bacterial strain                              |
| page_bacteria        | Page number where the bacterial name is found in the article                   |
| origin_bacteria      | Source of the bacterial name (e.g., table, figure, text)                       |
| section_bacteria     | Section of the article where the bacteria is mentioned (if origin is text)     |
| subsection_bacteria  | Subsection of the article (if origin is text)                                  |
| page_target          | Page number where the target value is found                                    |
| origin_target        | Source of the target value (e.g., table, figure, text)                         |
| section_target       | Section of the article where the target is mentioned (if origin is text)       |
| subsection_target    | Subsection of the article (if origin is text)                                  |
| column_prop          | Not specified, possibly related to table column (empty in provided rows)       |
| line_prop            | Not specified, possibly related to table row (empty in provided rows)          |
| page_scaffold        | Page number of the scaffold or full structure in the article                   |
| origin_scaffold      | Source of the scaffold (e.g., table, figure, image)                            |
| section_scaffold     | Section of the article for scaffold (if origin is image)                       |
| subsection_scaffold  | Subsection of the article for scaffold (if applicable)                         |
| page_residue         | Page number of substituents for the scaffold                                   |
| origin_residue       | Source of the substituents (e.g., table, figure, image)                        |
| section_residue      | Section of the article for substituents (if origin is image)                   |

---

## Metadata

| **Column Name**         | **Description**                                           |
|-------------------------|-----------------------------------------------------------|
| verification_required   | Whether the record required manual verification           |
| verified_by             | Name of the person who verified the data                  |
| verification_date       | Date when the verification was completed                  |
| has_mistake_in_data     | Indicates if the chemical/biological data had a mistake   |
| has_mistake_in_matadata | Indicates if the metadata had a mistake                   |

> **Key Notes:**  
– The dataset includes both full molecular structures and scaffold + substituent representations.  
– Target values are reported as MIC or pMIC, with associated units and inequality relations.  
– Metadata provides granular information about the source and location of the extracted data within scientific publications.

---

## Text Description

**Task:**  
Extraction of chemical structures of antibiotics from the oxazolidinone class and their corresponding minimal inhibitory concentrations (MIC, target values) against various bacterial species.

**Extracted Entities:**  
- **SMILES molecules** (column `smiles`, plus all columns containing `scaffold` and `residue`) – the molecule may be represented as a whole (metadata in `scaffold` columns) or as a scaffold with substituents (metadata in both `scaffold` and `residue` columns).  
- **Target values** (all columns with the word `target`) – MIC or pMIC values measured for specific bacterial strains.  
- **Bacteria** (all columns with the word `bacteria`) – species for which the target value was measured.

**Metadata:**  
- **Article information**: `doi`, `publisher`, `title`, `year`, `access`  
- **Page**: Page numbers in the article where data was extracted from  
- **Origin**: Source type – table (with number), figure (with number), text, image (unnumbered figure)  
- **Section, Subsection**: If the data is extracted from text or image, the section and subsection of the article are specified

---

## Validation Results

???

---

## Benchmark Results


---
