# A traits database for the species of macro-moth and micro-moth recorded by the Landscape-scale species monitoring of agri-environment schemes project: 2017-2021

## Overview
- A trait dataset for macro-moths and micro-moths recorded by LandSpAES (Landscape-scale Species Monitoring of Agri-environment Schemes), covering 2017–2021.
- Aims to understand how mobile moth taxa respond to local and landscape AES gradients across England.
- Data compiled from multiple published sources; broad trait coverage includes life cycle, phenology, conservation status, distribution, host plant associations, breeding habitat, and morphology.
- Not all England moth species are included; focus is on commonly recorded farmland species due to the LandSpAES survey design.

## Sampling design and scope
- Fieldwork: 6 light traps per 1 km survey square; two sampling occasions per year (one-night traps) across 54 survey squares in six National Character Areas (England).
- Timeframe: 2017–2021.
- Taxa: 925 moth species recorded on LandSpAES squares; includes many micro-moths otherwise underrepresented in farmland studies.
- Protocols: Sampling nights selected based on minimum weather requirements; moths euthanized, identified in the lab, with dissection where needed.
- Data sources: Trait data primarily from Waring & Townsend (2017) for macro-moths; Sterling & Parsons (2012) and Emmet & Heath (1991) for micro-moths; UKMoths as a supplementary source.

## Data files (Files in the repository)
- Macromoth_traits_LandSpAES_2023.csv — macro-moth trait data; 410 rows; 85 KB.
- Micromoth_traits_LandSpAES_2023.csv — micro-moth trait data; 605 rows; 180 KB.
- Moth traits_LandSpAES project_supporting information_2023.rtf — metadata on column derivations, header explanations, and references; 330 KB.
- Note: Supporting information also describes how headers map to data values and provides references used in trait collation.

## Trait data content
- Core trait categories (shared across macro- and micro-moths):
  - Life cycle ecology and phenology (timing and duration of life stages).
  - Conservation status and relative abundance.
  - Host plant specificity and host-plant characteristics (including main host species/genera and host-plant breadth).
  - Breeding habitat (broad categories and subcategories).
  - Morphological characteristics (e.g., forewing length).
  - Adult feeding and photoperiod preferences (e.g., visits to flowers, sap runs, artificial baits; diurnal/nocturnal/dawn-dusk activity; light attraction).
  - Pupal and larval/egg staging details (habitats, months of activity, overwintering stage).
  - Voltinism (north/south, single or multiple generations; seasonal variation).
- Data structure details:
  - For macro-moths: many columns describe life stages, feeding, habitat, morphology, and phenology with subcategories and month-specific indicators.
  - For micro-moths: similar trait sets, with some categories adapted to micro-moth sources; includes notes on data provenance (Emmet & Heath, Sterling & Parsons, UKMoths).
  - Monthly life-stage indicators: egg/larva/pupa/adult columns representing the 12 months (e.g., Egg_XXXX, Larva_XXXX, Pupa_XXXX, Adult_XXXX).
  - Habitat and host plant fields use 1/0 indicators across broad and specific categories (Hab_XX_XXXX, HPT_XXX, HPP_XXX, etc.).
  - Some headers and categories are merged to save space (documented in the header explanations).
- Data provenance notes:
  - Macromoth headers reference Waring & Townsend (2017); Micromoth headers reference Emmet & Heath (1991), Sterling & Parsons (2012), and UKMoths, with updates from Manley (2021).

## Data provenance and references
- Primary sources for trait derivation include:
  - Waring & Townsend (2017) for macro-moths.
  - Emmet & Heath (1991) and Sterling & Parsons (2012) for micro-moths; UKMoths as supplementary.
  - Davis (2012) and Agassiz et al. (2013) for species status and taxonomy.
- LandSpAES project final reports and project website:
  - Staley et al. (2021) on designing multi-scale survey methods.
  - Staley et al. (2022) LandSpAES final report to Natural England (LM0465).
  - LandSpAES project website: https://www.ceh.ac.uk/our-science/projects/landspaes
- Contact for queries: AESspeciesmonitoring@ceh.ac.uk

## GIS considerations and usage
- Suitable for map-based data products that encode species traits and life-history attributes alongside spatial survey data.
- Trait data are primarily presence/absence and categorical indicators, with month-by-month life-stage indicators enabling temporal spatio-temporal analyses.
- Data resolution: trait categories offer multiple subcategories (e.g., breeding habitats, host plant types) to enable different mapping scales.
- Limitations for GIS use:
  - Not exhaustively representative of all England moths; bias toward farmland species sampled in LandSpAES.
  - Some trait columns are merged or described with dense headers; careful mapping via the provided header documentation is required.
  - Micro-moth data rely on secondary sources and may have sparser coverage for certain taxa.
- Practical use in GIS:
  - Combine with LandSpAES spatial layers (survey squares, region boundaries) to map trait distributions across AES gradients.
  - Use month-specific columns to create seasonal distribution maps or to analyze phenology shifts relative to AES gradients.
  - Integrate with other environmental layers (habitat types, land-use, climate) to model associations between traits and landscape features.

## Access and contact
- Repository includes macro- and micro-moth trait CSV files and supporting information.
- For queries about the trait data or the LandSpAES project, email AESspeciesmonitoring@ceh.ac.uk or visit the LandSpAES project page and final report links provided in the document.