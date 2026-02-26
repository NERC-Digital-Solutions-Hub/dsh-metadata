# Environmental_CBPeru.csv

## Overview
- Dataset of measured physicochemical variables in 10 rivers across glacial valleys (Parón, Huaytapallana, Llanganuco) in the Cordillera Blanca, Ancash, Peru.
- Connected to the study on how declining glacier cover drives changes in aquatic macroinvertebrate biodiversity.
- Collected in two sampling periods (October 2019 and October 2020) to cover wet and dry seasons, with 37 environmental variables per site.

## Data content and structure
- Site codes: P01–P10 representing each river sampling location.
- Geographic and glacier context per site: basin area, glacier area, glacier coverage (GCC %), distance from glacier, slope, altitude.
- Comprehensive topographic and environmental context per site (e.g., coordinates, valley name, basin area, GCC, distance from glacier, slope, altitude).
- 37 recorded variables per site, including:
  - Physical/chemical water parameters: turbidity (NTU), water temperature (°C), electrical conductivity (µS/cm), pH, dissolved oxygen (mg/L), Pfankuch Index.
  - Nutrients and carbon: total nitrogen (mg/L), total phosphorus (mg/L), dissolved organic carbon (DOC, mg/L), dissolved inorganic carbon (DIC, mg/L), dissolved carbon (DC, mg/L).
  - Anions and cations: F, Cl, SO4, NO3 (mg/L); Al, B, Ca, K, Mg, Na, Si, Zn, Sr, Be, Cd, Co, Cr, Cu, Fe, Li, Mn, Ni, Pb, Se, Te, Ti (mg/L).
  - Season indicator: w = wet season, d = dry season (two records per site).
- Data file: Environmental_CBPeru.csv contains the environmental variables for each site and season in a single Excel sheet (sites in rows, variables in columns).

## Methods and data generation
- Sampling periods: October 14–30, 2019 and October 7–16, 2020.
- In-field measurements:
  - Water parameters (temperature, electrical conductivity, pH, dissolved oxygen) recorded every 5 seconds and averaged over 5 minutes using a Multi 3630 IDS multiparameter instrument.
  - Turbidity measured in the laboratory.
- Laboratory analyses:
  - Metal ions (Al, B, Be, Ca, Cd, Co, Cr, Cu, Fe, K, Li, Mg, Mn, Na, Ni, Pb, Se, Si, Sr, Te, Ti, Zn) via Inductively Coupled Plasma Optical Emission Spectroscopy (ICP-OES).
  - Total nitrogen and total phosphorus via Skalar Sans++ Automatic Wet Chemistry Analyzer.
  - Anions (F, Cl, SO4, NO3) via High Performance Liquid Chromatography (HPLC-IC).
  - Dissolved organic carbon (DOC) and dissolved inorganic carbon (DIC) via Analytik Jena Multi NC2100.
  - Turbidity via Oakton T-100 sensor.
- Channel and landscape context:
  - Pfankuch Index used to assess channel stability (six components: substrate angularity, rock brightness, sediment particle size/compaction, scouring/deposition, stable channel percentage, vegetation).
  - Topography: slope from a 12.5 m resolution DEM; distance to glacier via 10 m Sentinel-2 imagery; glacier delineation using Sentinel-2 data.
- Data provenance: site-specific geographic and glacier context drawn from tables and imagery; coordinates in UTM 18S.

## Data structure and units
- Organization: one Excel sheet; first column = Site; first row = variables; a Season column indicates wet or dry.
- 37 variables with defined units, including:
  - Turbidity (NTU), Water temperature (°C), Electrical conductivity (µS/cm), pH (unitless), DO (mg/L), Pfankuch Index (unitless).
  - TN, TP (mg/L); DOC, DIC, DC (mg/L); F, Cl, SO4, NO3 (mg/L).
  - Metals and metalloids: Al, B, Ca, K, Mg, Na, Si, Zn, Sr, Be, Cd, Co, Cr, Cu, Fe, Li, Mn, Ni, Pb, Se, Te, Ti (mg/L).
- Season indicator: w (wet) or d (dry).

## Quality control
- Instrument calibration prior to each field campaign.
- Use of established reference standards (Environment Canada materials and UK ERM-CA022a) to ensure accuracy and precision of metal analyses.

## Potential uses and applications
- Analyzing relationships among glacier cover, hydrochemistry, and riverine ecosystem dynamics.
- Building data products (dashboards, pivot tables) to explore gradients across sites and seasons.
- Integrating with biodiversity datasets (e.g., macroinvertebrate communities) to study ecosystem responses to glacial retreat.
- Supporting comparative studies of hydrochemistry across tropical Andean glacier-fed rivers.

## Considerations for users
- Two-season data per site enables seasonal comparison but requires careful interpretation when aggregating across sites.
- Data are lab-validated with explicit methods; ensure alignment of units when merging with external datasets.
- Proximal context (Pfankuch Index, topography) enhances interpretation of hydrological and ecological responses to physical habitat changes.