# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

## Overview
- Purpose: dataset on ammonia concentration and multi-pathway deposition to forest components to support GIS-based analysis and map-making.
- Location: Queensberry Estate, central Sri Lanka; coordinates 6.9693°, 80.5911°, altitude 1645 m.
- Period: January 2023 – December 2024.
- Measurements: NH3 concentration at 1.5 m height along monitoring quadrats using ALPHA samplers; deposition flux estimated for soil, understory, tree trunks, and tree canopy via a bi-directional resistance model.
- Data product focus: spatially-resolved, distance-based NH3 concentration and deposition flux across defined directions from the release source.

## Methods and Modelling
- NH3 enhancement system: wind-controlled release; activated when wind direction falls within monitoring quadrats (5-75°, 185-255°) and at threshold speeds (0.3–10 m s-1).
- Core deposition model: Fχ(z) = χa / Rt, where Rt is the total resistance to dry deposition.
- Deposition components:
  - Soil surface: resistance Rbg (quasi-laminar boundary layer)
  - Tree trunks: resistance Rb(tt) (quasi-laminar boundary layer)
  - Stomatal deposition: Rs (with LAI dependency)
  - Cuticular deposition: Rw with multiple parameterizations; includes day/night variants and LAI effects
  - Capacitance: Rd (for epicuticular film capacitance)
- Rw parameterizations (selected per pathway):
  - Massad et al., 2010
  - Jones et al., 2007
  - DEPAC module (van Zanten et al., 2010)
  - Sutton et al., 1998
- Day vs. night parameterizations and DEPAC module usage; LAI-based adjustments throughout.
- Model improvement: replaces mean monthly NH3 conc. with a dynamic model that peaks during release periods; ambient NH3 drives deposition when not releasing.
- Data scope: extension and improvement relative to 2022 dataset from the same site.

## Data Structure and Variables
- Dataset size: 816 measurements, 13 parameters (CSV format).
- Key columns (examples):
  - Distance (m): distance from NH3 source; sign indicates direction (southwest negative, northeast positive)
  - Month: year-month
  - NH3_conc (µg m^-3): monthly average ambient NH3 concentration at 1.5 m
  - Fg: cumulative NH3 deposition flux to soil (kg ha^-1)
  - Fs_us: cumulative stomatal deposition to understory (kg ha^-1)
  - Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones: understory cuticular deposition (kg ha^-1) via respective parameterizations
  - Fd_us: understory cuticular deposition (kg ha^-1) via Sutton et al. parameterizations
  - Ftt: cumulative deposition to tree trunks (kg ha^-1)
  - Fs_tc: stomatal deposition to tree canopy (kg ha^-1)
  - Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones: trunk cuticular deposition (kg ha^-1) via parameterizations
  - Fd_tc: trunk cuticular deposition (kg ha^-1) via Sutton et al. parameterizations
- Units and interpretation: flux values are cumulative; negative flux = emission.
- Spatial-Temporal context: measurements along two quadrats with a directional distance gradient; sampling at 1.5 m height.

## Quality Control and Limitations
- Visual quality control; removal of obvious instrument- or logger-related errors.
- Gaps: regular interval missing values due to scheduled power cuts; some gaps from sensor replacement.

## Spatial and Temporal Context for GIS
- Spatial setup: distance-based gradient from NH3 release source; two monitoring directions with sign indicating orientation.
- Temporal coverage: monthly data across 2023–2024.
- Metadata: site coordinates and altitude; compatible with integrating canopy LAI, topography, and land-cover layers for richer spatial analyses.

## Data Reliability and Documentation
- Dataset represents an improved modelling approach that captures NH3 peaks during release periods.
- Related publications: Deshpande et al. (2024a, 2024b) and supporting references on deposition resistance models.
- Funding: UKRI GCRF South Asian Nitrogen Hub.

## GIS Applications and Data Products
- Enables map-based visualization of NH3 concentration and multi-pathway deposition flux by distance and time.
- Facilitates creation of separate map layers for:
  - NH3_conc
  - Soil (Fg), understory (Fs_us, Fw_us variants, Fd_us)
  - Tree trunks (Ftt, Fw_tc variants, Fd_tc)
  - Tree canopy (Fs_tc, Fw_tc variants)
- Allows integration with LAI, canopy height, and other environmental covariates to analyze spatial patterns and deposition risk.
- Clear emission vs deposition indicators assist in dynamic mapping of periods when NH3 is released versus deposited.