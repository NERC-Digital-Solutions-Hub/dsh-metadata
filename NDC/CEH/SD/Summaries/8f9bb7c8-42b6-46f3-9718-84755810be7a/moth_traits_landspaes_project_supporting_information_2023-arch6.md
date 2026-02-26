# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

## Overview
- A trait database from LandSpAES, capturing macro- and micro-moth species traits collected 2017–2021 across England to assess effects of local and landscape agri-environment schemes (AES) gradients on mobile taxa.
- Study used a pseudo-experimental design with baseline survey data across 54 survey squares in six National Character Areas, spanning arable, grassland, and upland systems.
- Data support goal: enable data discovery, combination with other datasets, and creation of user-friendly data products for broader use.

## What’s in the data
- Trait data covering moths recorded on LandSpAES survey squares (England, 2017–2021), including life cycle ecology, phenology, conservation status, distribution, host plant relationships, breeding habitat, and morphology.
- Two primary trait files:
  - Macromoth_traits_LandSpAES_2023.csv: macro-moth traits, 410 rows.
  - Micromoth_traits_LandSpAES_2023.csv: micro-moth traits, 605 rows.
- Supporting information file:
  - Moth traits_LandSpAES project_supporting information_2023.rtf: metadata on how columns were derived, data sources, and notes.
- Scope:
  - Traits compiled for the 925 moth species recorded across LandSpAES squares (note: files list a total of 410 macro and 605 micro rows; dataset represents many common farmland moths from the survey network).

## Sampling and data provenance
- Collection method: six light traps per 1 km survey square; two sampling occasions per year; nights selected for minimal weather requirements.
- Specimen handling: moths euthanized and lab-identified; targeted dissections for certain species.
- Trait derivation: collated from published and online sources with emphasis on newer references; macro data primarily from Waring & Townsend (2017), micro data from Sterling & Parsons (2012), supplemented by Emmet & Heath (1991) and UKMoths.
- Documentation: methodology and header explanations detailed in the LandSpAES final project report (Staley et al. 2022) and in the accompanying supporting information file.

## File structure and headers
- Files in the repository:
  - Macromoth_traits_LandSpAES_2023.csv: 85 KB, 410 rows.
  - Micromoth_traits_LandSpAES_2023.csv: 180 KB, 605 rows.
  - Moth traits_LandSpAES project_supporting information_2023.rtf: 330 KB.
- Header information is documented in Tables 2 and 3 within the supporting information:
  - Key fields include scientific_name, common_name, various taxonomic and project-adjacency codes, residency/immigration status, conservation and abundance references, adult feeding behaviors, photoperiod, pupal habitats, forewing measurements, voltinism, overwintering stages, and host plant data.
  - Host plants and habitats are represented with multiple columns to capture broad categories and subcategories (e.g., Hab_XX_XXXX for breeding habitats; HPT_XXX and HPP_XXX for host plant types and parts).
  - Monthly life-stage indicators exist (e.g., Egg_XXXX, Larva_XXXX, Pupa_XXXX, Adult_XXXX) to denote state by month.
  - Micromoth notes field provides supplementary species information.
- Some categories are split across many columns (e.g., 12 monthly columns for egg or larval stages) to reflect detailed temporal patterns.

## How to use this data
- Data products: trait profiles per species enabling analyses of host specificity, phenology, habitat associations, and morphological traits in relation to AES gradients.
- Supports cross-referencing with LandSpAES observational data to explore relationships between traits and responses to AES features across scales.
- Data can be combined with external datasets due to explicit provenance, references, and detailed header descriptions.

## Limitations and caveats
- The trait dataset does not cover all moth species in England; emphasis is on species common to farmland and captured by the LandSpAES sampling design.
- Data are derived from multiple literature sources with varying levels of completeness; some traits may be more robust for macro-moths than micro-moths, depending on source coverage.
- Temporal and spatial coverage tied to LandSpAES sampling design (2017–2021, 54 squares, six regions), which may influence generalisability to other landscapes or time periods.

## Access and references
- For queries about this trait data or the LandSpAES project: aespeciesmonitoring@ceh.ac.uk
- Project website: https://www.ceh.ac.uk/our-science/projects/landspaes
- Final project report: Staley et al. 2022, Landscape-scale species monitoring of agri-environment schemes (UKCEH and BTO), final report to Natural England, project LM0465
- Key literature informing trait sources: Emmet & Heath (1991); Sterling & Parsons (2012); Waring & Townsend (2017); UKMoths (www.ukmoths.org.uk).