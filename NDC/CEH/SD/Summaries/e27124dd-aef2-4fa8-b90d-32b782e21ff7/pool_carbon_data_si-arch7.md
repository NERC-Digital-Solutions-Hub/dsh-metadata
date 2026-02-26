# Carbon concentrations in natural and restoration pools in blanket peatlands in Scotland, 2013-2015

## Overview
- Presents carbon concentration data from natural and restoration (artificial) pools across blanket peatlands in Scotland (2013–2015).
- Data collection and generation methods are described in the associated Hydrological Processes manuscript (2022); data have undergone quality control (e.g., values below detection limits).

## Data files and structure
- Six CSV files containing the dataset:
  - Pool_Carbon_Quarterly: All data from LL, CL, MU pooled into one table (quarterly pools only).
  - Pool_Carbon_Routine: All data from CL from routine sampling (CL only).
  - Pool_Carbon_Routine_DOC: Piezo soil water DOC data at different depths (CL only).
  - Pool_Carbon_Routine_Colour: Piezo soil water colour data at different depths (CL only).
  - Pool_Carbon_Routine_Depth: Pool depth on sampling day from continuous loggers (CL only).
  - Pool_Carbon_Routine_Soil: Bulked soil solution data (CL only).
- Site codes: CL, LL, MU (Loch Lier, Munsary, Cross Lochs).
- Pool types: NAT = natural pools; ART = artificial/restoration pools.
- Temporal coverage: 2013–2015, with quarterly sampling and routine measurements.

## Variables and measurements (selected highlights)
- Physical/chemical pool properties (per quarterly dataset):
  - pH; EC (µS/cm); DO (mg/L); Water Temp (°C); abs254; SUVA (l/mg/m); E4E6 ratio (465/665).
  - DOC (mg/L); POC (mg/L); CH4 (µg/L); CO2 (mg/L).
  - Pool area (m²); Pool depth (cm); Pool volume (m³).
- Routine dataset (per pool and time):
  - DOC_BASE, DOC_INFLOW, DOC_OUTFLOW, DOC_SURFACE, DOC_OLF (all mg/L).
  - pH; EC (µS/cm); DO (mg/L); Water Temp (°C); WTD (cm; water-table depth in dipwell).
  - POC (mg/L); CH4 (µg/L); CO2 (mg/L); abs254; SUVA; E4E6.
  - Pool physicals: Pool area (m²); Pool depth (cm); Pool volume (m³).
- Depth and soil-focused datasets:
  - Pool_Carbon_Routine_Depth: Depth below peat (cm) for each pool sampling event.
  - Pool_Carbon_Routine_DOC/Colour/Soil: Depth-specific DOC and optical properties in soil solution or piezometer contexts.
- Data fields are described with units and meanings in each file’s metadata (e.g., Year, Date, Week; Pool; Treat/NAT/ART; Depth; etc.).

## Spatial and temporal scope
- Spatial: Three sites across Scotland: Loch Lier (LL), Cross Lochs (CL), Munsary (MU).
- Temporal: Samples collected between 2013 and 2015, with quarterly time points and additional routine measurements for CL.

## Data quality and provenance
- Data QC applied; values below detection limits flagged/handled as part of quality control.
- Methods and data generation are documented in the referenced Hydrological Processes 2022 manuscript.

## GIS applications and workflows
- Suitable for map-based visualization of carbon dynamics across peatland pools:
  - Visualize spatial distribution of DOC, POC, CH4, CO2, and optical properties (abs254, SUVA, E4E6) across sites and across time.
  - Integrate pool-level metrics (area, depth, volume) with water chemistry for habitat and carbon cycling analyses.
  - Combine quarterly pool data with routine/soil measurements to create multi-resolution GIS layers (surface water vs. soil solution vs. piezometer data).
  - Use depth-related fields (Depth below peat; WTD) to analyze vertical carbon transport in peatland hydrology.
- Practical considerations:
  - Data come from multiple datasets with different resolutions (quarterly vs routine) and slightly different variable sets; align datasets by site, pool, and time (Year/Date/Week) for GIS analysis.
  - Join by Pool, Site, Year/Date/Week to create comprehensive time-series maps or layer stacks.

## Access and usage notes
- Data organized in six CSV files with explicit field descriptions and units.
- Primary use: map-based data visualizations and GIS-driven analyses of carbon concentrations and related hydrological/optical properties in blanket peatlands.