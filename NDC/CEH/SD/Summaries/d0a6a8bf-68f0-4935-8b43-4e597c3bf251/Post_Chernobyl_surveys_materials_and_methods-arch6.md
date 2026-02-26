# Metadata for datasets available from Chaplow et al. (2015): Chaplow, J.S., Beresford, N.A., Barnett, C.L. (2015). Post Chernobyl surveys of radiocaesium in soil, vegetation, wildlife and fungi in Great Britain. NERC Environmental Information Data Centre. http://doi.org/10.5285/d0a6a8bf-68f0-4935-8b434e597c3bf251

## Overview
- Five CSV datasets documenting post-Chernobyl radiocaesium surveys in Great Britain.
- Focus on radiocaesium (Cs-134 and Cs-137) in soil, vegetation, wildlife, and fungi across GB, with sampling from 1986 to 1997.
- Data collected to assess uptake and transfer of radiocaesium through ecosystems and to support environmental monitoring.

## Datasets included
- 1_Post_Chernobyl_survey_data_radiocaesium_in_soil_vegetation_wildlife_1986_and_1987.csv
  - Survey of Chernobyl fallout in graminaceous vegetation across Great Britain ( May–June 1986; re-surveys Oct 1986 and spring 1987 ).
  - Sample types: soil, vegetation, wildlife; includes soil horizons, gut contents, and flesh samples from various species.
- 2_Post_Chernobyl_survey_data_radiocaesium_in_vegetation_1986_1987_1988.csv
  - Radiocaesium in vegetation sampled in Cumbria (1986), north-west England (1987), north Wales (1987) and north Yorkshire (1988).
- 3_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1989_and_1990.csv
  - Soil and vegetation survey at three sites in Cumbria (1989–1990).
- 4_Post_Chernobyl_survey_data_radiocaesium_in_soil_and_vegetation_1992.csv
  - Results from three upland sheep farms in Cumbria (1992).
- 5_Post_Chernobyl_survey_data radiocaesium in fungi 1994 to 1997.csv
  - Fungi and associated soil sampled across GB (autumn 1994–spring 1997).

## Materials and methods (highlights)
- Vegetation sampling: grassy/graminaceous plants clipped from ~1 m2 plots, away from roads and overhanging vegetation; samples oven-dried, weighed, ground, and prepared for analysis.
- Wildlife sampling: collected species including rabbit, hare, fox, red deer, woodcock, grouse; stomach/rumen contents and flesh sampled; gut contents retained for analysis.
- Soil sampling: 20 x 20 x 15 cm blocks from vegetation plots; litter layer separated when present; horizons recorded; soils stored cold until processing.
- Analytical method: gamma spectrometry using high-purity Ge detectors (Ge) or Ge-Li detectors; detectors calibrated with British Calibration Service standards; accuracy checked against international standards; results decay-corrected to sampling date.
- Measurements reported in radiometric units:
  - Cs-134 and Cs-137 activity concentrations in soil and vegetation (Bq/kg dry matter) and deposits (Bq/m2).
  - Other radionuclides detected include K-40, Pu isotopes, and Ru isotopes (where present).
- Metadata and QA: detailed column-level descriptions accompany datasets; decay corrections, detector types, and calibration details documented; several fields capture sample provenance and processing steps.

## Data structure and key variables
- Site and sample identifiers:
  - CEH/ITE sample codes; CEH_Code_Site_name/CEH_Code_Farm; Site_name; Location; Latitude; Longitude.
  - Sampling_date_yyyymmdd; Year-specific Cs concentration fields (e.g., Cs134_bqkg_DM_lower, Cs137_bqkg_DM_upper).
- Measurement specifics:
  - Cs-134 and Cs-137 activity concentrations in various matrices:
    - Soil: upper and lower layers (0-4 cm; below 4 cm); in dry soil matter (DM);  per m2 deposition.
    - Vegetation: Cs-134/137 activity per kg dry weight; Deposition per m2 for vegetation.
    - Fungal samples (where applicable): Cs-137 activity concentration in fungi (dry weight).
  - Depths and bulk density:
    - Depth_lower_soil, Depth_upper_soil_layer; Bulk_density_whole_soil; Bulk_density_0-4cm; Bulk_density_below_4cm; Area and total soil depths (mineral vs organic layers).
- Soil and site characteristics:
  - Habitat (Open ground/Woodland); Soil_classification; Soil_pH (upper/lower); Soil_texture (Clay, Silt, Sand, Organic, Loam, etc.); LOI (loss on ignition); NH4 (extractable ammonium); K (potassium) metrics.
  - Land classification and sampling context (ITE/CEH land classification; Restriction_status for wildlife movement).
- Additional matrix-specific fields (where present):
  - 134Cs and 137Cs activity in various compartments (soil, vegetation, below 4 cm, 0-4 cm, organic/mineral layers).
  - Other radionuclides: Ru-103, Ru-106, Pu isotopes; K-40 detected in various matrices.
- Data quality/notations:
  - MDA indicators (e.g., < denotes detection below minimum detectable activity); n/a indicates not applicable or not present.

## How this supports data use
- Enables cross-dataset analyses of radiocaesium transfer across soil-plant-animal-fungi pathways.
- Allows integration with soil properties (pH, texture, LOI, bulk density) and geographic context (latitude/longitude, habitat) to model uptake and retention.
- Provides decay-corrected, standardized radiocaesium measurements suitable for ecological risk assessment and historical exposure studies.
- Rich metadata supports data discovery, provenance tracking (sample IDs, site codes, project IDs), and reproducibility of analyses.

## Considerations for data support and reuse
- Data are multi-faceted and field-intensive; expect heterogeneity across datasets and years.
- Complex column names and extensive field-level metadata require careful data mapping when integrating datasets.
- Some fields contain notes or non-analysed markers; pay attention to MDA and missing data indicators.
- Useful for longitudinal or comparative studies of radiocaesium in UK ecosystems following the Chernobyl incident.