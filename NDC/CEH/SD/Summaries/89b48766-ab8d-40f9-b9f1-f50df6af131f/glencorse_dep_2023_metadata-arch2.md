# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

## Aim and scope
- Document and summarize ammonia (NH3) concentration and deposition data from the Glencorse experimental site near Edinburgh (Birch woodland), established in 2022 to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
- Provides an extended dataset (2023) with improved deposition modeling and a four-layer canopy framework, building on a 2022 dataset.

## Data collection and experimental design
- Location and setup:
  - Glencorse woodland, ~55.8539°N, -3.2151°W, altitude ~200 m.
  - NH3 enhancement system controlled by wind conditions measured below canopy; NH3 released only when wind direction is 275–345° and speed threshold ≥ 0.31 m s−1.
- Measurements:
  - NH3 concentrations measured at 1.5 m height along the monitoring quadrat using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers.
  - Analyzed monthly from January 2023 to December 2024.
- Purpose of measurements:
  - Quantify ambient NH3 during release periods and background periods to assess concentration and deposition processes across different forest strata.

## Modeling approach for deposition and flux calculations
- Bi-directional canopy model:
  - Four-layer canopy compensation point model accounting for stomatal exchange and soil re-emission.
  - Deposition flux Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is total resistance to dry deposition (inverse of deposition velocity Vd).
- Layer-specific deposition resistances:
  - Soil surface: soil boundary layer resistance Rbg (quasi-laminar boundary layer).
  - Tree trunks: quasi-laminar boundary layer around trunks (Rb(tt)).
  - Tree canopy and understorey: stomatal deposition flux via stomatal resistance Rs, with LAI dependence.
  - Cuticular deposition: multiple parameterizations (Rw) with LAI dependency; four variants including day/night parameterizations and DEPAC module integration (for acidifying compounds).
- Parameterizations and references:
  - Rw variants drawn from Massad et al. (2010), Jones et al. (2007), Sutton et al. (1998), DEPAC module (van Zanten et al., 2010), and other foundational works (Owen & Thomson 1963; Schuepp 1977; Nemitz et al. 2000).
  - LAI dependencies and phenology incorporated; day–night distinctions based on solar radiation.
  - DEPAC module used for one of the cuticular parameterizations (DEPAC/DEPosition of Acidifying Compounds).
- Model improvements:
  - Replaces the previous approach (relying on mean monthly NH3 concentrations) with a model that simulates NH3 concentration peaks during release periods to better estimate deposition during NH3 release.

## Quality control and data integrity
- Visual quality checks performed; obvious instrument errors, datalogger issues, and power-cut–related gaps removed.
- Missing values attributed to scheduled power cuts; some gaps also due to sensor replacement.
- Data are stored as a CSV with structured fields and documented units.

## Data structure and dataset contents
- Dataset size: 108 measurements of 17 parameters.
- Core columns (examples):
  - Distance (m), Distance description (positive toward northeast, negative toward southwest).
  - Month (year-month).
  - NH3_conc_measured (µg m−3): monthly average ambient NH3 concentration at 1.5 m along transect (ALPHA samplers).
  - NH3_conc_soil, NH3_conc_us, NH3_conc_ts, NH3_conc_tc (µg m−3): modeled NH3 concentrations at soil surface, understory, trunk surfaces, and tree canopy heights respectively.
  - Deposition fluxes to various targets (kg ha−1): Fg (soil deposition), Fs_us (stomatal deposition to understory), Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones (cuticular deposition to understory via different parameterizations), Fd_us (cuticular deposition to understory via Sutton et al. parameterization), Ftt (deposition to tree trunks), Fs_tc (stomatal deposition to canopy), Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones (canopy cuticular), Fd_tc, with versions indicating alternative parameterizations and negative values indicating emission.
- Data description details:
  - Distance describes distance from NH3 enhancement source.
  - NH3_conc_* fields describe modeled or measured concentrations at different forest compartments.
  - F* fields capture cumulative NH3 deposition or emission across the respective compartments using various parameterizations.

## Data availability, usage, and lineage
- This dataset is an extension and improvement over a 2022 dataset from the same site.
- Key methodological advancement: deposition peaks during NH3 release are now simulated to improve deposition estimates during release rather than relying on monthly means.
- Funding:
  - UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme (NE/Y006208/1).
- References and context:
  - Foundational work on gas transport and deposition resistance (Chamberlain; Schuepp; Wesely & Hicks; others).
  - Specific parameterizations and datasets cited for NH3 exchange and LAI-dependent deposition models (Massad et al., Jones et al., Sutton et al., Nemitz et al., DEPAC module).

## Relevance for environmental monitoring and analysis
- Provides standardized, QA’d NH3 concentration and deposition data with a transparent, multi-layer deposition model suitable for cross-site comparisons and temporal trend analysis.
- Enables integration with vegetation and soil response data to assess environmental health and policy performance over time.
- Demonstrates data stewardship practices: clear data structure, explicit deposition modeling framework, and accessibility of underlying model parameters for reuse and validation.