# Structure and composition of woodlands across Mozambique: supporting documentation

## Overview
- Quantitative datasets describing woodland structure and composition from 431 plots across 27 villages in Mozambique (3 districts: Gaza, Niassa, Zambezia; 2014–2015).
- Part of the ESPA-funded ACES project; aims to understand how land use affects ecosystem services and rural livelihoods, linking woodland data with household surveys and remote sensing.
- Data describe woodland structure, litter and biomass (leaf, woody litter, grass), coarse woody debris, and canopy cover; local tree names recorded; species identifications provided in a separate dataset.
- Data intended to quantify ecosystem service provision and to support analyses of human wellbeing and landscape-scale patterns.

## Study areas and sampling framework
- Districts and villages:
  - Mabalane (Gaza Province): 7 villages plus a pilot village.
  - Marrupa (Niassa Province): 10 villages.
  - Gurue (Zambezia Province): 10 villages.
- Plot design and scales:
  - Circular plots with a 20 m radius (0.126 ha) within defined village sampling areas.
  - Within plots: all tree stems >5 cm DBH recorded; four 1 m² quadrats sampled for leaf litter, woody litter, and grass biomass.
  - Coarse woody debris measured along four transects crossing the plot.
  - Canopy cover estimated with a Densiometer (center of plot in each cardinal direction).
  - GPS-based geolocation with altitude; local tree names recorded; trees identified to species (separate dataset).
- Sampling intensity and area definitions:
  - Mabalane: 24 circular plots per village; village sampling area defined as a 5 km radius from village centre (representing typical daily woodland resource access).
  - Marrupa and Gurue: 12 plots per village (6 random points with paired plots to reduce walking time); village boundaries determined by local leaders due to close proximity of villages.
- Timeline:
  - Mabalane: May–September 2014.
  - Marrupa: May–August 2015.
  - Gurue: September–December 2015.

## Plot design, measurements, and data collected
- Tree and woody debris measurements:
  - stems >5 cm DBH; record local tree name, DBH measurement height, and stem condition (live/dead, cut/broken, etc.).
  - Stumps of cut stems included; height of stump recorded; DBH adjustments for stems measured below 1.3 m (see DBH correction).
- Litter and biomass:
  - Leaf litter, woody litter, and grass biomass weighed in 1 m² quadrats at four directions per plot.
  - Subsampling for leaf litter and grass dried in lab to determine dry weight; woody litter presumed dry.
- Canopy and structural data:
  - Canopy cover via Densiometer; qualitative observations of canopy, slope, fire impact.
- Coarse woody debris:
  - Measured along four transects per plot; diameter at intersection with transect, length, decomposition class, and local name recorded.
- Soil and grass species data:
  - Soil samples collected but not included in this dataset; dominant grass species assessment was attempted but omitted due to identification difficulties in dry season.
- Data capture and instrumentation:
  - GPS (Garmin etrex series), DBH tapes, Densiometer, tape measures, Android tablets with ODK, hanging scales for biomass, precision lab scales, 1 m² quadrat frames.

## Data structure and contents
- Six data files (datasets) with linking keys:
  - cwd.csv: coarse woody debris pieces per plot (length, diameter, species, etc.).
  - cwd_decomposition.csv: decomposition class descriptions and correction factors for biomass.
  - plot_metadata.csv: plot-level metadata (coordinates, area, date, altitude, observations, data completeness flags).
  - quadrat_data.csv: biomass weights for leaf litter, woody litter, and grass, plus canopy cover per quadrat.
  - tree_stem_data.csv: tree stems >5 cm DBH per plot (species, DBH, status, stump height, etc.).
  - tree_stem_data_pilot.csv: tree stems for pilot study (nested plots) with similar fields.
- Key fields and linkage:
  - survey_id identifies site (4 = pilot, 5 = Mabalane, 6 = Marrupa, 7 = Gurue).
  - plot_id uniquely identifies plots; subplot_id used only for pilot nested plots.
  - transect_id and quadrat_id indicate specific transects/quadrats within plots.
- Units and data types:
  - Measurements in meters (length, DBH heights), centimeters (DBH), grams (wet/dry weights), and percentages (canopy cover).
  - Missing data are blank; zeros indicate real measurements (e.g., no debris or biomass recorded).
- Data interpretation notes:
  - Some plots lack complete data; data quality notes and completeness indicators are included in plot_metadata.
  - Tree and stem IDs may not be strictly chronologically ordered within CSV files.

## Quality control and data quality
- In-field quality control:
  - Field teams trained; translators provided for local languages and Portuguese.
  - Data collected electronically (ODK) where possible; standardized binary responses used to minimize ambiguity.
- Post-collection quality control:
  - Lead author performed quality assurance; outliers and unexpected values identified and corrected or removed.
  - Data cleaned and translated (Portuguese to English) where needed.
- Documentation of methods changes:
  - Acknowledgement that methods evolved; differences between sites are noted in the dataset descriptions.

## Data limitations and caveats
- Method evolution and site differences mean cross-site comparability may require careful harmonization.
- Grass species data were omitted due to identification challenges; soil data collected but not included here.
- Not all plots have complete datasets; missing data are documented in plot_metadata.
- Pilot study plots used alternative designs (nested plots) and have distinct data fields (pilot-specific dataset).

## DBH correction and estimation
- For stems measured below 1.3 m, a correction function estimates DBH at 1.3 m to avoid biomass overestimation.
- Function based on taper measurements from Miombo species in central Mozambique; applies a height-adjustment parameter and a constant k derived from dm and p.

## Context, references, and potential uses
- ESPA ACES project context:
  - Charcoal production and land-use intensification examined; linkage to ecosystem services and rural livelihoods.
- Key references cited for methods and context:
  - Waddell 2002 for coarse woody debris sampling and decomposition corrections.
  - Baumert et al. (2016) on charcoal supply chains.
  - Related studies on land-use impacts and wellbeing.
- Data utility for data leaders:
  - Comprehensive data inventory of woodland structure, biomass, and canopy metrics across multiple sites.
  - Clear data lineage with linking keys (survey_id, plot_id, transect/quadrat IDs) enabling integration with household surveys and remote sensing.
  - Highlights data quality practices (training, translation, electronic collection) and documentation of gaps and method changes.
  - Useful for landscape-scale analyses of ecosystem services, policy planning, and cross-network data collaborations across Mozambique.