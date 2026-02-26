# Project Carbon Storage in Intertidal Environments (C-SIDE)

- Funding and data context: NERC project (NE/R010846/1) detailing labile, recalcitrant, and refractory organic matter in UK saltmarsh soils collected from 2018 to 2021; Data Resource ID provided for dataset access.

## Data scope and aims
- Quantifies three pools of soil organic matter (labile, recalcitrant, refractory) and carbon reactivity index (CRI) to assess biodegradability and storage potential.
- Dataset comprises 1211 down-core soil samples from UK saltmarsh sites across 2018–2021 to enable cross-site comparability.

## Location and sampling design
- Observations located in the United Kingdom with coordinates provided in WGS84 (lat/lon) to allow spatial analysis.
- Sites chosen to represent diverse UK saltmarsh habitats while maintaining similar environmental regions for comparability.

## Variables and measurements
- Core and location data: Core_ID, Saltmarsh name, Latitude (Lat_dec_deg), Longitude (Long_dec_deg), Depth interval of sub-sample (cm), Depth interval mid-point (cm).
- Organic matter fractions (wt%): Labile OM (%wt), Recalcitrant OM (%wt), Refractory OM (%wt), Total OM (%wt).
- CRI: CRI Carbon (dimensionless), as CRI = %OM_R / %OM_total, where OM_R combines recalcitrant and refractory fractions.
- Proxy data field: CRI serves as a continuum of reactivity (0 = fully biodegradable, 1 = non-biodegradable).

## Methods and data processing
- Sample preparation: Freeze-dried, milled ~20 mg subsamples; placed into 70 mL aluminium oxide crucibles.
- Thermogravimetric analysis (TGA): Mettler Toledo TGA2, 40°C to 1000°C at 10°C/min in N2 flow; thermograms adjusted to a common temperature scale and clipped to 200–650°C to remove water/impurities.
- Data normalization: Thermograms normalized to mass loss to ensure comparability across samples.
- OM fraction definitions (thermally defined by TGA): Labile 200–400°C; Recalcitrant 400–550°C; Refractory 550–650°C. Updated ranges used: Labile OM (200–400°C) and combined Recalcitrant+Refractory OM (400–650°C) for CRI calculation.
- Calibration and QA: Thermogravimetric analysis calibrated with standard substances; laboratory equipment calibrated per institutional practices; no explicit statistical treatment reported (NA for statistics).
- CRI calculation: CRI is derived from the OM fractions following the Rp Index methodology (Kristensen, 1990) as CRI = %OM_R / %OM_total.

## Data file and structure
- Primary data file: C_SIDE_organic_matter_pools_and_reactivity.csv
- Key columns (with formats): 
  - Core_ID (text), Saltmarsh name (text), Lat_dec_deg (number), Long_dec_deg (number)
  - Depth_interval_cm (number), Depth_midpoint_cm (number)
  - Labile_OM_Perc (number), Recalcitrant_OM_Perc (number), Refractory_OM_Perc (number)
  - Total_OM_Perc (number), CRI_Carbon (number)
- Additional metadata: Descriptions and units provided for each column; NA used where data are not applicable.

## Access, usage, and references
- Data can be uploaded to data portals with metadata for discoverability; formats provided as CSV for easy reuse.
- References guiding methodology:
  - Kristensen, E. (1990). Characterization of biogenic organic matter by stepwise thermogravimetry.
  - Smeaton, C. & Austin, W.E.N. (2022). Quality not quantity: Prioritizing the management of sedimentary organic matter across continental shelf seas.