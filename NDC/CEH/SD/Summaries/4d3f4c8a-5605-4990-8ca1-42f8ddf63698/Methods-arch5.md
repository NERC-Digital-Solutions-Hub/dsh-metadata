# EIDC dataset 1: Caterpillar counts from grass margins and hedgerows under streetlights, Oxfordshire, UK, 2018-2020

## Overview
- Dataset documenting caterpillar counts from two habitat types (hedgerows and grass margins) under streetlights, using lit vs unlit matched-pairs design in Oxfordshire, UK.
- Timeframe: 2018–2020; lighting treatments mainly LED and high-pressure sodium (HPS), with some low-pressure sodium (LPS).
- Based on methods from a Science Advances study on street lighting and insect populations; reproduced under CC BY-NC.

## Study design and scope
- Field sites: 26 lit/unlit site pairs plus one triplet, selected to ensure comparable habitat aside from lighting.
- Habitat types: hedgerows (beat sampling) and grass margins (sweep-net sampling); sampling aligned with moth caterpillar life stages.
- Lighting: consistent for at least five years prior; lighting types recorded (LED, HPS, LPS); ALAN effects disentangled from urbanisation via GIS analysis.
- Sampling timing: night sampling between 21:00 and 06:30; nights chosen to minimize phenological artefacts; lux readings taken at heights corresponding to caterpillar exposure (hedgerows ~1.25 m, grass margins ~0.25 m).
- Spectral data: collected for grass margins to assess spectral composition; CCT values reported (HPS ~2200 K, LPS ~1800 K, LED 2700–4000 K); spectral data limited to grass margins.

## Data collection methods
- Hedgerow caterpillars: spring beating at three points per transect (14 m long); methods include drainpipes and beating trays; targeted 4th/5th instars.
- Grass margins: winter sweep-netting for noctuid caterpillars on grasses and low-growing plants; transects ~14 m; multiple visits due to low catch (mean 6.9 per transect).
- Site matching criteria: transects geographically close (median 118 m apart) and along straight roads; hedgerow trees, hedgerow height/width, and vegetation characteristics controlled within pairs; some site exclusions applied to maintain comparability.

## Measurements and data recorded
- Caterpillar counts by transect:
  - All caterpillars (All_Cats), diurnal (DiurCats), nocturnal (NonDiurCats) categories.
  - Grass margins: 16 taxonomic units; hedgerows: 20 taxonomic units in analyses.
- Site and sampling metadata:
  - Visit_ID, Site_ID, Site_Name, Date, DaysSince, Treatment_1 (lit/unlit), Treatment_2 (lighting type), Time, Sunset, MinsPastSunset, Temp_Degree_Celsius, TransectOffset, Dist_between_trans, urbanization metrics at 100/250/500 m radii.
  - Habitat-specific descriptors: Hedge_Height, Dom_plant_species (dominant hedge species); Grass_mean_illumination and Hedge_mean_illumination (lux at respective heights).
  - Spatial references: lit and unlit transect centroids (E/N, lat/long).
- Data capture and quality:
  - Data recorded on standardized forms; entered into Excel with dropdowns; automated calculations; double-checked for errors; samples stored at -20°C (with Covid-related exceptions in 2020).
  - Provisional identifications by lead author using literature and UK Lepidoptera resources.

## Data files and structure
- Main data files:
  - Boyes_et_al_2021_hedgerow_counts.csv (hedgerow caterpillar counts)
  - Boyes_et_al_2021_grass_counts.csv (grass margin caterpillar counts)
- Field site metadata:
  - Boyes_et_al_2021_field_sites_data.csv (site-level information including light type, transect centroids, distance between transects, urbanization metrics)
- Key data columns (examples):
  - Visit_ID, Site_ID, Treatment_1 (Lit/UL), Treatment_2 (LED/HPS/LPS/Unlit), Time, Sunset, MinsPastSunset, Temp_Degree_Celsius, All_Cats, DiurCats, NonDiurCats, Hedge_Height, Dom_plant_species, Lit_urban, Unlit_urban, p100/p250/p500 urban metrics, 100m/250m/500m radii, transect distances.

## Data quality, provenance, and governance
- Provenance: dataset builds on published methods; authors and affiliations listed; data linked to a peer-reviewed study for context.
- Quality controls: standardized sampling protocols across all pairs; matched-pair approach to minimize confounding variables; sampling conducted on the same nights across treatments.
- Data integrity: 24-hour data entry window; data validation through range checks and outlier screening; manual and automated QA steps; samples preserved when possible (losses due to Covid-19 constraints in 2020).
- Taxonomic resolution: 20 hedgerow units; 16 grass-margin units; provisional identifications by a single expert to ensure consistency.
- Documentation: explicit data dictionaries and column descriptions; clear naming conventions for data files; references to related methodological papers.

## Limitations and caveats
- Lux as a proxy: lux readings reflect human visual perception and may not fully capture ecological spectral effects; spectral data were not fully calibrated and were limited to grass-margin sites.
- Spectral coverage: full spectral measurements were not available for all site types; spectrometer data limited to grass margins.
- Sample retention: some caterpillar samples not retained in 2020 due to Covid-19 restrictions.
- Generalizability: matched-pair design within a specific geographic region and lighting context; results contextualized within Oxfordshire and similar lighting regimes.

## Licensing and access
- Source methods reproduced under CC BY-NC; dataset references provided for licensing and attribution.
- Data structure and file names documented to support reuse and integration with other datasets.

## Practical guidance for data stewards
- Ensure clear metadata: maintain a detailed data dictionary, include sampling dates, lighting treatment, transect geometry, and environmental covariates.
- Preserve provenance: link main data files to field site metadata and to the study’s methodological sources.
- Maintain data quality controls: enforce standardized data entry procedures, validation checks, and versioning for updates or corrections.
- Plan for updates: document any changes to lighting regimes, site conditions, or sampling protocols; track any additional sites or extended timeframes.
- Facilitate reuse: provide guidance on taxonomic units, aggregation rules (All_Cats, DiurCats, NonDiurCats), and compatibility with related datasets (e.g., urbanization metrics).