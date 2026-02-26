# Metadata for datasets available from Chaplow et al. (2015): Chaplow, J.S., Beresford, N.A., Barnett, C.L. (2015). Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain. NERC Environmental Information Data Centre.

## Overview
- Metadata describing five CSV datasets of post-Chernobyl radiocaesium measurements across Great Britain.
- Datasets span 1986–1997 and cover soil, vegetation, wildlife, and fungi.
- Data collected to assess uptake and transfer of radiocaesium in terrestrial ecosystems, with associated soil and habitat context.

## Datasets
- 1_Post_Chernobyl_survey_data_radiocaesium_in_soil_vegetation_wildlife_1986_and_1987.csv
  - GB-wide survey of Chernobyl fallout in graminaceous vegetation; sampling in May–June 1986, re-surveys Oct 1986 and spring 1987; includes soil, vegetation types, and wildlife samples.
- 2_Post_Chernobyl_survey_data_radiocaesium_in_vegetation_1986_1987_1988.csv
  - Radiocaesium in vegetation sampled in Cumbria (1986), north Wales (1987), and north Yorkshire (1988).
- 3_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1989_and_1990.csv
  - Soil and vegetation sampling at three sites in Cumbria (1989–1990).
- 4_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1992.csv
  - Soil and vegetation results from grazing areas of three upland sheep flocks in Cumbria (1992).
- 5_Post_Chernobyl_survey_data radiocaesium in fungi 1994 to 1997.csv
  - Fungi and associated soil sampled across Great Britain (autumn 1994–spring 1997).

## Measurements and units
- Primary radionuclides: Cs-134 and Cs-137 activity concentrations.
  - Reported in Bq/kg dry matter (DM) for soils and vegetation.
  - Cs-134/137 deposits reported in Bq/m² where applicable.
- Additional field measurements and derived metrics included:
  - Wet and dry weights of vegetation; fresh/flesh contents for wildlife samples.
  - Soil layers: 0–4 cm topsoil, with separate measurements for upper/lower layers; <2 mm fraction gamma analyses.
  - Other radionuclides and soil/biomass properties appear in extended fields (e.g., K-40, Ru-103, Ru-106, Cs-137 in various matrices, LOI, pH, texture, bulk density, etc.).
- Structural metadata fields provide mappings to internal codes and site identifiers (CEH/ITE codes).

## Sampling and laboratory methods
- Vegetation sampling:
  - Graminaceous plants clipped from 1 m² plots to within 1 cm of soil.
  - Grass/Heather categories in some datasets; samples oven-dried (typical 60–85°C range depending on protocol) and ground for analysis.
- Soil sampling:
  - 20 cm × 20 cm × 15 cm samples collected; litter layer separated if present.
  - Soils characterized for pH, texture, organic matter; bulk density measured; samples dried and sieved (<2 mm fraction) for gamma spectrometry.
- Gamma spectrometry:
  - High-resolution detectors (Ge) with calibration against standards; decay corrections to sampling date.
  - Activity concentrations reported as Bq/kg DM or Bq/m², depending on matrix and measurement.
- Wildlife sampling:
  - Samples from species including rabbit, hare, fox, red deer, woodcock, grouse.
  - Ingested foods and GI contents collected; carcass tissues sampled (e.g., flesh, gut contents); gamma analyses performed on collected tissues.
- Fungi sampling:
  - Fungal species sampled with associated soil, analyzed for radiocaesium content.
- Quality and traceability:
  - Calibration against recognized standards; international standard checks; documentation of internal CEH/ITE codes and sampling metadata.

## Data structure and metadata
- Data organized into five CSV files corresponding to datasets above.
- Extensive fields (e.g., Age_of_wildlife, CEH_Code, sampling dates, location coordinates, habitat, soil pH, soil texture, LOI, bulk density) with long-form descriptors for each column.
- Many columns include units, definitions, and method notes; some fields may be NA or marked as not applicable or not analysed.
- Site and sample identifiers are linked via CEH/ITE codes; geographic coordinates recorded where available.

## Geographic and temporal scope
- Geographic coverage: Great Britain (England, Wales, and Scotland contexts within GB-wide surveys).
- Notable regions: Cumbria (NW England), north Wales, north Yorkshire; additional GB-wide vegetation and fungi sampling.
- Temporal coverage: 1986–1987 (early surveys), through 1988–1997 for vegetation, soil, and fungi datasets; multiple sampling campaigns across years.

## Data quality and limitations
- Precision and detection: activity concentrations include decay-corrected values; some entries may be at or below minimum detectable activity (MDA) in certain fields.
- Data integration challenges:
  - Complex, multi-matrix dataset with many cross-referenced metadata fields and internal codes.
  - Variability in sample types, weights (DM vs fresh), and measurement matrices requiring careful unit harmonization.
- Spatial resolution: some sites have precise coordinates; others may have generalized location data or site-level identifiers.
- Temporal resolution: irregular sampling intervals across datasets (year-to-year gaps in some matrices).

## Access and usage notes
- Source: Chaplow et al. (2015); NERC Environmental Information Data Centre (EIDC).
- Datasets are available as CSV files with rich metadata and code mappings; suitable for data integration, spatio-temporal analyses, and ecosystem radiocaesium transfer studies.
- Proper use should account for units (DM vs fresh weight), decay corrections, and potential missing values or MDA-related gaps.

## Potential analyses and questions
- How radiocaesium transfer varies across vegetation types (grasses/heather) and habitats (open ground vs woodland) after Chernobyl.
- Spatial patterns of Cs-134 and Cs-137 concentrations in soil, vegetation, and wildlife across GB regions and over time.
- Relationship between soil properties (pH, texture, LOI, bulk density) and radiocaesium uptake in soil and plants.
- Temporal trends in radiocaesium deposition and uptake in different matrices (soil, vegetation, fungi, wildlife) from 1986–1997.
- Comparative uptake across wildlife species and feeding pathways (e.g., grazing vs predation) using activity concentrations in tissues and GI contents.
- Integration with other radionuclide measurements (e.g., K-40, Ru isotopes, Pu isotopes) for broader radiochemical profiling and risk assessment.