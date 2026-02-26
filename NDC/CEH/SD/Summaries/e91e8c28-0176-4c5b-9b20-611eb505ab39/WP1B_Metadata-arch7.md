# Chemical composition of anaerobic digestate and biomass ash blends as a result of storage

## Overview
- A dataset exploring how adding biomass ash to anaerobic digestate affects nutrient stability over time, with emphasis on nitrogen and sulfur components.
- Includes time-series experiments, detailed compositional analyses, and an acidification treatment component.
- Data are suitable for GIS-enabled visualization of spatially distributed samples from UK AD plants and their temporal changes.

## Data assets and content
- Primary dataset: WP1B.csv (key file for treatments, materials, and analytical results).
- Materials analyzed:
  - Digestates from different UK industrial-scale anaerobic digestion plants (D1, D2).
  - Biomass ashes (A1, A2) with high mineral content.
  - Combined treatments (D1A1, D2A1) representing ash-amended digestates.
- Measured variables (per time point and treatment):
  - Dry solids (DS), pH
  - Total Kjeldahl Nitrogen (Total-N, both fresh and dry basis)
  - Nitrogen species: N-NO3, N-NH4
  - Nutrients: P, K, Mg, Ca, S, Cl
  - Micronutrients: Cu, Zn, Fe, Mn, Mo, B
  - Other: total N, total S, various mineral contents (mg/kg or % as appropriate)
- Treatment details:
  - Four substrates: D1, D2, D1A1, D2A1
  - Acidification factor: with or without 98% H2SO4 to target pH 5.5
  - Replicates: three sub-replicates per treatment
- Data collection:
  - Samples prepared (~9 L per treatment), stored at ~20°C
  - Time points on days 0, 1, 2, 4, 8, 16, 32, 64, 128
  - Analytical methods described (external laboratories; standard methods referenced)

## Geographic and temporal scope
- Geographic: samples sourced from multiple industrial-scale AD plants across the United Kingdom.
- Temporal: long-term storage experiment with measurements spanning up to 128 days.

## Experimental design and methods
- Design: 2x2 factorial acidification across four substrates, yielding eight treatments.
- Procedure:
  - 9 L per substrate treated with or without acid; when acidified, volume of 98% H2SO4 recorded to achieve pH 5.5.
  - Treatments subdivided into three replicates per treatment.
  - Containers stored indoors at ~20°C; subsamples collected at predefined days.
- Analytical framework:
  - Comprehensive suite including TS/DS, pH, Total-N, TS, and multiple elemental constituents.
  - Methods referenced include standard APHA methods and JAS-series analyses.
- Observations:
  - Acidification caused significant foaming; required vigorous mixing to reach target pH.
  - Foaming and agitation requirements indicate potential commercial-scale challenges for digestate acidification with ash amendments.

## Key findings relevant to nutrient dynamics
- Digestates (D1, D2) contain substantial ammonium (N-NH4) and total Kjeldahl nitrogen, with relatively low N-NO3 in some samples.
- Ash samples (A1, A2) show very high mineral contents, especially calcium and phosphorus, and different nitrogen speciation (low N-NH4 in this dataset).
- Nitrate and ammonium distributions differ between digestate and ash, with potential implications for nutrient availability and ammonia loss risk under storage and amendment.
- Acidification experiments indicate practical challenges (foaming, mixing energy) that may affect real-world applicability of ash-amended digestate storage strategies.

## Data access, attribution, and provenance
- Data access: https://doi.org/10.5285/e91e8c28-0176-4c5b-9b20-611eb505ab39
- Citation: Lag-Brotons et al. (2020). Chemical composition of anaerobic digestate and biomass ash blends as a result of storage. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/e91e8c28-01764c5b-9b20-611eb505ab39
- Authors and contact details for metadata and supplementary files are provided in the dataset description.

## GIS relevance and potential visualizations
- Spatial mapping of sample origins (UK AD plants) to show geographic distribution of digestate and ash sources.
- Temporal GIS: animated time-series visualizations of key nutrients (e.g., ammonium, nitrate, phosphorus, potassium) across days for each treatment.
- Thematic layers could include:
  - Digestate vs. ash composition contrasts (nutrient-rich ash vs. nutrient profiles in digestate).
  - Potential risk maps for ammonia volatilization under storage/storage-plus-amendment scenarios.
  - Overlay with agronomic suitability or regulatory limits for nutrient application.
- Data schema alignment: WP1B.csv provides structured treatment, material, days, and analytical results suitable for layering in GIS.

## Limitations and considerations for GIS work
- Some data points show non-detects or "<" values; need appropriate censoring or imputation rules for mapping.
- Only a subset of AD plants across the UK is represented; geospatial analyses should account for sampling coverage bias.
- The foaming phenomenon observed during acidification suggests caution when modeling real-world operational scales for acidified digestates.
- Units and measurement conventions are specified, but careful unit harmonization may be required when integrating with other datasets.

## Related metadata and references
- Data sources and standard methods cited include APHA (1999) and JAS methods for nutrient analyses.
- Supplementary metadata includes detailed sample descriptions, replicates, and treatment coding (D1, D2, D1A1, AD1A1, etc.).

## How to use this resource in GIS workflows
- Retrieve WP1B.csv and accompanying metadata for site-level and treatment-level attributes.
- Link samples to geographic coordinates of the originating AD plants to create spatial layers.
- Build time-enabled maps to visualize nutrient dynamics and the impact of ash amendments over the storage period.
- Annotate maps with notes on acidification challenges and operational considerations identified in the dataset.