# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

- Purpose: Compile a comprehensive trait dataset for macro- and micro-moths recorded by LandSpAES to understand how mobile taxa respond to local and landscape agri-environment scheme (AES) gradients across England.
- Scope: Baseline, multi-year survey (2017–2021) across 54 1km survey squares in six National Character Areas, covering arable, grassland, and upland agricultural systems.
- Design: Novel pseudo-experimental framework to assess responses of mobile taxa to generalized AES gradients beyond farm/AEA boundaries.

## Study design and data collection

- Sampling protocol:
  - 6 light traps per survey square.
  - Moths sampled twice per year, one-night sessions per occasion.
  - Nights selected to meet minimum weather requirements.
  - Specimens euthanized and identified in the lab; dissections where needed.
- Taxa scope: Includes many farmland macro- and micro-moth species, notably several micro-moths not commonly studied in farmland ecology.
- Data sources for trait assembly:
  - Macro-moths: Waring & Townsend (2017).
  - Micro-moths: Sterling & Parsons (2012); supplemented by Emmet & Heath (1991) and UKMoths.
- Data compilation approach:
  - Traits collated from published/online sources with priority to recent sources.
  - Micro-moth data required broader reference material due to limited micro-moth data availability.

## Trait data composition

- Macro-moth traits (Macromoth_traits_LandSpAES_2023.csv):
  - Life cycle ecology and phenology; conservation status and distribution; host plant specificity and characteristics; breeding habitat; morphological traits (e.g., forewing length).
  - Data structure includes sub-categories for broader categories (e.g., habitat) to provide different resolution levels.
  - Example headers cover: scientific name, common name, status, adult feeding behaviours, photoperiod activity, overwintering stages, voltinism, host plants (types and specific species), breeding habitats, forewing measurements, and monthly activity indicators.
- Micro-moth traits (Micromoth_traits_LandSpAES_2023.csv):
  - Similar trait categories as macro-moths: life cycle, status and abundance, host plant specificity, breeding habitat, morphology.
  - Monthly and stage-specific presence indicators (egg, larva, pupa, adult) distributed across 12 months; includes overwintering stages and host plant context.
- Headers and data structure:
  - Tables detail column headers and the source of each data element.
  - Some categories are represented by multiple columns (e.g., monthly presence across 12 months).
  - Host plant data include broad categories and specific main host plants; host part data; habitat/breeding categories with both broad and subcategories.
- Supporting information:
  - Moth traits_LandSpAES project_supporting information_2023.rtf provides metadata on how each column was derived, numbering criteria, and a list of references.

## Files included

- Macromoth_traits_LandSpAES_2023.csv: Macro-moth traits for 410 rows.
- Micromoth_traits_LandSpAES_2023.csv: Micro-moth traits for 605 rows.
- Moth traits_LandSpAES project_supporting information_2023.rt f: Metadata, column derivation, and references.
- Note: The dataset notes that it does not cover all English moth species but focuses on many common farmland species due to the LandSpAES sampling design.

## Metadata, provenance and references

- Primary data provenance:
  - LandSpAES project final report (Staley et al. 2022) and final methodology papers (Staley et al. 2021) informing the sampling design and AES gradient framework.
- Key references used for trait data:
  - Macro-moths: Waring & Townsend (2017).
  - Micro-moths: Sterling & Parsons (2012); Emmet & Heath (1991); UKMoths.
  - Supporting biodiversity and moth guides: Agassiz et al. (2013); Davis (2012); Manley (2021).
- Contact and access:
  - For queries about the trait data or LandSpAES: AESspeciesmonitoring@ceh.ac.uk
  - LandSpAES project website: https://www.ceh.ac.uk/our-science/projects/landspaes
  - Final project report: https://randd.defra.gov.uk/ProjectDetails?ProjectId=20012

## Usage, limitations and relevance for environmental monitoring

- Relevance for analysts:
  - Enables cross-species trait analyses to interpret responses of mobile moth taxa to AES gradients across landscapes.
  - Supports integration with other environmental datasets to explore ecosystem responses to agri-environment schemes.
- Limitations:
  - Not exhaustive of all English moths; biased toward common farmland species due to the LandSpAES sampling design and geographic coverage.
  - Trait data are compiled from published sources; some micro-moth data rely on older or less comprehensive references.
- Data structure implications:
  - Rich, multi-resolution trait data with detailed headers; requires careful handling of monthly stage indicators and host-plant categorizations for analyses.
- Potential applications:
  - Monitoring and policy evaluation of AES performance on mobile taxa.
  - Comparative analyses with other taxa or datasets to assess landscape-scale AES impacts.