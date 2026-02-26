# Ammonia concentration and deposition data from Queensberry experimental site in Sri Lanka (2023)

## Overview
- Studies the effects of high ammonia (NH3) in the air on forest vegetation, bryophytes, lichens, and soil at Queensberry Estate, central Sri Lanka.
- Enhancement system releases NH3 only when wind conditions meet directional and speed thresholds (wind from 5–75 degrees, 185–255 degrees; speeds 0.3–10 m/s).
- NH3 concentrations measured at 1.5 m height along two monitoring quadrats; sampling monthly from January 2023 to December 2024.
- Dataset extends the 2022 dataset from the same site and includes improvements to the deposition/flux modeling.

## Data collection and measurements
- Location: tropical sub-montane forest at Queensberry Estate (coordinates and altitude provided).
- Equipment: UKCEH Adapted Low-cost Passive High Absorption (ALPHA) samplers for NH3 concentration.
- Height and layout: measurements conducted at 1.5 m along monitoring quadrats.
- Temporal coverage: monthly measurements 2023–2024.
- Output: 816 measurements across 13 parameters, stored in a CSV with clearly described columns.

## Model, calculations, and methodology
- Deposition modeling: four-layer canopy compensation point model; bi-directional resistance framework accounts for stomatal exchange and soil re-emission potential.
- Deposition flux formulation: Fχ(z) = χa / Rt (where Rt is total resistance to dry deposition).
- Surface-specific deposition/resistance components:
  - Soil surface: quasi-laminar boundary layer resistance (Rbg).
  - Tree trunks: quasi-laminar boundary layer around trunks (Rb(tt)).
  - Stomatal deposition: stomatal resistance (Rs) with Leaf Area Index (LAI) dependency.
  - Cuticular deposition: multiple parameterizations (three main approaches plus DEPAC) with LAI dependency.
  - Capacitance (Rd) parameterization for cuticular deposition examined (Cd-based).
- Notable improvements: current model simulates NH3 concentration peaks during release periods to estimate deposition, rather than using monthly mean concentrations to drive deposition across a month (enhances peak deposition estimates).
- Accessory details: parameterizations include Massad et al. (2010), Jones et al. (2007), Sutton et al. (1998), DEPAC module (van Zanten et al., 2010), and Chamberlain sources for resistances.
- Documentation: full experimental design, methodology, analysis, and findings described in related Deshpande et al. papers (2024a, 2024b); this dataset specifically notes the methodological improvement.

## Data quality control and structure
- Quality control: visual checks; removal of obvious instrument/mislogging errors; gaps due to scheduled power cuts; sensor replacement may introduce additional gaps.
- Structure: CSV with 13 parameters measured or derived; columns include:
  - Distance (m) from NH3 source (negative = southwest, positive = northeast)
  - Month (YYYY-MM)
  - NH3_conc (µg m^-3)
  - Fg (soil deposition flux; kg ha^-1; negative = emission)
  - Fs_us (stomatal deposition to understory; kg ha^-1)
  - Fw_us_Massad (cuticular deposition to understory; kg ha^-1)
  - Fw_us_DEPAC (cuticular deposition to understory; kg ha^-1)
  - Fw_us_Jones (cuticular deposition to understory; kg ha^-1)
  - Fd_us (cuticular deposition to understory; kg ha^-1)
  - Ftt (soil/root deposition to tree trunks; kg ha^-1)
  - Fs_tc (stomatal deposition to tree canopy; kg ha^-1)
  - Fw_tc_Massad (cuticular deposition to tree canopy; kg ha^-1)
  - Fw_tc_DEPAC (cuticular deposition to tree canopy; kg ha^-1)
  - Fw_tc_Jones (cuticular deposition to tree canopy; kg ha^-1)
  - Fd_tc (cuticular deposition to tree canopy; kg ha^-1)
- Flux convention: negative values indicate emission; positive values indicate deposition.
- Data is an extension of the 2022 dataset from the same site, with improved deposition modeling during NH3 release periods.
- Data provenance: described in the related publications and dataset records (Deshpande et al., 2024a, 2024b).

## Data access, structure, and metadata
- Data format: CSV file with clearly defined column descriptions and units.
- Key metadata captured: distance from source, directional orientation, temporal stamp (month/year), multiple deposition flux components for soil, understory, and tree canopy, and NH3 concentration.
- Units:
  - Distance: meters (m)
  - NH3_conc: micrograms per cubic meter (µg m^-3)
  - Fluxes (Fg, Fs_us, Fw_us_*, Fd_us, Ftt, Fs_tc, Fw_tc_*, Fd_tc): kilograms per hectare per year (kg ha^-1)
- Data is linked to funding, methodology, and referenced in published works; full methodological details are provided in associated Deshpande et al. papers.

## Funding and references
- Funding: UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1).
- References to core methods and context:
  - Chamberlain (1968, 1984) on gas transport to rough surfaces
  - Fowler (1978) and related dry deposition work
  - Massad, Nemitz, Sutton (2010) on resistance modeling and parameterizations
  - Nemitz et al. (2000); Sutton et al. (1998); Jones et al. (2007)
  - DEPAC module (van Zanten et al., 2010)
  - Deshpande et al. (2024a, 2024b) for dataset context and meteorological/NH3 concentration details

## Implications for data leadership and data strategy
- Demonstrates end-to-end data lifecycle: acquisition via field experiments, standardized processing, multiple deposition models, quality control, and structured dissemination in a CSV dataset.
- Highlights importance of model enhancement for accurate exposure and deposition estimates during emission events, aligning data products with user needs for precise, event-driven insights.
- Emphasizes robust metadata and clear data conventions (units, directions, sign conventions) to ensure discoverability and interoperability across networks and users.
- Illustrates the value of extending and improving existing datasets (2022 baseline) to capture peak deposition dynamics, informing policy-relevant assessments and cross-site comparisons.
- Underlines governance aspects relevant to Data Leaders: documenting methodology, updating models, ensuring traceability to references, and providing transparent provenance for data consumers.
- Notes practical data quality considerations: instrument downtime, scheduled power cuts, and sensor maintenance as common causes of data gaps that should be documented and accounted for in data plans.