# Dataset #4: Nanozymes – Catalytic Properties of Nanozyme Materials

## Original Data

**Title:** Nanozymes dataset – Comprehensive information about nanozyme materials and their catalytic activity  
**Description:** This dataset captures essential experimental information on nanozymes, including their chemical composition, structural and morphological properties, catalytic behavior, and reaction conditions. Data was manually extracted from scientific publications, with each row representing a unique experimental setup or measurement. The dataset supports the exploration of structure–activity relationships and benchmarking of nanozyme performance under varying conditions.  
**Total number of records:** 1133  
**Number of features (columns):** 20  
**Data type:** Mixed  
**Application:** Nanomaterials  
**Automatic validation:** No  

A complete data table can be found in the file: `nanozymes_benchmark.csv`

---

## Data Scheme

### Nanozymes Dataset – Column Descriptions

| **Column Name**            | **Description**                                                                 |
|----------------------------|---------------------------------------------------------------------------------|
| formula                    | Chemical formula of the nanozyme (e.g., Fe₃O₄, CeO₂, Au, etc.)                  |
| activity_type              | Type of catalytic activity (e.g., peroxidase-like, oxidase-like, catalase-like) |
| syngony                    | Crystal system (e.g., cubic, hexagonal, monoclinic)                             |
| length(nm)                 | Length of the nanoparticle (in nanometers)                                      |
| width(nm)                  | Width of the nanoparticle (in nanometers)                                       |
| depth(nm)                  | Depth/thickness of the nanoparticle (in nanometers)                             |
| surface                    | Surface modification or functionalization (e.g., PVP, PEG, doping)              |
| km_value                   | Michaelis constant (Km) value                                                   |
| km_unit                    | Unit of Km (e.g., mM, µM)                                                       |
| vmax_value                 | Maximum reaction rate (Vmax) value                                              |
| vmax_unit                  | Unit of Vmax (e.g., mM/s, µM/min)                                               |
| reaction_type              | Catalyzed reaction type (e.g., TMB + H₂O₂, ABTS, OPD + H₂O₂)                    |
| c_min(mM)                  | Minimum substrate concentration (mM)                                            |
| c_max(mM)                  | Maximum substrate concentration (mM)                                            |
| c_const_value              | Constant concentration of a co-substrate (if used)                             |
| c_const_unit               | Unit of the co-substrate concentration                                          |
| ccat_value                 | Catalyst (nanozyme) concentration                                               |
| ccat_unit                  | Unit of catalyst concentration (e.g., mg/mL, mM)                                |
| ph                         | pH at which the reaction was performed                                          |
| temperature                | Temperature in °C at which the reaction was performed                           |

---

## Metadata

| **Column Name**   | **Description**                                             |
|------------------|-------------------------------------------------------------|
| doi              | Digital Object Identifier of the article                    |
| title            | Title of the article                                        |
| journal          | Name of the publishing journal                              |
| oa               | Open Access status of the article (TRUE/FALSE)              |
| year             | Year of publication                                         |

---

> **Key Notes:**  
- **Units**: All concentration- and activity-related units are embedded directly in column names or represented in separate "unit" columns.  
- **Surface**: If blank, indicates no surface modification or not reported.  
- **Missing values**: Parameters not provided in an article are left blank in the dataset.  
- Each row corresponds to a distinct experiment (not just a unique article).  
- Dataset is intended for benchmarking and structure–activity analysis of nanozymes.

---

## Text Description

The **Nanozymes dataset** aggregates detailed experimental measurements related to the catalytic properties of synthetic enzyme-mimicking nanoparticles (nanozymes). These materials mimic natural enzymes and are used in biosensing, environmental detection, and therapeutic applications.

For each experiment, the dataset captures:

- **Composition and structure**: including chemical formula and crystal system (syngony)
- **Morphology**: dimensions of the particles (length, width, depth)
- **Surface chemistry**: coating or functional groups, if present
- **Catalytic performance**: Michaelis constant (Km), maximum reaction rate (Vmax), type of catalytic reaction
- **Reaction conditions**: substrate concentrations, catalyst concentration, pH, temperature

The dataset supports comprehensive **benchmarking of nanozyme activity** and deeper investigation into **structure–function relationships**. It also facilitates **machine learning** and **data-driven modeling** in nanozyme design.

---

## Validation Results

???

---

## Benchmark Results

???
