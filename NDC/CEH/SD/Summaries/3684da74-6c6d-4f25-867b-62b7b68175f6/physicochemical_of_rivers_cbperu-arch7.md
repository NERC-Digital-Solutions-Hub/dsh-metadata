# Environmental_CBPeru.csv

## Overview
- Dataset of measured physicochemical variables in 10 rivers from glacial valleys (Parón, Huaytapallana, Llanganuco) in the Cordillera Blanca, Ancash, Peru.
- Purpose: analyze physicochemical changes under glacial retreat across a gradient of glacier coverage and relate to aquatic macroinvertebrate biodiversity.
- Two sampling periods: October 2019 and October 2020.

## Spatial scope and site metadata
- Sites coded P01 to P10, representing ten rivers/locations.
- Geographic context includes:
  - Valley names: Parón, Huaytapallana, Llanganuco
  - Basin area, glacier area, and glacier-covered fraction (GCC) per site
  - Distance from glacier (km), slope (%), altitude (m above sea level)
- Coordinates provided in UTM 18S for each site; topographic context derived from:
  - 12.5 m resolution DEM for slope
  - 10 m resolution Sentinel-2 imagery to determine distance to glacier
- Site-by-site glacier coverage and proximity enable analysis of glacier-driven changes

## Data content and variables
- 37 environmental variables per site per season (wet and dry).
- Core water-quality parameters measured in the field with a Multi 3630 IDS multiparameter instrument (every 5 seconds, averaged over 5 minutes):
  - Water temperature (WT, °C)
  - Electrical conductivity (CE, µS/cm)
  - pH
  - Dissolved oxygen (DO, mg/L)
  - Turbidity (Turb, NTU; turbidity measured in the lab for most samples)
- Additional laboratory-derived chemical parameters:
  - Nutrients: Total nitrogen (TN, mg/L), Total phosphorus (TP, mg/L)
  - Dissolved organic carbon (DOC, mg/L)
  - Dissolved inorganic carbon (DIC, mg/L)
  - Dissolved carbon (DC, mg/L)
  - Anions: F, Cl, SO4, NO3 (mg/L)
  - Cations and metals: Al, B, Ca, K, Mg, Na, Si, Zn, Sr, Be, Cd, Co, Cr, Cu, Fe, Li, Mn, Ni, Pb, Se, Te, Ti (mg/L where applicable)
- Pfankuch Index (PI) as a measure of channel bed stability (based on substrate angularity, rock brightness, particle size/compaction, scouring/deposition, stable channel percentage, and vegetation)
- Seasonal indicator: w = wet season, d = dry season

## Data collection and methods
- Water sources originate from western flanks of Huandoy and Huascarán glaciers.
- Sampling windows:
  - 14–30 Oct 2019
  - 7–16 Oct 2020
- Field measurements:
  - In situ: WT, CE, pH, DO using Multi 3630 IDS
  - Turbidity: laboratory analysis from filtered samples
  - Sample collection for lab analysis: 50 mL for most analytes; 10 mL filtered for turbidity
- Laboratory analyses (at University of Leeds, Environment Faculty):
  - Metals (Al, B, Be, Ca, Cd, Co, Cr, Cu, Fe, K, Li, Mg, Mn, Na, Ni, Pb, Se, Si, Sr, Te, Ti, Zn): ICP-OES
  - TN, TP: Automatic wet chemistry analyzer
  - Anions (F, Cl, SO4, NO3): HPLC-IC
  - DOC, DIC: Micro-elemental analyzer
  - Turbidity: Oakton T-100 sensor
- Channel stability and channel geometry characterized via Pfankuch Index

## Data structure and units
- Data stored in a single Excel sheet.
- Layout:
  - First column: Site (P01–P10)
  - First row: Variables (37 environmental variables)
  - Season column: Indicates season with a code (w = wet, d = dry)
- Variables and units (representative subset):
  - Turbidity (NTU)
  - WT (°C)
  - CE (µS/cm)
  - pH (unitless)
  - DO (mg/L)
  - PI (Pfankuch Index; unitless)
  - TN, TP, DOC, DIC, DC (mg/L)
  - Anions (F, Cl, SO4, NO3) (mg/L)
  - Cations/ Trace metals (Al, B, Ca, K, Mg, Na, Si, Zn, Sr, Be, Cd, Co, Cr, Cu, Fe, Li, Mn, Ni, Pb, Se, Te, Ti) (mg/L)
- Seasonal distinction captured to compare wet vs. dry conditions

## Quality control and provenance
- Equipment calibrated before each field campaign.
- Calibration standards include Environment and Climate Change Canada references and interlaboratory standards for metals (ERM-CA022a).
- Data contributed by:
  - Sample collection: Palacios, E.; Medina, K.; Loarte, E.
  - Laboratory analysis: Palacios, E.; Gamboa, M.; Brown, L.
  - Supporting information: Castañeda, A.; Polo, R.; Tapia, P.
  - Planning and management: Medina, K.; Loarte, E.; Brown, L.; Pellicciotti, F.
- References include Pfankuch (1975) for channel stability methodology; dataset linked to the article on glacier retreat and macroinvertebrate biodiversity.

## How to use in GIS
- Integrate site coordinates (UTM 18S) with spatial layers:
  - DEM-derived slope
  - Glacier extents and GCC rasters
  - Sentinel-2 based proximity analyses
- Combine 37 variables (per site per season) with attribute tables to create:
  - Thematic maps of water quality across sites
  - Gradient analyses of physicochemical changes along glacier coverage
  - Spatially-enabled analyses of relationships between physicochemical parameters and Pfankuch Index
- Use site-level attributes (basin area, glacier area, GCC, distance to glacier, altitude, slope) to contextualize environmental drivers
- Seasonality can be analyzed by creating separate layers or time-enabled datasets for wet vs. dry seasons

## Limitations and considerations
- Two sampling periods (2019 and 2020) provide seasonal snapshots; broader temporal coverage would enhance trend analysis.
- Some sites (e.g., P08) show very low or zero glacier coverage, which should be considered when interpreting gradient effects.
- Turbidity measured in the lab; ensure proper workflow replication if integrating with field turbidity measurements.
- Data uses UTM 18S coordinates; ensure consistent CRS when merging with other GIS data

## References
- Pfankuch, J. D. (1975). Stream reach inventory and channel stability evaluation. USDA Forest Service Northern Region, Montana.
- Related article: Declining glacier cover drives changes in the biodiversity of aquatic macroinvertebrates in the Cordillera Blanca, Peru.