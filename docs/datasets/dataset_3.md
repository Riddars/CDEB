
# Dataset #3: Synergy – Toxicity of Drug, Nanoparticle, and Their Synergistic Effect on Bacterial Strains

## Original Data

**Title:** Synergy dataset – Toxicity of drug, nanoparticle, and their synergistic effect on bacterial strains  
**Description:** The dataset contains experimental data on the antibacterial activity of individual drugs, nanoparticles (NPs), and their combinations against various bacterial strains. It includes measurements of inhibition zones, MIC values, viability, and calculated synergy metrics (e.g., FIC, fold increase).  
**Total number of records:** 3226  
**Number of features (columns):** 34  
**Data type:** Mixed  
**Application:** Nanomaterials  
**Automatic validation:** Yes  

A complete data table can be found in the internal dataset file: `synergy_NeurIPS_updated_data`

---

## Data Scheme

### Synergy Dataset – Column Descriptions

| **Column Name**                            | **Description**                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| NP                                         | Name of the nanoparticle (e.g., Ag, Au, CuO).                                                                 |
| Bacteria                                   | Bacterial strain tested (e.g., *Escherichia coli*).                                                           |
| ATCC(species)                              | Strain identifier (e.g., MTCC 443, ATCC 25922).                                                               |
| NP_Synthesis                               | Synthesis method (e.g., chemical synthesis, green synthesis).                                                 |
| Drug                                       | Name of the antibiotic/drug used in combination.                                                              |
| Drug_dose                                  | Dosage/concentration of the drug.                                                                             |
| NP_concentration                           | Required NP concentration to produce an antibacterial effect.                                                 |
| NP_size_min(nm)                            | Minimum size of nanoparticles (nm).                                                                           |
| NP_size_max_(nm)                           | Maximum size of nanoparticles (nm).                                                                           |
| NP_size_avg_(nm)                           | Average size of nanoparticles (nm).                                                                           |
| shape                                      | Morphology of the nanoparticles (e.g., spherical).                                                            |
| method                                     | Assay type used (e.g., MIC, disc_diffusion, well_diffusion, etc.).                                           |
| ZOI_drug(mm)_or_Minimal_concentration      | Zone of inhibition (mm) or MIC for the drug alone.                                                            |
| error_ZOI_drug(mm)_or_Minimal_concentration| Error or standard deviation for drug-only measurement.                                                        |
| ZOI_NP_or_MC_NP                            | Zone of inhibition or MIC for the nanoparticle alone.                                                         |
| error_ZOI_NP_or_MC_NP                      | Error or standard deviation for NP-only measurement.                                                          |
| ZOI_drug_NP_or_MIC_drug_NP                 | Zone of inhibition or MIC for the drug + NP combination.                                                      |
| error_ZOI_drug_NP_or_MIC_drug_NP           | Error or standard deviation for the combination.                                                              |
| fold_increase_in_antibacterial_activity    | Enhancement in antibacterial activity due to synergy (fold change).                                           |
| Zeta_potential(mV)                         | Surface charge of the nanoparticle (mV).                                                                      |
| MDR                                        | Multidrug-resistant strain (R = Resistant).                                                                   |
| FIC                                        | Fractional Inhibitory Concentration index.                                                                    |
| Effect                                     | Type of interaction (e.g., synergistic, additive).                                                            |
| reference                                  | Citation or URL to the original publication.                                                                  |
| doi                                        | Digital Object Identifier (DOI) of the article.                                                               |
| article_list                               | Internal article identifier in the dataset.                                                                   |
| time_(hr)                                  | Duration of exposure (in hours).                                                                              |
| Coating_with_antimicrobial_peptide/polymers| Surface modification with peptides or polymers (if used).                                                     |
| combined_MIC                               | Combined MIC of NP and peptide/polymer.                                                                       |
| peptide_MIC                                | MIC of antimicrobial peptide alone.                                                                           |
| viability                                  | Bacterial viability (%) post-treatment.                                                                       |
| viability_error                            | Error or standard deviation for viability.                                                                    |

---

## Metadata

| **Column Name**      | **Description**                             |
|----------------------|---------------------------------------------|
| journal_name         | Name of the publishing journal.             |
| publisher            | Publisher of the article.                   |
| year                 | Year of publication.                        |
| title                | Title of the article.                       |
| journal_is_oa        | Journal is Open Access (TRUE/FALSE).        |
| is_oa                | Article is Open Access (TRUE/FALSE).        |
| oa_status            | Open Access status (e.g., green, closed).   |

---

> **Key Notes:**  
- **Units**: Embedded directly in column names (e.g., nm, mV, mm).  
- **Missing values**: Represented as blank cells (e.g., for Drug, peptide_MIC, etc.).  
- **Synergy metrics**: `FIC` and `fold_increase_in_antibacterial_activity` quantify interaction strength between drug and NP.  
- **MDR**: Indicates resistance status (R = Resistant).  
- **Coating**: Captures presence of peptide/polymer coatings with antimicrobial properties.

---

## Text Description

The **Synergy dataset** contains experimental data focused on evaluating the combined antibacterial effects of inorganic nanoparticles and conventional antibiotics. It includes tests performed on multiple bacterial strains, including standard and multidrug-resistant (MDR) variants.

The dataset captures:

- Physicochemical properties of nanoparticles (size, shape, zeta potential, synthesis method)
- Drug-specific details (name, dose, MIC, effect)
- Antibacterial activity metrics:  
  - Drug alone  
  - Nanoparticle alone  
  - Drug + NP combination  
- Synergy indicators (FIC, fold increase)
- Bacterial viability after treatment
- Metadata including publication source, year, and access status

This dataset is intended to support research in **nanomedicine** and **antimicrobial resistance**, particularly in the design and evaluation of **nanoparticle-drug combinations** with synergistic effects.

---

## Validation Results

Validation was performed manually using the original PDF articles located in the folder: `synergy_article_list`.

Each dataset entry was cross-checked for:

- Consistency with original source data
- Accuracy of numerical values and units (e.g., MIC, ZOI)
- Correctness of metadata (journal, DOI, title)

Validation results are contained in: `Validation_synergy_NeurIPS_updated_data`

Key fields in the validation file include:

- `verification required`
- `verified_by`
- `verification_date`
- `has_mistake_in_data`
- `has_mistake_in_metadata`
- `entry_status`

---

## Benchmark Results

???

