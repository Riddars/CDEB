
### Dataset #8: Eye Drops

---

### Original Data

- **Title:** Eye Drops  
- **Description:**  
  The dataset contains data on the corneal permeability of small molecules represented in SMILES format. The compounds are primarily pharmaceutical substances, and the dataset was compiled to support the development of predictive models for corneal permeability – a key factor in ophthalmic drug delivery.  

- **Total number of records:** 163  
- **Number of features (columns):** 2 (main extracted features: permeability and logP)  
- **Data type:** Tables  
- **Application:** Small molecules  
- **Automatic validation:** Yes  


---

### Data Scheme

#### Dataset – Column Descriptions

| Column Name            | Description                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------|
| smiles                  | SMILES of the compound. Not directly extracted from the article; manually drawn and curated. |
| name                    | Name of the compound (e.g., 4-Chlorobenzensulfonamide, Acebutolol).                         |
| perm (cm/s)             | Corneal permeability. Extracted directly when available, or calculated from logP.           |
| logP                    | Logarithm of permeability. Extracted when available, or calculated from permeability.       |
| doi                     | DOI of the article (if available).                                                          |
| PMID                    | PubMed ID of the article.                                                                   |
| title                   | Title of the article.                                                                       |
| publisher               | Publisher of the article.                                                                   |
| year                    | Year of publication.                                                                        |
| access                  | 1 – open access; 0 – closed access.                                                         |
| page                    | Page number where the data was located.                                                     |
| origin                  | Source of the data in the article (e.g., table 3).                                          |
| verification_required   | TRUE/FALSE – whether the entry required manual verification.                                |
| verified_by             | Name of the person who verified the entry.                                                  |
| verification_date       | Date of verification.                                                                       |
| has_mistake_in_data     | TRUE/FALSE – whether a mistake was found in the data.                                       |
| has_mistake_in_metadata | TRUE/FALSE – whether a mistake was found in the metadata.                                   |
| entry_status            | Status of the entry (e.g., Verified).                                                       |

---

### Metadata

| Column Name     | Description                                         |
|------------------|-----------------------------------------------------|
| doi              | DOI of the article (if available)                  |
| PMID             | PubMed ID of the article                           |
| title            | Title of the publication                           |
| publisher        | Name of the publisher                              |
| year             | Year of publication                                |
| access           | Open access (1) or not (0)                         |
| page             | Page number where the data is located              |
| origin           | Source location within the article (e.g., table 3) |

---

### Key Notes

– **Objective:** Extraction and structuring of corneal permeability data for small molecules used in ophthalmology  
– **Extracted entities:**  
  • SMILES of compound  
  • Corneal permeability (`perm (cm/s)`)  
  • Logarithm of permeability (`logP`)  
– **SMILES were not directly extracted from the articles** – they were drawn manually based on compound names and additional table information  
– Additional metadata is included to support traceability (e.g., PMID, DOI, title, publisher, year)  
– Validation includes manual verification and error flagging for both data and metadata

---

### Text Description

The Eye Drops dataset compiles structured data on the corneal permeability of pharmaceutical compounds, which is a critical property for evaluating the effectiveness of topical ophthalmic drugs. The dataset includes 163 entries, each representing a distinct compound. For each entry, the SMILES structure, compound name, permeability (in cm/s), and logP are recorded.  

SMILES structures were obtained manually based on compound names presented in the articles, especially when names were incomplete or represented as derivatives. Where only logP or permeability values were available, the corresponding missing value was calculated.  

Comprehensive metadata is provided for each entry, including bibliographic details (e.g., title, publisher, year, access type, page, and origin of data). Each entry has been manually reviewed and verified where necessary, with flags indicating any errors found in content or metadata.

---

### Validation Results

**Validation process description:**  
- Manual drawing and curation of SMILES structures based on compound names and supplementary information in the articles  
- Cross-checking of permeability/logP values and recalculation where needed  
- Manual verification of each entry by a designated validator (Xenia), including:  
  • Verification of chemical structure accuracy  
  • Accuracy of permeability and logP values  
  • Verification of bibliographic metadata  
- Error flags (`has_mistake_in_data`, `has_mistake_in_metadata`) used to track issues  
- Verification status (`Verified`) and date recorded  



---

### Benchmark Results

 ??
---
