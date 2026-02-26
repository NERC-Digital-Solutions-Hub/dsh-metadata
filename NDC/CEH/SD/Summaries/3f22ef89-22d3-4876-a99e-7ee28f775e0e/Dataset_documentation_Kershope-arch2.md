# Solute concentrations in water samples from clearfelled and standing Sitka spruce ( Picea sitchensis ) forest ecosystems, Kershope Forest

## Overview
- Describes a dataset of solute concentrations and related water quality parameters in drainage water and various forest-system waters at Kershope Forest, Cumbria, England.
- Solutes include potassium, calcium, magnesium, iron, sodium, aluminium, phosphate, nitrate, ammonium, chloride, sulphate, plus pH, suspended solids, and total organic carbon.
- Intended to assess how clearfelling Sitka spruce plantations affects nutrient fluxes and soil fertility, within the Crookburn Hill Drainage Experiment framework.
- Data collected by the Institute of Terrestrial Ecology (ITE) Merlewood staff; chemical analyses by ITE Merlewood Chemical Analysis Section and later by CEH laboratories; some methods cross-validated over time.

## Study design and site
- Location: Kershope Forest, Cumbria, England; former upland grassland planted with Sitka spruce in 1948.
- Site description: peaty gley soil (Cambic stagnohumic gleys), calcareous parent material with calcified depth 75–150 cm; gentle easterly slope (1–5 degrees); mean altitude ~225 m.
- Experimental setup: Block 1 of an original drainage experiment comprising six plots with varying drain spacing (10–40 m) and drain depth (60–90 cm). Three plots felled in 1983; three remained standing.
- Objective: quantify sources and fluxes of solutes through standing vs. clearfelled forest plots and through the forest-soil system across different drainage configurations.

## Sampling and data collection
- Drainage water
  - Main exit drain water sampled weekly from each plot (1981–1987); sampling designed to capture representative flow and avoid floor disturbance via a 2 m PVC sampling extension; discharge measured with a V-notch weir; occasional extra samples during floods.
- Other forest-system waters
  - Soil solution samplers and lysimeters (two horizons per plot, L and O horizons; several horizons per sampler) sampled fortnightly.
  - Rainfall: bulk precipitation collected weekly with funnel assemblies; light exclusion and debris prevention measures.
  - Stemflow: collected from representative trees across size classes; volume and samples collected biweekly.
  - Throughfall: sampled fortnightly.
  - Knapp throughflow: measured but noted as unreliable due to equipment issues.
  - Needle trays (brash throughfall): sampled fortnightly; needles accumulated in trays and pooled for analysis.
- Sampling period notes
  - Drainage water: 17 June 1981 – 30 December 1987.
  - Water samples (other than drainage): 17 June 1981 – 23 December 1985.
  - Sampling covered both standing and felled plots, with pre- and post-felling monitoring.

## Analytical methods
- Laboratory analyses conducted at Merlewood and CEH facilities.
- Ion measurements and related parameters
  - Calcium, magnesium, aluminium, iron by atomic absorption; sodium and potassium by flame emission.
  - Phosphate by molybdenum blue method; ammonium by indophenol blue method.
  - Chloride historically by thiocyanate, later by ion chromatography for some years; nitrate by reduction method and Griess-Hosvay; sulphate by barium chloride turbimetric method, then ion chromatography.
  - pH measured in sub-samples; samples filtered prior to most determinations.
- Additional metrics
  - Suspended solids (TSS) and total organic carbon (TOC) measured by standard methods.
- Data quality and method continuity
  - Old and new methods were used concurrently for about three months to ensure comparability; weekly and fortnightly sampling schedules supported high temporal resolution for trend analysis.

## Data products and file descriptions
- Drainsker.csv
  - Main dataset of solute concentrations and related metrics for drainage water from six plots (three felled, three unfelled) in Block 1.
  - Columns include sampling occasion, sample code, date, discharge (m3 s-1), suspended solids (mg L-1), pH, and concentrations for K, Ca, Mg, Fe, Na, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, and TOC.
  - A code of -1 indicates no sample for that entry.
- Soilsker.csv
  - Solute concentrations from soil samplers across horizons (L, O, E, B) and lysimeters; includes horizon-specific sampling codes and sample type (e.g., stem-flow, throughfall, lysimeter, soil).
  - Columns cover week code, date, volume (ml), pH, and concentrations for the same solutes as above.
  - Uses a detailed coding scheme to map samples to specific plots, horizons, and sample types.
- Kershope_sampling_points.csv
  - Sampling locations and site metadata for the points listed in the study; includes felled status, block, drain spacing, drain depth, and geographic coordinates (easting/northing) in the British National Grid.
- Kershope_codes.csv (referenced for code key)
  - Provides a key to interpret sample codes used in Soilsker.csv and related tables, mapping sample codes to plots, horizons, sample types, and other descriptors.
- Data origin and access notes
  - Data were generated as part of a broader program on forest hydrology and nutrient fluxes in response to clearfelling; records indicate collaboration between Forestry Commission Northern Research Station and CEH/ITE with cross-institution data handling.

## References and further reading
- Adamson, J., Hornung, M. (1990). The effect of clearfelling a Sitka spruce plantation on solute concentrations in drainage water. Journal of Hydrology, 116(1), 287-297.
- Adamson, J., Hornung, M., Pyatt, D., Anderson, A. (1987). Changes in solute chemistry of drainage waters following the clearfelling of a Sitka spruce plantation. Forestry, 60(2), 165-177.
- Allen, S.E. (Ed.). (1989). Chemical Analysis of Ecological Materials (2nd ed.). Blackwell.
- Avery, B.W. (1980). Soil classification for England and Wales. Soil Use & Management, 1, 89-94.
- Knapp, B.J. (1973). A system for the field measurement of soil water movement. Bulletin.
- Neal, C. et al. (1999). Analysis of impacts of major anion variations on surface water acidity: case studies from Wales and Northern England. Hydrology and Earth System Sciences, 2(2/3), 303-322.
- Pyatt, D.G. et al. (1985). A drainage experiment on a peaty gley soil at Kershope Forest, Cumbria. Soil Use & Management, 1, 89-94.
- Rowland, A.P. (1983). An automated method for ammonium-N determination. Communications in Soil Science & Plant Analysis, 14(1), 49-63.

## Data usage and objectives for monitoring
- Enables standardized assessment of environmental health and policy performance over time by providing time-resolved, comparable nutrient flux data across different forest management states (standing vs felled) and drainage configurations.
- Supports data accessibility and transparency by detailing collection methods, sampling design, and data formats, facilitating reuse by researchers, managers, and policy analysts.