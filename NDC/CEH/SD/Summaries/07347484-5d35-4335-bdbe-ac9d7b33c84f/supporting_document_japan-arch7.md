# Impact of environmental radiation on the health and reproductive status of fish from Japan, 2017

## Overview
- Study (May 2017, 10 days) assessing the impact of environmental radiation on cataract formation and reproductive status in fish from Japan.
- Focus on measuring physical health indicators and germinal tissues to infer radiation effects.

## Study sites and sampling
- Lakes: Suzuuchi (SU), Funazawa (FZ), Kashiramori (KM), Abakuma; Abukuma River Shinobu Dam site (coordinates provided).
- Abukuma Shinobu Dam site coordinates: 37°42'21.28"N, 140°30'07.03"E (not shown on map).
- Targeted time frame and location details used to select sampling points.

## Target species
- Crucian carp (Cyprinus carpio), common carp (Carassius carassius), largemouth bass (Micropterus salmoides), smallmouth bass (Micropterus dolomieu), carp KOI (Cyprinus sp.).

## Objectives
- Assess radiation-related cataract formation in carps and largemouth bass.
- Assess radiation-related effects on the reproductive status of carps.

## Methods
- Specimen collection:
  - Largemouth bass: total length 17–22 cm (same-size group).
  - Carps: total length 20–30 cm (to target two generations, F0 and F1, ideally).
- Processing:
  - Fish killed, measured; scales and otoliths removed for age determination.
  - Gonads dissected, weighed, fixed in buffered formalin for 24 h, then preserved in ethanol.

## Data structure: japan_biometry.csv
- Site: Lake (geographical region).
- Site units/methodology: Geographical region.
- Species (examples): 
  - Common carp Cyprinus carpio
  - Crucian carp Carassius carassius
  - Largemouth bass Micropterus salmoides
  - Smallmouth bass Micropterus dolomieu
  - Carp KOI Cyprinus sp.
- Measurements and units:
  - Weight: Total fish weight (grams)
  - BL: Body length up to the start of the tail (cm)
  - SL: Length up to the fork of the tail (cm)
  - TL: Total fish length (cm)
  - GW1: Gonad weight (grams)
  - GW2: Second gonad weight for males (grams; may be blank if not recorded)
  - Sex: M (male) or F (female)
  - Liver weight: (grams; may be blank if not recorded)
- Notes:
  - Blank fields indicate weight/measurement not recorded.
  - Units: weights in grams; lengths in centimeters.
  - Data accommodates multiple species with corresponding fields.

## Spatial data and GIS relevance
- Provides lake-level identifiers and a geographical region field suitable for GIS joins.
- Specific coordinate provided for Abukuma Shinobu Dam site; enables point mapping.
- Data can be visualized as layers: sampling sites by lake, species distributions, and measured biometric indicators.

## Data access and reuse
- Dataset available at DOI: 10.5285/07347484-5d35-4335-bdbe-ac9d7b33c84f
- Citation: Lerebours, A.; Smith, J.T. (2019). Impact of environmental radiation on the health and reproductive status of fish from Japan, 2017. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/07347484-5d35-4335-bdbe-ac9d7b33c84f

## Considerations for GIS specialists
- Data harmonization across species and measurement fields; address missing GW1/GW2, Sex, and Liver weight values.
- Integrate with environmental radiation data and basemaps to analyze spatial patterns of health indicators.
- Temporal aspect is limited to a single sampling window; potential to compare F0 and F1 generation data if age/temporal metadata permit.
- Validate lake boundaries and ensure accurate mapping for SU, FZ, KM, Abakuma; incorporate Shinobu Dam coordinates as a point layer.

## Limitations and notes
- Abukuma Shinobu Dam site coordinates are provided but not mapped in the accompanying materials.
- Geographic coverage is limited to the listed lakes and site; broader regional extrapolations should be approached cautiously.