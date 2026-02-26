# Structure and composition of woodlands across Mozambique: supporting documentation

## Overview
- Quantitative measurements of woodland structure and composition from 431 plots across 27 villages in Mozambique.
- Data collected across three districts/provinces: Mabalane (Gaza), Marrupa (Niassa), and Gurue (Zambezia) during 2014–2015.
- Measurements include tree stems >5 cm DBH, leaf/woody litter and grass biomass, coarse woody debris, and canopy cover.
- Data collected as part of the ESPA-funded ACES project to understand how land use affects ecosystem services and rural wellbeing; linked with household surveys and remote sensing for scaling.
- Methodologies co-developed with ACES researchers; field data collected by authors with local assistance; quality assured by lead author.

## Study areas and sampling design
- Mabalane District: 7 villages targeted for charcoal production intensity; 24 plots per village within a 5 km radius of village centers.
- Marrupa District: 10 villages; 12 plots per village to represent woodland complexity (paired plots to reduce walking time).
- Gurue District: 10 villages; 12 plots per village; village boundaries used to delineate sampling areas due to proximity of villages.
- Plot placement: random within defined village sampling areas; overall aim to capture gradient of land-use intensity and woodland types (mainly Miombo).

## Plot design and measurements
- Plots: circular, 20 m radius (0.126 ha). Center located and geolocated; edge defined using a robust field method approximating an octagonal edge.
- Within each plot:
  - All tree stems >5 cm DBH recorded with species names provided locally; stumps included.
  - Coarse woody debris measured along four transects from plot center to edge; length, diameter at intersection, decay class, and local species named recorded.
  - Canopy cover estimated with a Densiometer.
  - Four 1 m^2 quadrats used to collect and weigh leaf litter, woody litter, and grass biomass (wet weight; dry weights inferred for some samples).
  - Soil samples collected but not included in these datasets.
  - Grass species data attempted but omitted due to identification challenges in the dry season.
- Pilot study within Mabalane used varied plot designs to test suitability for future surveys.

## Data structure and contents
- Six datasets spanning the field measurements:
  1. cwd.csv — individual coarse woody debris pieces per transect/plot with length, diameter, decomposition class, and local species.
  2. cwd_decomposition.csv — decomposition class descriptions and reduction factors for biomass corrections.
  3. plot_metadata.csv — plot center coordinates, plot size/area, date, slope, burnt status, canopy observations, completeness indicators, and data quality notes.
  4. quadrat_data.csv — biomass (wet) in four quadrats per plot and four canopy cover estimates.
  5. tree_stem_data.csv — all tree stems >5 cm DBH with diameter, species, status (dead/alive, cut/broken), stump height, and positional/observational data.
  6. tree_stem_data_pilot.csv — pilot study tree-stem measurements (nested plots) with similar fields.
- Linking identifiers: survey_id (4 = pilot, 5 = Mabalane, 6 = Marrupa, 7 = Gurue), plot_id, and where applicable subplot_id or transect/quadrat_id.

## Data collection instruments and protocols
- Field equipment: Garmin GPS for location, DBH tapes for diameter, Spherical Crown Densiometer for canopy, tape measures for plot and debris metrics, ODK-enabled Android tablets for data capture, hanging scales for biomass, and high-precision scales for lab weights.
- Plot location and measurements documented with averaged center waypoint; altitude and slope recorded; notes on recent fire and canopy observations.
- Data collected in Portuguese and translated to English; standardized data entry with predefined fields to minimize ambiguity.

## Quality control and data integrity
- Data quality assured by the lead author; field teams trained; translators used to ensure consistent communication.
- In-field consistency checks and post-collection cleaning to identify outliers and anomalies; missing values and errors flagged in plot_metadata and datasets.
- Electronic data capture reduced transcription errors; where possible, missing or partial data were annotated rather than guessed.

## Estimating DBH for measurements below 1.3 m
- When stem measurements were taken below 1.3 m, a correction function based on local Miombo species tapering was applied to estimate DBH at 1.3 m.
- The method uses measured diameter and height of measurement to adjust DBH, ensuring biomass estimates remain robust when measurements are not taken exactly at breast height.

## Limitations and considerations
- Method evolution across sites means some procedures varied slightly; such differences are noted in the documentation and dataset descriptions.
- Not all plots have complete datasets; grass species data were omitted due to identification challenges; soil data are not included in these datasets.
- Canopy measurements missing for some plots (due to equipment availability); some plots have partial data (marked in plot_metadata).
- Boundaries and sampling areas differ between sites, potentially affecting cross-site comparability; where relevant, site-specific method notes are provided.

## References and context
- References to relevant literature and project outputs underpinning the study design and interpretation of results, including lineage on charcoal production, land-use impacts, and coarse woody debris methodology.