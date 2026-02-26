# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Ammonia (NH3) enhancement experiment conducted in a Birch plantation at Glencorse woodland to study NH3 effects on forest ecosystems.
- NH3 release is wind-controlled (275–345 degrees) and activated at threshold wind speeds; monitoring performed with Adapted Low-cost Passive High Absorption (ALPHA) samplers.
- Measurements include monthly NH3 concentrations and vertical concentration gradients used to drive a dry deposition model across canopy layers.
- Deposition fluxes are estimated for soil, understory vegetation, tree trunks, and tree canopy using a four-layer canopy bi-directional resistance model.

## Spatial and temporal coverage
- Location: Glencorse experimental site, near Edinburgh, UK (latitude 55.8539°, longitude -3.2151°; altitude 200 m).
- Timeframe: September 2021 to December 2022 for concentration data; deposition modelling spans the same period.
- Spatial arrangement: monitoring quadrats with measurements at varying distances from the NH3 enhancement source; distance is signed (negative = southwest, positive = northeast).

## Data collection and processing (GIS-ready)
- NH3 concentrations measured at 1.5 m height along the monitoring transect.
- Vertical NH3 concentrations recorded at 25 cm intervals from 5 cm above ground at 4, 10, and 16 m distances from the enhancement system.
- Data used to parameterize a four-layer canopy deposition model:
  - Soil surface deposition (R_bg), tree trunks (Rb(tt)), stomatal deposition (Rs), and cuticular deposition (Rw) with multiple parameterizations.
  - Bi-directional exchange accounted for stomatal compensation point and soil re-emission.
- Data cleaning: visual QA to remove instrument malfunctions, datalogger issues, and power-cut artifacts; missing values linked to power interruptions or sensor replacements.
- Data structure: 126 measurements comprising 17 parameters; stored in CSV with clearly defined fields.

## Data structure and fields (selected highlights)
- Distance (m): position from NH3 source; negative = southwest, positive = northeast.
- Month: year-month of measurement.
- NH3_conc_measured (µg m^-3): monthly average NH3 concentration at 1.5 m height along transect.
- NH3_conc_soil (µg m^-3): modeled monthly average NH3 concentration at soil surface (0.05 m).
- NH3_conc_us (µg m^-3): modeled monthly NH3 concentration in understory layer (0.5 m).
- NH3_conc_ts (µg m^-3): modeled monthly NH3 concentration at trunk surfaces (1.75 m).
- NH3_conc_tc (µg m^-3): modeled monthly NH3 concentration in tree canopy (3.5 m).
- Deposition fluxes (kg ha^-1) for various surfaces and components, including:
  - Fg (soil deposition flux)
  - Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (understory deposition: stomatal and cuticular parameterizations)
  - Fd_us (understory cuticular deposition, Sutton parameterization)
  - Ftt, Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc (canopy/trunk deposition and related parameterizations)
- Each flux type includes positive values (deposition) and negative values (emission) when applicable.
- The dataset integrates multiple parameterizations (Massad et al. 2010; Jones et al. 2007; DEPAC module van Zanten et al. 2010; Sutton et al. 1998) for comparative analysis.

## Data quality and limitations
- Visual QA conducted; obvious errors removed; some gaps due to scheduled power cuts or sensor replacements.
- Resolution is constrained to the measurement period (monthly averages for NH3_conc_measured) and specific vertical/horizontal sampling configurations.
- Data represent a controlled NH3 enhancement scenario and are most applicable to similar forest canopy contexts or to validate deposition models under wind-controlled release.

## GIS and visualization opportunities
- Map NH3 concentration and deposition flux along the transect as spatial lines or along transect distance from the source.
- Create 2D/3D surfaces showing NH3 concentration by distance and height (using vertical profiles at 0.05 m, 0.5 m, 1.75 m, and 3.5 m).
- Compare deposition components (soil, understory, trunks, canopy) using separate layers or a composite deposition map.
- Time-series visualizations by month to show temporal trends in measured concentrations and modeled deposition.
- Integrate with forest structure data (LAI, canopy height, roughness) for enhanced spatial interpretation and exposure assessment.

## Access, funding, and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- References for methodologies and parameterizations include classical and contemporary deposition models (e.g., Chamberlain; Fowler; Nemitz; Massad; Jones; Sutton; van Zanten) and the DEPAC module.
- Data are provided as CSV with clearly described columns and units, suitable for importing into GIS and data visualization tools.