

# Dataset #2: SelTox – Toxicity of Inorganic Nanoparticles on Bacteria

## Original Data

**Title:** SelTox dataset – Toxicity of inorganic nanoparticles in various normal and pathogenic bacterial strains  
**Description:** The dataset contains experimental information on the toxicity of inorganic nanoparticles tested against different bacterial strains, including both normal and multidrug-resistant (MDR) types.  
**Total number of records:** 3286  
**Number of features (columns):** 30  
**Data type:** Mixed  
**Application:** Nanomaterials  
**Automatic validation:** Yes  

A complete data table can be found in the internal dataset file: `SelTox_NeurIPS_updated_data`

---

## Data Scheme

### SelTox Dataset – Column Descriptions

| **Column Name**               | **Description**                                                                 |
|------------------------------|---------------------------------------------------------------------------------|
| np                           | Name of the nanoparticle (e.g., Ag, Au, ZnO).                                  |
| coating                      | Surface coating/modification of the nanoparticle (if any: 1 = Yes, 0 = No).     |
| bacteria                     | Bacterial strain tested (e.g., *Enterococcus faecalis*, *Escherichia coli*).   |
| mdr                          | Indicates multidrug-resistant strain (1 = Yes, 0 = No).                         |
| strain                       | Specific strain identifier (if provided).                                      |
| np_synthesis                 | Synthesis method (e.g., green_synthesis, chemical synthesis).                   |
| method                       | Assay type (e.g., MIC, ZOI).                                                   |
| MIC_NP                       | Minimum Inhibitory Concentration of the nanoparticle.                          |
| concentration                | Concentration of nanoparticle used for ZOI measurement.                        |
| zoi_np                       | Zone of Inhibition (in mm) for the nanoparticle alone.                         |
| np_size_min (nm)             | Minimum particle size (nm).                                                    |
| np_size_max (nm)             | Maximum particle size (nm).                                                    |
| np_size_avg (nm)             | Average particle size (nm).                                                    |
| shape                        | Particle morphology (e.g., spherical, rod-shaped).                             |
| time_set                     | Duration of the experiment (in hours).                                         |
| zeta_potential               | Zeta potential (mV); blank if not measured.                                    |
| reference                    | Reference to study (URL or citation).                                          |
| doi                          | Digital Object Identifier of the article.                                      |
| article_list                 | Internal article identifier in dataset.                                        |
| Solvent for extract          | Solvent used in green synthesis (e.g., water, ethanol).                        |
| Temperature for extract, C   | Temperature of extract preparation (°C).                                       |
| Duration preparing extract, min | Duration of extract preparation (minutes).                              |
| Precursor of NP              | Chemical precursor used (e.g., AgNO₃).                                         |
| Concentration of precursor (mM) | Molar concentration of precursor.                                         |
| hydrodynamic diameter        | Hydrodynamic size in solution (if measured).                                   |
| pH during synthesis          | pH value during synthesis (if reported).                                       |

---

## Metadata

| **Column Name**    | **Description**                                      |
|--------------------|------------------------------------------------------|
| journal_name       | Name of the publishing journal.                      |
| publisher          | Publisher of the article.                            |
| year               | Year of publication.                                 |
| title              | Title of the article.                                |
| journal_is_oa      | Journal is Open Access (TRUE/FALSE).                 |
| is_oa              | Article is Open Access (TRUE/FALSE).                 |
| oa_status          | Open Access status (e.g., green, hybrid, closed).    |

---

> **Key Notes:**  
- `mdr`: 1 = Multidrug-resistant strain, 0 = Non-resistant.  
- Units are embedded in column names (e.g., nm, mM, °C, mm).  
- Fields like `strain`, `zeta_potential`, `hydrodynamic diameter` may be blank if data is not reported.  
- Coating: "0" means no coating, "1" means coating present.  
- Validation and verification were conducted based on original articles in PDF format.

---

## Text Description

The SelTox dataset provides detailed experimental data on the antibacterial activity of inorganic nanoparticles against both normal and multidrug-resistant bacterial strains. It captures key physicochemical properties of nanoparticles (e.g., size, shape, synthesis method), assay conditions (e.g., MIC, ZOI), and biological targets (bacterial species and resistance status).

Each record includes:

- Nanoparticle specifications (material, synthesis method, size, zeta potential)
- Biological target information (bacterial species, MDR status)
- Assay type and result (MIC, ZOI)
- Conditions of synthesis (e.g., solvent, temperature, pH)
- Metadata and publication references (DOI, journal, year, etc.)

The goal of the dataset is to support research in nanotoxicology by enabling analysis of how nanoparticle characteristics correlate with antibacterial efficacy, particularly against drug-resistant strains.

---

## Validation Results

Validation was carried out manually using the original PDF articles available in the folder `seltox_article_list(only)`. Each record was cross-checked against the article to verify:

- Numerical accuracy (e.g., MIC values, nanoparticle sizes)
- Correctness of units and synthesis parameters
- Completeness of metadata (title, journal, DOI)

The validation results are documented in the file: `Validation_SelTox_NeurIPS_updated_data`

Key columns in the validation table include:

- `verification required`
- `verified_by`
- `verification_date`
- `has_mistake_in_data`
- `has_mistake_in_metadata`
- `entry_status` (e.g., Requires correction)

Example of issues flagged:
- Entry 2897 marked as `Requires correction` due to mistakes in data.
- All validation entries include timestamp and verifier name.

---

## Benchmark Results

???

---
