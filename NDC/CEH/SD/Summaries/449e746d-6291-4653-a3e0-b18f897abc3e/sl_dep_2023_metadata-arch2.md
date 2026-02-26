# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

## Overview
- Purpose: Investigate effects of high atmospheric ammonia (NH3) on forest vegetation, bryophytes, lichens, and soil in a tropical sub-montane forest.
- Location: Queensberry Estate, central Sri Lanka (6.9693° N, 80.5911° E; altitude 1645 m).
- Experimental setup: NH3 enhancement system controlled by wind conditions to release NH3 when wind directs toward monitoring quadrats (threshold speeds 0.3–10 m s⁻¹; azimuth windows 5–75° and 185–255°).
- Data collected: NH3 concentrations measured at 1.5 m height along two monitoring quadrats using UK CEH Adapted Low-cost Passive High Absorption (ALPHA) samplers; analyzed monthly from January 2023 to December 2024.
- Deposition estimation: Uses a four-layer canopy compensation point model (bi-directional resistance) to estimate NH3 deposition (and emission) to soil, understory vegetation, tree trunks, and tree canopy.
- Outputs: Deposition fluxes to soil, understory, and tree components; multiple parameterizations (Massad et al. 2010; Jones et al. 2007; DEPAC module 2010; Sutton et al. 1998) to compare deposition forms (stomatal, cuticular) and to allow for phenological LAI effects.
- Major improvement: Model now simulates NH3 concentration peaks during release to estimate deposition, rather than driving deposition with mean monthly concentrations.
- Dataset lineage: Extension of the 2022 Queensberry dataset; aligned with prior work on NH3 deposition estimation in Scotland and Sri Lanka.
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).

## Methods

### Data collection and experimental design
- Site and timing: Ammonia enhancement experiment established in 2022; data analyzed Jan 2023–Dec 2024.
- Release control: NH3 released only when wind direction aligns with monitoring quadrats; azimuth and wind thresholds ensure targeted exposure.
- Measurement setup: NH3 concentration measured at 1.5 m height along both quadrats using ALPHA samplers; monthly analyses.

### Deposition modeling
- Core model: Bi-directional resistance framework with canopy compensation point for NH3 exchange.
- Deposition flux formula: Fχ(z) = χa / Rt, where χa is ambient NH3 concentration at height z and Rt is total resistance to dry deposition.
- Soil deposition: Rbg parameterized via quasi-laminar boundary layer resistance; dependent on friction velocity, canopy roughness, and aerodynamic terms.
- Tree trunk deposition: Rb(tt) parameterized via boundary-layer resistance around trunks; involves Reynolds and Schmidt numbers and related factors.
- Stomatal deposition: Rs parameterized with LAI dependency and bounds (RsMax, RsMin, radiance terms).
- Cuticular deposition: Fluxes estimated using multiple parameterizations (Rw) with LAI scaling and environmental factors; includes day/night variants and additional DEPAC-based formulations.
- DEPAC and LAI: DEPAC module used for one Rw formulation; HAAR-like LAI adjustments included for phenology.
- Day/night handling: Day parameterizations activated when solar radiation > 5 W m⁻²; night parameterizations when < 5 W m⁻².
- Parameterizations included: 
  - Massad et al. 2010 (multiple Rw forms)
  - Jones et al. 2007
  - Sutton et al. 1998
  - DEPAC module (van Zanten et al. 2010)
- Notable details: Ground and canopy processes are integrated to estimate deposition to soil, understory, tree trunks, and tree canopy, with explicit attention to LAI and phenology.

## Quality control and data structure

### Quality control
- Visual checks performed; obvious instrument or datalogger issues removed.
- Power cuts cause regular missing values; some gaps from sensor replacements.

### Data structure and content
- Dataset size: 816 measurements across 13 parameters (extension includes 15 named columns in the accompanying description).
- Data format: CSV file with the following columns:
  - Distance (m): Distance from NH3 enhancement source; negative indicates southwest, positive indicates northeast.
  - Month: Month and year.
  - NH3_conc (µg m⁻³): Monthly average NH3 concentration at 1.5 m height along each distance.
  - Fg (kg ha⁻¹): Cumulative NH3 deposition flux to the soil surface (negative indicates emission).
  - Fs_us (kg ha⁻¹): Cumulative stomatal deposition to understory vegetation (negative indicates emission).
  - Fw_us_Massad (kg ha⁻¹): Cumulative cuticular deposition to understory via Massad et al. (2010) parameterization (negative indicates emission).
  - Fw_us_DEPAC (kg ha⁻¹): Cumulative cuticular deposition to understory via DEPAC module (negative indicates emission).
  - Fw_us_Jones (kg ha⁻¹): Cumulative cuticular deposition to understory via Jones et al. (2007) parameterization (negative indicates emission).
  - Fd_us (kg ha⁻¹): Cumulative cuticular deposition to understory via Sutton et al. (1998) parameterization (negative indicates emission).
  - Ftt (kg ha⁻¹): Cumulative deposition to tree trunks (negative indicates emission).
  - Fs_tc (kg ha⁻¹): Cumulative stomatal deposition to tree canopy (negative indicates emission).
  - Fw_tc_Massad (kg ha⁻¹): Cumulative cuticular deposition to tree canopy via Massad et al. (2010) parameterization (negative indicates emission).
  - Fw_tc_DEPAC (kg ha⁻¹): Cumulative cuticular deposition to tree canopy via DEPAC module (negative indicates emission).
  - Fw_tc_Jones (kg ha⁻¹): Cumulative cuticular deposition to tree canopy via Jones et al. (2007) parameterization (negative indicates emission).
  - Fd_tc (kg ha⁻¹): Cumulative cuticular deposition to tree canopy via Sutton et al. (1998) parameterization (negative indicates emission).

## Data use and accessibility
- This dataset serves as a standardized, QA-focused data product suitable for monitoring and comparative analyses in environmental health and policy performance over time.
- It is an extension of the 2022 Queensberry dataset and includes an improved deposition-model approach to capture NH3 release peaks.
- Funding and collaboration information provided; references listed support model choices and methodology.
- Source data and related outputs are connected to broader nitrogen-cycle research initiatives and data portals (with explicit references to regulatory and environmental information repositories).

## Relevance to the Analysts Monitoring the Environment archetype
- Demonstrates standardized data collection, quality assurance, and transformation from instrument-collected NH3 concentrations to model-based deposition outputs, suitable for environmental health monitoring and policy evaluation.
- Uses established, peer-reviewed parameterizations and a transparent set of equations to derive deposition fluxes to multiple forest components, enabling cross-site comparisons and integration with other environmental datasets.
- Highlights data stewardship practices (documentation of data structure, missing values, and improvements over prior datasets) and the importance of making underlying data accessible for secondary use and broader scrutiny.