# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

## Purpose and context
- Studies the effects of elevated atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil.
- Location: Queensberry Estate, central Sri Lanka (6.9693°, 80.5911°, altitude 1645 m).
- Experiment setup: NH3 enhancement controlled by wind direction and threshold speeds (0.3–10 m s^-1); NH3 measured at 1.5 m height along monitoring quadrats.
- Sampling period: Monthly analyses from January 2023 to December 2024 using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers.
- Modelling goal: Estimate NH3 deposition (and emission) to soil, understory vegetation, tree trunks, and tree canopy using a four-layer canopy bi-directional resistance model.

## Data collection and modelling approach
- Measurements include ambient NH3 concentrations and deposition fluxes to different surface types.
- Deposition flux modelling uses a bi-directional resistance framework with:
  - Fχ(z) = χa / Rt (deposition flux at height z)
  - Fluxes to soil (Rbg), tree trunks (Rb(tt)), stomatal deposition (Rs), and cuticular deposition (Rw) via multiple parameterizations.
- Key components and parameterizations:
  - Soil boundary layer resistance (Rbg)
  - Tree trunk boundary layer resistance (Rb(tt))
  - Stomatal resistance (Rs) with leaf-area index (LAI) dependency
  - Multiple cuticular deposition parameterizations (Rw), including Massad et al. (2010), Jones et al. (2007), DEPAC module (van Zanten et al., 2010), and a Stutton et al. (1998) capacitance-based approach
  - Four Rw schemes with day/night variations and LAI dependencies
  - A DEPAC module for enhanced deposition parameterization
- Model advancement: The current dataset uses a mechanism that simulates NH3 concentration peaks during release periods to estimate deposition, while ambient concentration drives deposition when releases are inactive. This is an improvement over a prior version that used mean monthly NH3 concentrations for all intervals.
- Quality control and data cleaning: Visual checks; removal of instrument/ datalogger/power-cut errors; gaps due to power outages or sensor replacement.

## Data structure and contents
- Dataset size: 816 measurements of 13 parameters.
- File format: CSV.
- Columns and meaning:
  - Distance (m): Distance from NH3 enhancement source; negative = southwest, positive = northeast.
  - Month: Month and year.
  - NH3_conc (µg m^-3): Monthly average NH3 concentration at 1.5 m height from ALPHA samplers.
  - Fg (kg ha^-1): Cumulative NH3 deposition flux to soil (negative = emission).
  - Fs_us (kg ha^-1): Cumulative NH3 stomatal deposition flux to understory vegetation (negative = emission).
  - Fw_us_Massad (kg ha^-1): Cumulative NH3 cuticular deposition flux to understory (Massad et al., 2010).
  - Fw_us_DEPAC (kg ha^-1): Cumulative NH3 cuticular deposition flux to understory (DEPAC module).
  - Fw_us_Jones (kg ha^-1): Cumulative NH3 cuticular deposition flux to understory (Jones et al., 2007).
  - Fd_us (kg ha^-1): Cumulative NH3 cuticular deposition flux to understory (Sutton et al., 1998).
  - Ftt (kg ha^-1): Cumulative NH3 deposition flux to tree trunks.
  - Fs_tc (kg ha^-1): Cumulative NH3 stomatal deposition flux to the tree canopy.
  - Fw_tc_Massad (kg ha^-1): Cumulative NH3 cuticular deposition flux to the tree canopy (Massad et al., 2010).
  - Fw_tc_DEPAC (kg ha^-1): Cumulative NH3 cuticular deposition flux to the tree canopy (DEPAC module).
  - Fw_tc_Jones (kg ha^-1): Cumulative NH3 cuticular deposition flux to the tree canopy (Jones et al., 2007).
  - Fd_tc (kg ha^-1): Cumulative NH3 cuticular deposition flux to the tree canopy (Sutton et al., 1998).
- Notes:
  - Negative flux values indicate emission in all deposition-flux columns.
  - The 13-parameter set refers to NH3 concentration plus 12 deposition-flux components; Distance and Month are metadata columns accompanying the primary 13-parameter data.

## Site, timeframe, and provenance
- Site details: Queensberry Estate, central Sri Lanka; altitude 1645 m.
- Dataset is an extension of the 2022 dataset from the same site.
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).

## Data availability and usage guidance
- Data format and structure support easy integration into dashboards or self-serve analysis workflows.
- Clear documentation of deposition pathways (soil, understory, tree trunks, and canopy) and multiple parameterizations enables cross-method comparisons and sensitivity analyses.
- Useful for:
  - Evaluating bi-directional NH3 exchange processes in tropical forest ecosystems.
  - Cross-site comparisons with Sri Lanka and Scotland datasets (as per related publications).
  - Informing ecological risk assessments and policy discussions on ammonia deposition impacts.
- References for methodology and context are provided, including foundational parameterizations and the DEPAC module.

## Relevance to data-support practice
- Clear “ask-driven” data product: combines NH3 concentrations with multi-compartment deposition flux estimates to enable end users to explore ammonia dynamics and deposition pathways.
- Data quality notes and a transparent improvement history (peak/deposition coupling) support trust and reuse.
- Dataset aligns with goals to produce usable data products (e.g., dashboards, reports) and to promote wider sharing and reuse of outputs.