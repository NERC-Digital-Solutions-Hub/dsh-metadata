# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

## Overview
- Dataset from a study on how local-scale environmental factors relate to Acute Oak Decline (AOD) symptoms.
- Three oak woodlands in southern England (Monks Wood, Writtle Forest, Stratfield Brake).
- 60 sampled oaks (20 per site: 10 symptomatic, 10 asymptomatic) to explore interactions between tree/soil/site characteristics and AOD status.
- Data organized into three CSV files for tree, site, and soil characteristics.

## Data Files and Their Contents
- Tree_characteristics.csv
  - Per-tree data including: site, tree ID, latitude/longitude (WGS84), AOD symptom status, species classification (morphometric leaves; genetic SNP confirmation), leaf counts for morphometry, tree dimensions (height, DBH, crown widths), crown density reduction, rooting depth.
- Site_characteristics.csv
  - Per-tree contextual data: site name, AOD status, depth to gleying, basal area within 0–20 m and 20–40 m, compound topographic index, tree social status (dominant to dying).
- Soil_characteristics.csv
  - Per-tree per-depth soil properties: sample depth (5–15 cm or 40–50 cm), organic matter (LOI), pH, texture (clay/silt/sand %), total carbon and nitrogen, mineral N (nitrate and ammonium), Olsen P, cation exchange capacity, exchangeable cations (Al, Ca, Fe, K, Mg, Mn, Na), bulk density; data also include measurement method details and replication.

## Measurements, Units and Methods
- Tree measurements
  - Latitude/Longitude: decimal degrees (WGS84)
  - Tree height: metres
  - DBH (diameter at breast height): centimetres
  - Crown dimensions: metres (widths EW and NS)
  - Crown density reduction: percent
  - Rooting depth: centimetres
  - Species identity: morphometric leaf analysis and genetic SNP-based confirmation
  - AOD_symptom_status: symptomatic (bleeding stem cankers) or asymptomatic
  - Social status: dominant, codominant, subdominant, suppressed, or dying
- Site context
  - Depth_to_Gleying_cm: centimetres
  - Basal_Area_0_20m and Basal_Area_20_40m: square metres
  - Compound_topographic_index: unitless
  - Site-specific AOD status linked to trees
- Soil properties
  - Sample_depth: 5–15 cm or 40–50 cm
  - OM_%: percent organic matter
  - pH: pH units (in water)
  - Texture: clay_%, silt_%, sand_% (percent in fraction)
  - TotalC_% and TotalN_%: percent carbon and nitrogen
  - NitrateN_mgkg and AmmoniumN_mgkg: mg/kg dry soil
  - OlsenP_mg/kg: mg/kg dry soil
  - CEC_mmolc kg: mmolc kg
  - Exchangeable Al, Ca, Fe, K, Mg, Mn, Na: mg/kg dry soil
  - Bulk density: g dry soil cm^-3
- Quality control and replication
  - Technical replicates for key analyses (e.g., LOI, pH, particle size, Total C/N, Olsen P, mineral N, exchangeable cations)
  - Blanks, reference materials, and calibration details documented for each instrument
  - Handling of measurements below detection limits (e.g., loD/2 convention for certain extracts)

## Experimental Design
- Sites: Monks Wood (Cambridgeshire), Stratfield Brake (Oxfordshire), Writtle Forest (Essex)
- Sampling frame: 60 trees total (3 sites × 20 trees/site)
  - At each site: 10 AOD-symptomatic trees identified by bleeding canker signs; 10 asymptomatic trees randomly selected from the remaining population (>20 m from a symptomatic tree)
- Leaf and soil sampling
  - Leaves: five leaves per tree for morphometric and genetic species identification
  - Soil: eight field-moist samples per depth (5–15 cm and 40–50 cm) per tree, pooled by depth to one composite sample; soils air-dried and sieved (<2 mm) prior to most analyses

## Collection, Transformation and Quality Assurance
- Field protocols
  - Standard forest mensuration procedures for tree measurements
  - Crown condition monitoring per established protocols
  - 0.8 m soil pits near each tree; depth to gleying and rooting depth measured in pits
  - Micro-topography recorded along radial transects; Topographic Wetness Index calculated per Sørensen et al. (2006)
  - Basal area determined with a relascope within 0–20 m and 20–40 m zones
- Laboratory analyses
  - Loss on ignition for organic matter
  - pH measurement in water
  - Particle size distribution via Malvern Mastersizer 3000
  - Total C and N with CN analyzer
  - Exchangeable cations via BaCl2 extraction and ICP-OES
  - Olsen P by Olsen method; mineral N by KCl extraction and colorimetric analysis
  - Replicates and calibration standards documented; blanks and reference materials used
  - For some Olsen P samples with low peaks, re-analysis with alternate spectrophotometer
- Data handling
  - Missing values indicated as 'nd'
  - Below-detection-limit values treated as half the detection limit for calculations

## Temporal and Spatial Coverage
- Temporal: Fieldwork and sampling conducted July–November 2016 (one time point)
- Spatial: Three woodlands in southern England with tree-level coordinates provided in Tree_characteristics.csv

## Intended Use and Availability
- Purpose: Enable analysis of how local-site and soil factors relate to AOD symptom expression at the tree scale
- Data structure supports integration with other environmental datasets; designed for standardized storage and portal upload
- Associated pre-print describing the local-scale site and soil factors in AOD: available at the provided DOI

## References and Provenance
- Methods and protocols draw on established forest mensuration, crown assessment, soil analysis, and data-quality guidance
- Key references include Hamilton (1975), Lakatos et al. (2014), Sørensen et al. (2006), Olsen et al. (1954), USEPA (2000), and related oak species identification studies (Kremer et al. 2002; Guichoux et al. 2013)