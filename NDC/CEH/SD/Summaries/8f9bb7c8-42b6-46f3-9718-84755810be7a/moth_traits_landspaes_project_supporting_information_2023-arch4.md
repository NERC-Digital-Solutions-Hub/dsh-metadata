# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

## Overview
- Dataset of moth trait data from LandSpAES project (2017–2021) examining responses of mobile taxa to local and landscape agri-environment schemes (AES) gradients.
- Study design: pseudo-experimental, baseline survey across 54 survey squares in six English National Character Areas, spanning arable, grassland, and upland systems.
- Moths sampled with six light traps per square, surveyed twice yearly on nights meeting weather requirements; species euthanized and lab-identified, enabling inclusion of many macro- and micro-moth species.
- 925 moth species recorded on LandSpAES squares during 2017–2021; includes many micro-moths not typically covered in farmland studies.

## What is in the dataset
- Trait data for macro-moths and micro-moths, including:
  - Life cycle ecology and phenology
  - Conservation status and distribution
  - Host plant specificity and characteristics
  - Breeding habitat and morphological characteristics
  - Additional species-level metadata and trait indicators
- Data are provided in two CSV files:
  - Macromoth_traits_LandSpAES_2023.csv (410 rows; macro-moth traits)
  - Micromoth_traits_LandSpAES_2023.csv (605 rows; micro-moth traits)
- Supporting information document (Moth traits_LandSpAES project_supporting information_2023.rtf) detailing data derivation, header explanations, and sources.
- Notes on data derivation emphasize that macro-moth traits reference Waring & Townsend (2017) and micromoths draw on Sterling & Parsons (2012) with supplementary sources (Emmet & Heath 1991; UKMoths), plus other references.
- Data do not cover all England moth species; focused on common farmland species due to LandSpAES sampling framework and multi-year design.
- Header documentation includes detailed descriptions for each column and how data were derived, with explicit examples of complex headers (e.g., months represented as separate columns for life stages and flight periods).

## Data collection and provenance
- Grounded in LandSpAES project final report and associated publications:
  - Staley et al. 2021: Designing a survey to monitor multi-scale impacts of agri-environment schemes on mobile taxa
  - Staley et al. 2022: Landscape-scale species monitoring of agri-environment schemes (final report to Natural England)
- Data provenance includes multiple established field guides and checklists (e.g., Agassiz et al., Emmet & Heath, Waring & Townsend, Sterling & Parsons, UKMoths).
- The dataset explicitly documents variability in data resolution (e.g., broader categories with subcategories) and cross-referencing of host plant data and habitat classifications.

## File structure and metadata
- Repository contains three primary files:
  - Macromoth_traits_LandSpAES_2023.csv
  - Micromoth_traits_LandSpAES_2023.csv
  - Moth traits_LandSpAES project_supporting information_2023.rtf
- Each trait file includes a comprehensive header schema with species-level traits (e.g., scientific name, common name, conservation status, adult/larval flight timing, voltinism, overwintering stage, host plants, habitat/breeding habitats, forewing measurements, and host plant parts).
- Header tables (Table 2 for Macromoth and Table 3 for Micromoth) provide detailed explanations for each column, including the meaning and data sources for nested categorical variables and monthly indicators.
- Monthly indicators are stored as separate columns (e.g., Egg_XXXX, Larva_XXXX, Pupa_XXXX, Adult_XXXX) to indicate presence in a given month.
- Data quality and usage notes are included in the supporting information, with guidance on interpreting complex headers and merged fields.

## Documentation, standards, and usage notes
- Detailed metadata and column-level explanations to support data discoverability and interoperability.
- Clear description of data derivation sources and methods, enabling audit trails and reproducibility.
- Notes on limitations, including that the trait data do not cover all England moth species but cover many common farmland taxa due to study design.
- Contact information for queries on trait data or the LandSpAES project:
  - AESspeciesmonitoring@ceh.ac.uk
  - LandSpAES project website: https://www.ceh.ac.uk/our-science/projects/landspaes
  - Final project report: https://randd.defra.gov.uk/ProjectDetails?ProjectId=20012

## Access, reuse, and limitations
- Data are designed to support analyses of AES impacts on mobile taxa and can be integrated with other data systems to compare species traits with AES gradients.
- Extensive metadata facilitates reuse, including monthly life-stage indicators, host-plant relationships, morphology, and habitat associations.
- Limitations to consider:
  - Not all England moth species are represented; emphasis on farmland-associated taxa.
  - Trait data rely on published sources and field guides; some micro-moth data are less complete than macro-moth data.
  - Varied resolution across traits (some categories broad, with detailed subcategories available).

## References and contact
- References include Agassiz et al. (2013); Davis (2012); Emmet & Heath (1991); Manley (2021); Staley et al. (2021, 2022); Sterling & Parsons (2012); Waring & Townsend (2017).
- For queries about the trait data or LandSpAES:
  - AESspeciesmonitoring@ceh.ac.uk
  - LandSpAES project site: https://www.ceh.ac.uk/our-science/projects/landspaes
  - Final project report: https://randd.defra.gov.uk/ProjectDetails?ProjectId=20012