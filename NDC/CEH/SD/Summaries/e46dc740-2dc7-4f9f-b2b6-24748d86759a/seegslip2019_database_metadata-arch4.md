# pasture fed livestock farms across Great Britain, 2019

## Overview
- Data collected by the UK Centre of Ecology & Hydrology (CEH) for a BBSRC-funded project.
- Purpose: evidence the impacts of pasture-fed livestock approaches on grassland parameters, especially sward composition and soil qualities.
- Context: grasslands are significant in the UK; Pasture Fed Livestock Association (PFLA) provides certification standards linked to biodiversity, soil health, and animal health outcomes.

## Data collection and design
- Timeframe: 2019 (sampling May–September).
- Participants: 17 farms across Great Britain, all members of PFLA; 10 fully certified, 7 with intentions to certify.
- Field design: paired fields per farm representing mob grazing vs set-stocking or contrasting ley types; some farms sampled multiple field pairs.
- Methods:
  - Vegetation: 3 random quadrats per field (2x2 m); measurements include species, cover, flowering, vegetation height, wormcasts, soil surface signs, and biomass in sub-samples.
  - Soils: 10 bulked soil samples per field via a W-shaped transect; soil cores (15 cm depth) plus additional cores for chemistry; eDNA sub-samples deposited in ENA.
  - Management: on-site farmer interviews about sward longevity, grazing type, stocking density, inputs.
- Data products: soil and vegetation data, field/farm management data, and stock information.
- Data access: anonymised farms identified by IDs; bacterial/fungal community data linked via ENA PRJEB46195.

## Data architecture and content
- Data tables (CSV, anonymised):
  - SEEGSLIP_PLOTS_2019.csv — plot-level vegetation data (farm_no, field_id, plot type, plot_number, survey dates, slope, aspect, canopy/shrub/ground heights, etc.).
  - SEEGSLIP_SPECIES_2019.csv — species-level plot data (BRC names, cover, flowering status, land classification codes, location refs).
  - SEEGSLIP_BIOMASS_2019.csv — dried biomass by Grass, Dicot, Cereal, and Total.
  - SEEGSLIP_SOIL_2019.csv — soil chemistry and physical properties across depths (pH in water/CaCl2, conductivity, moisture, LOI, bulk density, stone metrics, PSD, aggregate stability, CaCO3, TOTC/TOTN, OlsenP/TOTP).
  - SEEGSLIP_FARMDATA_2019.csv — farm-level and field-level management data (grazing type, management across fields, rest periods, fertiliser use, costs, supplementary feeding).
  - SEEGSLIP_FIELDS_2019.csv — field-level management attributes (mob grazing area, set stocking area, field size, shade, rest, sloping variables, etc.).
  - SEEGSLIP_STOCK_2019.csv — stocking information (livestock types, supplementary feeding practices, bale rolling).
- Data quality and QA:
  - LOI and other chemical analyses followed standardized CEH/A2 methods with quality controls and internal standards.
  - Laser diffraction PSD calibration and cross-checks; duplicates and blanks included for QA.
  - Some data gaps indicated by -999; notes on potential measurement limitations (e.g., organic matter interference in LD).

## Data governance and access
- Ownership and stewardship: CEH; dataset linked to BBSRC-funded research.
- Anonymisation: farms and fields anonymised with IDs to protect landowner confidentiality.
- Supplemental data: soil DNA sequences deposited in European Nucleotide Archive (ENA) under accession PRJEB46195.
- Documentation: detailed methodology and references to established soil and land classification protocols (e.g., ITE Land Classification 2007; CS soil methods).

## Data quality, limitations, and context
- Strengths:
  - Thorough field sampling design capturing grazing treatments and ley types.
  - Comprehensive soil chemistry and physical property measurements aligned with established soil manuals.
  - DNA-based soil data available for deeper ecological analyses.
- Limitations:
  - 2019 snapshot; cross-sectional across 17 farms (limited temporal coverage).
  - Some measurements have missing data (-999) and high organic matter can affect certain instruments (e.g., LD accuracy).
  - Anonymised IDs constrain direct linking to non-disclosive external datasets unless shared metadata.

## Value and applications for Data Leaders
- Systems-level insight: enables cross-farm comparisons of mob grazing versus other management strategies and their effects on sward structure and soil health.
- Data stewardship and reuse: well-structured, domain-specific dataset with clear data lineage, QA procedures, and an accompanying DNA resource; fosters best practices in metadata, discoverability, and cross-dataset integration.
- Policy and stakeholder relevance: supports evidence generation for pasture-based, biodiversity-friendly, and soil-improving farming approaches; compatible with wider grassland and land-use data networks.
- Community and collaboration: links to PFLA certification context and potential for integration with biodiversity, carbon, and soil microbiome datasets within broader data-sharing initiatives.

## Practical considerations for users
- Data format and scope: seven CSV tables covering plots, species, biomass, soil, farm data, fields, and stock; GB-wide 2019 snapshot with anonymised farm IDs.
- Metadata alignment: uses established soil classification references and land-use codes; LOI and SOC methods documented with QA steps.
- Next steps for analysts: integrate with complementary datasets (e.g., biodiversity metrics, carbon stocks), perform comparative analyses across grazing regimes, and explore soil microbiome relationships using ENA data.