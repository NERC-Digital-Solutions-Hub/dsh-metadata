# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2022)

## Overview
- Purpose: Investigate the effects of elevated ambient ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil in a tropical sub-montane forest in Sri Lanka.
- Study site: Queensberry Estate, central Sri Lanka (coordinates and altitude provided in the text).
- Experimental design: NH3 enhancement system controlled by wind direction and threshold speeds; NH3 released only when wind aligns with monitoring quadrats.
- Measurements: NH3 concentrations measured at 1.5 m height along monitoring quadrats using UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; monthly analyses from April to December 2022.
- Modelling approach: Bi-directional resistance model to estimate NH3 deposition (and emission) to soil, understory vegetation, tree trunks, and tree canopy using a four-layer canopy compensation point framework.
- Outputs: Deposition fluxes to different surfaces, calculated via specified resistances and ambient NH3 concentrations.

## Data collection and deposition modelling
- Data collection details:
  - NH3 enhancement experiment conducted in 2022; wind-controlled release conditions.
  - Measurement height: 1.5 m; sampling along monitoring quadrats.
  - Sampling frequency: Monthly from April to December 2022.
- Modelling components:
  - Deposition flux Fχ(z) = χa / Rt, where Rt is total resistance to dry deposition.
  - Soil surface deposition via soil boundary layer resistance Rbg.
  - Tree trunks via quasi-laminar boundary layer resistance Rb(tt).
  - Stomatal deposition via stomatal resistance Rs with Leaf Area Index (LAI) dependency.
  - Cuticular deposition fluxes via multiple Rw parameterizations and one Rd (capacitance) parameterization for comparison.
  - Four Rw parameterizations with day/night variants and LAI dependence; DEPAC module (van Zanten et al. 2010) included.
  - Additional parameterizations incorporate semi-empirical relationships (e.g., Massad et al., Jones et al., Sutton et al.) and environment-specific LAI Haarweg values.
- Outputs and data relationships:
  - Deposition to soil, understory, and canopy surfaces computed through respective resistances.
  - Includes emissions indicators (negative flux) where applicable.

## Data structure and quality control
- Dataset size and structure:
  - 144 measurements across 13 parameters.
  - Data provided as a CSV file with clearly defined columns.
- Key columns (examples):
  - Distance (m): Distance from NH3 enhancement source; sign indicates direction (negative southwest, positive northeast).
  - Month: Month and year.
  - NH3_conc (µg m^-3): Monthly average NH3 concentration at 1.5 m height.
  - Fg: Cumulative NH3 deposition flux to soil surface.
  - Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones: Cumulative stomatal and cuticular deposition flux to understory vegetation from various parameterizations.
  - Fd_us: Cumulative cuticular deposition flux to understory vegetation (Sutton 1998 parameterization).
  - Ftt: Cumulative deposition flux to tree trunks.
  - Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc: Corresponding fluxes for the tree canopy.
- Data quality and governance:
  - Visual quality checks conducted; obviously erroneous data removed (instrument malfunctions, datalogger issues, power cuts).
  - Regular gaps due to scheduled power cuts; some missing values due to sensor replacement.
- Completeness note:
  - Complete methodological and analytical details linked to Deshpande et al. (2024).

## Data availability, usage, and provenance
- Availability: Dataset provided as CSV with explicit units and descriptions for each variable, enabling reuse and cross-comparison.
- Documentation and methodology: Complete details of experimental design, methodology, analysis, and findings available in Deshpande et al. (2024).
- Funding: UKRI GCRF South Asian Nitrogen Hub supported the facility.
- References: Includes foundational works on deposition resistances and modelling (e.g., Chamberlain, Fowler, Massad et al., Nemitz et al., Jones et al., Sutton et al., van Zanten et al., and others).

## Implications for data strategy and stewardship
- Demonstrates a well-structured, multi-parameter data collection and modelling workflow, useful for data leaders focusing on end-to-end data lifecycle:
  - Clear data schema with unit metadata and directional distance encoding enhances discoverability and reuse.
  - Bi-directional deposition modelling integrates multiple data streams (NH3 concentrations, meteorological-like parameters, LAI, and surface resistances), illustrating cross-domain data integration.
  - Quality control practices highlight the importance of documenting data gaps and reasons (power outages, sensor replacements) for transparent provenance.
- Opportunities for improvement and standardization:
  - Consolidate metadata to improve cross-site comparability (e.g., standardized parameter naming, units, and measurement heights).
  - Provide a data dictionary and lineage to trace how each flux value was computed from resistances and NH3 concentrations.
  - Consider broader data sharing with a repository to enhance discoverability across nitrogen and atmospheric deposition communities.
- User-centric relevance:
  - The dataset supports policy-relevant assessments of NH3 deposition and emission dynamics in forest ecosystems.
  - The structured outputs (fluxes by surface and parameterization) facilitate scenario analyses and sensitivity testing for data-informed decision-making.