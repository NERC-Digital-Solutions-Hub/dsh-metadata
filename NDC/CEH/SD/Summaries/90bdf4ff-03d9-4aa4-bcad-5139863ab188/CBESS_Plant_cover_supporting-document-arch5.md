# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) percentage cover of plant species on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset measuring the percentage cover of plant species in 1m x 1m quadrats on salt marsh sites in Essex and Morecambe Bay.
- Field campaign conducted in Winter and Summer 2013.
- Sites include Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Provides a comprehensive species list with percentage cover (and some counts) per quadrat; describes contrasting soil types (clay in Essex vs sandy in Morecambe Bay) and differing grazing regimes and inundation characteristics.

## Data scope and content
- Observational data of plant percentage cover per 1m x 1m quadrat; up to 22 quadrats per site.
- Seasonal dimension: Winter (W) and Summer (S).
- Habitat types included: Saltmarsh and Mudflat; location codes and site codes provided.
- Extensive species list (e.g., Agrostis stolonifera, Salicornia europaea, Spartina spp., Trifolium repens, Juncus spp., etc.) with fields for percentage cover and counts where applicable.
- Some non-typical saltmarsh species (e.g., Urtica dioica) and non-typical metrics flagged in the data.
- File format: Excel workbook.

## People and roles
- Staff responsible for the dataset: Hilary Ford.

## Location and sampling details
- Essex coordinates:
  - Abbotts Hall (AH): 51.783 N, 0.8667 E
  - Fingringhoe Wick (FW): 51.817 N, 0.9667 E
  - Tillingham Marshes (TM): 51.683 N, 0.9333 E
- Morecambe Bay coordinates:
  - Cartmel Sands (CS): 54.1667 N,  -3.0 W
  - Warton Sands (WS): 54.133 N, -2.8 W
  - West Plain (WP): coordinates not provided
- Location descriptions note contrasting soil types (clay in Essex; sandy in Morecambe Bay) and grazing regimes (heavy grazing by geese in Essex; intensive sheep grazing in parts of Morecambe Bay; West Plain lightly grazed).

## Data structure and file formats
- File format: Excel workbook.
- Key fields for data organization (Dataset Field Descriptions):
  - Row Number (sorting key)
  - Season (Winter W or Summer S)
  - Location (Morecambe M or Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat MF or Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1m, B: 1–10m, C: 10–100m, D: >100m)
- Species columns each contain:
  - Percentage cover (numerical)
  - Number (where applicable)
- Example species names include Agrostis stolonifera, Salicornia europaea, Spartina anglica, Triglochin maritima, Juncus spp., Potentilla annserina, and many more.
- Some metadata notes indicate variable descriptions such as “not typical saltmarsh sp” for certain entries (e.g., Urtica dioica, mosses, Bostrychia sp. / Cladophora).

## Data quality, provenance, and metadata
- Calibration procedures: None described.
- Quality control: Not documented.
- Monitoring period: Winter and Summer 2013 field campaign.
- Data provenance documented via field collection details, site descriptions, and a structured observation schema within the Excel workbook.

## Data access, use, and sharing
- Data is organized in an Excel workbook, suitable for ingestion into spreadsheets or basic GIS workflows.
- No explicit licensing, embargo, or sharing terms described in the provided text; standard Data Steward practices would prescribe clear licensing and portal upload instructions, as well as versioning and provenance.

## Data stewardship considerations and challenges
- Potential gaps in user needs alignment due to the dataset’s specificity (salt marsh plant cover across six sites and multiple species).
- Timeliness of data access: field campaign dates are 2013; ongoing updates or additions not specified.
- Consistency and interoperability: large number of species columns and non-typical species require standard taxonomic alignment; some fields indicate non-typical saltmarsh species.
- Quality assurance gaps: absence of documented QC procedures; implement data validation, taxonomic harmonization, and field-validated metadata.
- Sharing and updates: no explicit process for going to portals or handling embargoes; establish data access licenses, update procedures, and version control to facilitate reuse across systems.
- Operational challenges highlighted by the archetype: coordinating data collection across multiple sites and formats; large datasets with complex structure; ensuring metadata completeness (e.g., missing exact WP coordinates).