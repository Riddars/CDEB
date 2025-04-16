
### Dataset #9: Improved Photostability due to Multi-Component Crystals Formation

---

### Original Data

- **Title:** Improved Photostability due to Multi-Component Crystals Formation  
- **Description:**  
  The dataset contains information on photostable drug molecules and their multi-component crystalline forms (cocrystals or salts). For each entry, data is extracted on the drug, coformer, their molecular structures in SMILES format, the ratio in the crystal, and the change in photostability relative to the original drug.  

- **Total number of records:** 70  
- **Number of features (columns):** 7 (main extracted features)  
- **Data type:** Mixed  
- **Application:** Small molecules  
- **Automatic validation:** Yes  


---

### Data Scheme

#### Dataset – Column Descriptions

| Column Name                | Description                                                                                      |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| name cocrystal              | Name of multi-component crystal in the article                                                  |
| ratio cocrystal             | Component ratio forming the multi-component crystal                                             |
| name drug                   | Name of the drug compound                                                                        |
| SMILES drug                 | Canonical SMILES of the drug molecule                                                           |
| name coformer               | Name of the coformer used in the crystal                                                        |
| SMILES coformer             | Canonical SMILES of the coformer molecule                                                       |
| photostability change       | Description of change in photostability (e.g., increases, decreases, does not change)          |

---

#### Metadata – Article and Source Information

| Column Name        | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| pdf                 | PDF file name                                                               |
| doi                 | DOI of the publication                                                      |
| supplementary       | 0 – from main article; 1 – from supplementary materials                    |
| authors             | List of authors                                                             |
| title               | Full title of the article                                                   |
| journal             | Journal name                                                                |
| year                | Year of publication                                                         |
| open access         | 1 – open access; 0 – closed access                                          |
| page                | Page or article ID number                                                   |
| *_type file         | Source of the data (e.g., manuscript, text, figure, scheme, table)          |
| *_origin            | Location in the article (e.g., figure 1, table 2, text)                     |
| *_page              | Page number where the information is found                                 |

---

### Key Notes

– **Objective:** Extraction of chemical structures of drugs and coformers forming a multi-component crystal (cocrystal or salt), and the corresponding change in photostability of the solid form compared to the original drug.  

– **Extracted entities:**  
  • Name of cocrystal (`name cocrystal`)  
  • Component ratio (`ratio cocrystal`)  
  • Drug name and SMILES (`name drug`, `SMILES drug`)  
  • Coformer name and SMILES (`name coformer`, `SMILES coformer`)  
  • Photostability change (`photostability change`)  

– **Metadata includes:**  
  • Bibliographic information (DOI, authors, journal, title, year, open access)  
  • Source type and page (manuscript, figure, table, etc.)  
  • Supplementary material indicator  

– **Not included when:**  
  • Crystalline structure (Refcode) is not specified  
  • There are errors in data transferred from figures  
  • Photodegradation mechanism of the original molecule is not described  

---

### Text Description

This dataset focuses on the photostability of pharmaceutical molecules and the effect of forming multi-component crystals (cocrystals or salts) with coformers. Photostability is a critical property in drug formulation, as exposure to light can degrade therapeutic compounds.  

The dataset captures the relationship between the crystal form and the photostability of the drug by documenting:  
- The identity and ratio of components in the crystal  
- Molecular structures of the drug and coformer (in SMILES format)  
- Reported change in photostability compared to the original drug  

Information was extracted from peer-reviewed publications and supplementary materials. SMILES structures were taken from figures or manually interpreted based on names and structures. Each record includes a detailed citation trail (DOI, journal, authors, etc.) and data source within the article (e.g., table, figure, or text).

Manual validation flags indicate entries needing correction or further review.

---

### Validation Results

**Validation process description:**  
- Manual extraction of drug/coformer names and their SMILES from figures and text  
- Recording the component ratio and photostability change as described in the article  
- Cross-checking SMILES for accuracy and consistency  
- Flagging issues such as:  
  • Errors in SMILES (drug or coformer)  
  • Missing or inaccurate origin details  
  • Unclear photostability interpretation  

**Validation metadata includes:**  
- `verification_required`: Whether manual review was needed  
- `verified_by`: Validator's name  
- `verification_date`: Date of review  
- `has_mistake_in_data`: Whether data errors were found  
- `has_mistake_in_metadata`: Whether metadata errors were found  
- `entry_status`: Final status (e.g., Verified, Requires correction)  
- `comment`: Notes on specific issues (e.g., incorrect SMILES)


---

### Benchmark Results
???
