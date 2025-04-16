

### Dataset #7: Chelate Metal Complexes

---

### Original Data

- **Title:** Chelate Metal Complexes  
- **Description:**  
  The dataset contains data on thermodynamic stability constants (lgK) of chelate complexes of gadolinium (Ga), gadolinium (Gd), technetium (Tc), lutetium (Lu), and chelating ligands. These complexes are used as diagnostic markers (contrast agents) in the diagnosis of various diseases during magnetic resonance imaging (MRI).  

- **Total number of records:** 907  
- **Number of features (columns):** 21  
- **Data type:** Mixed  
- **Application:** Small molecules  
- **Automatic validation:** Yes  

---

### Data Scheme

#### Dataset – Column Descriptions

| Column Name         | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| pdf                  | Name of the PDF file                                                        |
| doi                  | DOI of the article                                                          |
| doi_source           | If the source article is cited within a review; otherwise same as DOI       |
| supplementary        | 0 – data from article; 1 – data from supplementary materials                |
| title                | Article title                                                               |
| publisher            | Publishing organization                                                     |
| year                 | Year of publication                                                         |
| access               | 1 – open access; 0 – closed access                                          |
| compound_id          | Compound identifier in the article                                          |
| compound_name        | Name of the compound in the article                                         |
| smiles               | Extracted chemical structure in canonical SMILES format (no stereochemistry)|
| smiles_type          | Type of structure: ligand or environment                                    |
| metal                | Metal forming the complex                                                   |
| target               | Thermodynamic stability constant (lgK)                                      |
| page_smiles          | Page number with structure illustration                                     |
| origin_smiles        | Source of the structure: figure N / table N / scheme N                      |
| page_metal           | Page number with metal mention                                              |
| origin_metal         | Source of metal mention                                                     |
| page_target          | Page number with target value                                               |
| origin_target        | Source of target value: table N / section N                                 |
| verification_required| TRUE – requires manual verification                                         |

---

### Metadata

| Column Name     | Description                                         |
|------------------|-----------------------------------------------------|
| pdf              | PDF file name in the folder                        |
| doi              | Article DOI                                        |
| doi_source       | Primary DOI source                                 |
| supplementary    | Source: article (0) or supplementary materials (1) |
| title            | Article title                                      |
| publisher        | Publisher                                          |
| year             | Year of publication                                |
| access           | Access: open (1) or closed (0)                     |

---

### Key Notes

– **Objective:** Extraction of chemical structures of ligands and metals forming a chiral complex, and their corresponding thermodynamic stability constants (lgK)  
– **Extracted entities:**  
  • SMILES of ligand(s) (`smiles` column)  
  • Target value lgK (`target` column)  
  • Metal (`metal` column)  
– Structures are converted to canonical SMILES format using RDKit; stereochemistry is removed  
– Strict filtering criteria applied to structures and data quality (see constraints below)

---

### Text Description

This dataset is a structured collection of data extracted from scientific articles, containing information on the thermodynamic stability of chelate metal complexes with organic ligands. The goal is to systematize and standardize information on the stability of metal-ligand complexes that are potentially applicable in medical diagnostics, particularly in MRI imaging.  

Each record represents one complex and includes the following:  
- Ligand structure (in canonical SMILES format)  
- Metal forming the complex (e.g., Ga)  
- lgK value (stability constant)  
- Source metadata: article DOI, page numbers, tables, figures  
- Article metadata: title, publisher, year, open access status, etc.  

The data underwent automatic validation, including structural checks against inclusion criteria (e.g., no undefined radicals, bioconjugates, boron clusters, etc.), and canonicalization using RDKit.

---

### Validation Results

**Validation process description:**  
- SMILES validity checked using RDKit  
- Stereochemistry removed  
- Structural filtering applied:  
  • Must contain carbon  
  • No undefined/incomplete structures  
  • Excludes boron clusters (e.g., carboranes), bioconjugates, polymers  
  • Excludes precursors or reaction intermediates  
- Source verification (pages, tables, figures)  
- Records with `verification_required = TRUE` need additional manual validation  


---

### Benchmark Results

???
