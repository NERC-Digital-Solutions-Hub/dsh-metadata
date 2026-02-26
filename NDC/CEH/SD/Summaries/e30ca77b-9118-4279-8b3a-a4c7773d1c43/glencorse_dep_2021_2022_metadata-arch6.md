# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Experimental study at Glencorse woodland near Edinburgh to examine ammonia (NH3) enhancement effects on forest ecosystems.
- NH3 release is wind-controlled, targeting specific wind directions and threshold speeds to study deposition and emission over canopy layers.
- Data support goal: provide measurements and modeled deposition fluxes that can be explored and reused for data-driven insights into NH3 exchange with vegetation.

## Data Collection and Measurements
- Location and setup: Birch plantation at Glencorse site (55.8539°, -3.2151°, altitude 200 m); enhancement system activated when wind blows from 275–345° toward monitoring quadrats.
- Release control: NH3 released only under threshold wind speeds of 0.310 m/s.
- NH3 concentration measurements:
  - Height: 1.5 m along the monitoring transect using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers.
  - Time: monthly analyses from September 2021 to December 2022.
- Vertical concentration profiling:
  - Measurements at every 25 cm interval from 5 m to 3.5 cm above ground at distances of 4, 10, and 16 m from the enhancement source.
  - Used to parameterize vertical concentration gradients for canopy-layer modeling.
- Modeling scope:
  - Four-layer canopy compensation point model to estimate NH3 deposition and soil/understory/canopy/tree interactions.
  - Bi-directional resistance framework accounting for stomatal exchange and soil re-emission.

## Data Structure and Quality Control
- Dataset composition:
  - 126 measurements across 17 parameters.
  - Provided as a CSV file with columns including Distance (m), Month, NH3 concentrations at multiple heights/locations, and various deposition fluxes.
- Parameters include:
  - NH3_conc_measured (1.5 m height, transect), NH3_conc_soil (0.05 m), NH3_conc_us (0.5 m), NH3_conc_ts (1.75 m), NH3_conc_tc (3.5 m canopy), and cumulative deposition/flux components (Fg, Fs_us, Fw_us_* etc. for different parameterizations).
- Quality control:
  - Visual checks; removal of obvious instrument/mislogging errors and power-cut induced gaps.
  - Regularly missing values attributed to scheduled power cuts; some data gaps from sensor replacement.
- Data structure specifics:
  - Columns include distance from NH3 source, month, and multiple NH3 concentration estimates and deposition fluxes (positive values for deposition, negative for emission).

## Modeling and Calculations
- Deposition framework:
  - Deposition flux at height z: Fχ(z) = χa / Rt (where χa is ambient NH3 concentration and Rt is total resistance to dry deposition).
  - Soil surface deposition uses soil boundary layer resistance Rbg, with parameterization involving wind, roughness, and boundary-layer concepts.
  - Tree trunks and canopy deposition use quasi-laminar boundary layer resistances (Rb(tt)) and related formulations with Friction velocity (u*), Schmidt number (Sc), and Reynolds number (Re*).
  - Stomatal deposition flux modeled via Rs, incorporating leaf area index (LAI) dependency.
  - Cuticular deposition flux considered with multiple parameterizations (Rw) and integrated LAI dependence; four parameterizations evaluated:
    1) Rw(min) and growth factors with LAI scaling (Massad et al., 2010)
    2) Rw(day) and Rw(night) using ambient NH3 and LAI
    3) DEPAC-based module (van Zanten et al., 2010) with LAI Haarweg
    4) Rw dependent on canopy LAI and environmental factors
- Additional components:
  - Stomatal deposition flux Rs parameterized with RsMax, RsMin, and alpha/ rad factors (including solar radiation).
  - Cad and capacitance-related term Rd for cuticular deposition (with reference to Sutton et al., 1998).
- Summary: The study uses a four-layer canopy bi-directional exchange model combining soil, understory, trunk, and canopy processes, with multiple deposition parameterizations to explore sensitivity of NH3 fluxes to LAI, light, temperature, humidity, and growth stage.
- References embedded in methodology include foundational works (Chamberlain; Fowler; Nemitz; Massad; Jones; DEPAC; Sutton; van Zanten; Wesely) for deposition resistance modeling and parameterizations.

## Data Availability and Access
- Data are organized in a CSV file with clear variable descriptions per column (distances, months, NH3 concentration estimates by height/location, and cumulative deposition fluxes across layers and parameterizations).
- Complete methodology and modeling details are documented in Deshpande et al. (2024); foundational equations and parameterization sources are cited within the document.
- Timeframe: NH3 enhancement experiment data and analyses collected from September 2021 through December 2022.

## Potential Data Products and Use
- Self-serve dashboards or pivot-table style explorations of NH3 concentrations by distance, height, and month, plus corresponding deposition fluxes.
- Comparative analyses of different Rw parameterizations to assess sensitivity of deposition estimates to canopy phenology (LAI) and environmental conditions.
- Visualizations of vertical NH3 concentration gradients used to drive canopy deposition modeling.
- Data merging opportunities with other NH3 datasets to study regional deposition patterns, especially in forested ecosystems.
- Reuse in policy-support contexts that require quantified NH3 deposition to forestry ecosystems or validation of bi-directional exchange models.

## Funding
- Supported by UKRI GCRF South Asian Nitrogen Hub for establishing the facility and data collection.

## References and Provenance
- Methodological and modeling references underpinning deposition resistances and bi-directional NH3 exchange (e.g., Chamberlain; Fowler; Nemitz; Massad; Jones; Massad et al.; DEPAC module; Sutton; van Zanten; Wesely & Hicks) with a complete methodological description available in Deshpande et al. (2024).