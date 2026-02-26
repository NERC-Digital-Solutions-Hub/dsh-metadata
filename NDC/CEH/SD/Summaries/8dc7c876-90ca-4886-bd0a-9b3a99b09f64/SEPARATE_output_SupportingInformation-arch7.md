# Source apportionment of annual nutrients and sediment loads to rivers in England and Wales modelled with SEPARATE

- Overview
  - Dataset of annual loads of nitrogen, phosphorus (total and dissolved), and fine-grained sediment to rivers in England and Wales.
  - Modelled with SEPARATE version 2 (SEctor Pollutant AppoRtionment for the AquaTic Environment).
  - Emissions are summarized by non-coastal Water Framework Directive (WFD) Cycle 2 waterbodies, covering individual and cumulative waterbodies.

- Spatial scale and scope
  - At WFD waterbody Cycle 2 scale; non-coastal waterbodies.
  - Emissions are provided for both diffuse and point sources to rivers.
  - The dataset enables mapping in GIS by linking to WFD Cycle 2 shapefiles.

- SEPARATE description
  - SEPARATE is a multi-pollutant source apportionment framework for England and Wales.
  - Contains emissions from diffuse sources (agriculture, urban, river channel banks, atmospheric deposition, groundwater) and point sources (STWs, septic tanks, CSOs, storm tanks).
  - Pollutant emissions are provided for nitrogen, phosphorus (total and dissolved), and sediment.

- Pollutant emission sources and methodology (high-level)
  - Diffuse agricultural: uses the ADAS Agricultural Pollutant Transfer framework built on PSYCHIC/NIPPER models; inputs include soils, weather, elevation, crop data, field boundaries, manure distribution, and fertiliser practices.
  - Diffuse urban: combines annual urban runoff (Wallingford Modified Rational Method) with representative event mean concentrations.
  - River channel banks: estimated via a national-scale bank erosion index based on river regime, shear stress, sinuosity, and network density.
  - Direct atmospheric deposition: nitrogen from NEAP-N; phosphorus from rainfall-derived concentrations and rainfall amounts.
  - Sewage treatment works (STWs): emissions from a national register of consented discharges with measured flows and concentrations; very small or data-less STWs excluded.
  - Septic tanks: phosphorus emissions from recent EA studies.
  - Combined sewer overflows (CSOs) and storm tanks: emissions estimated from overflow mechanisms, rainfall-driven discharge modeled relative to dry-weather flow.
  - Groundwater: included for nitrogen and dissolved phosphorus via specific input assumptions.

- Data inputs and assembly
  - Integrates multiple data sources (agriculture, urban runoff, river banks, deposition, wastewater, septic, CSOs, storm tanks, groundwater).
  - Emissions are aggregated to waterbody scale for policy support and local decision-making.

- Format and GIS usage
  - Stored in CSV format; can be mapped in GIS by joining to WFD River Waterbody Catchment Cycle 2 shapefiles (join via EA_WB_ID).
  - Columns include location metadata (region, catchment, waterbody name and ID, local and cumulative areas) and pollutant load data.
  - Pollutants are represented with coding such as X for pollutant type, with local (L) and cumulative (C) tallies, and subdivisions for undisturbed (untreated) versus mitigated values where applicable.
  - Example column groups:
    - Local year/totals: X_au_L_t, X_am_L_t, X_be_L_t, X_ur_L_t, X_sw_L_t, X_st_L_t, X_sc_L_t, X_so_L_t, X_dd_L_t, X_to_L_t
    - Cumulative totals: X_au_C_t, X_am_C_t, X_be_C_t, X_ur_C_t, X_sw_C_t, X_st_C_t, X_sc_C_t, X_so_C_t, X_dd_C_t, X_to_C_t
    - Local/ cumulative percentages: X_am_L_p, X_be_L_p, X_ur_L_p, etc., and X_am_C_p, X_be_C_p, X_ur_C_p, etc.
  - Units include tons per year (loads) and percentages for composition.

- Uncertainty and caveats
  - Results are national-scale estimates with local-scale applicability limitations.
  - Waterbodies with area <25 km2 (about 43% of waterbodies) should be treated with caution due to data accuracy.
  - Agricultural baseline reflects 2010–2012 mitigation levels; a no-mitigation baseline is included for comparison.
  - STW emissions are based on monitored data but small or poorly documented works introduce uncertainty; some estuarine/coastal outfalls are not included.
  - Channel bank contributions do not account for margin protection works.
  - Temporal coverage varies by sector (e.g., agric 2010 vs. 2010–2012 for STWs); SEPARATE uses the most up-to-date data available at the time.

- Supporting documentation
  - Documentation and data provenance available via CEH catalogue and cited references, including methodological sources for each pollutant source and model component.

- Practical use for GIS specialists
  - Enables creation of map-based data products showing spatial distribution of pollutant loads by waterbody.
  - Supports policy delivery analysis under the Water Framework Directive with national-to-local applicability.
  - Provides a structured, joinable data model to enrich GIS waterbody datasets with pollutant source contributions and scenario comparisons.