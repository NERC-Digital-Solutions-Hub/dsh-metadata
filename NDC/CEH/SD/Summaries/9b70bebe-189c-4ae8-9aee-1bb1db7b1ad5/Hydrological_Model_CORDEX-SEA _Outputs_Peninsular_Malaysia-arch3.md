# Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum daily flows on a 0.008333° × 0.008333° grid (~1 km) across Peninsular Malaysia.
- Covers historical period (1971–2005) and projected future (2006–2099) driven by CORDEX-SEA climate data.
- Part of the Malaysia-Flood Impacts Across Scales (FIAS) project, aiming to identify flood-vulnerable areas and potential damages/disruptions.

## Data and Modelling Approach
- Hydrological model: Physically-based, grid-based, non-calibrated to individual catchments, designed for spatially consistent estimates across ungauged locations.
- Domain and resolution: Peninsular Malaysia, latitude 1.2°–6.8°, longitude 99.5°–104.6° E; grid resolution ~1 km.
- Artificial influences scenarios: CAI (current artificial influences, e.g., water transfers/diversions) and FAI (planned future artificial influences).
- Driving climate data: CORDEX-SEA daily variables (precipitation, near-surface air temperature, daily max/min temps); potential evapotranspiration estimated from temperature.
- Climate scenarios and ensembles: Historical baseline (1971–2005) and future (2006–2099) driven by six RCPs/ensemble configurations (RCP2.6, RCP4.5, RCP8.5 with 6, 7, and 13 members respectively; aggregated as 13 historical and 26 future realizations).
- Context: Output stems from the broader Malaysia-FIAS project, which explored flood risk across scales under multiple climate scenarios (RCPs).

## Data Format, Access, and Scope
- Outputs: Monthly mean flows and annual maximum daily flows (both in m3 s−1) on a 1 km grid; provided as NetCDF files.
- File coverage: 13 historical realizations and 26 future realizations (across 3 RCPs).
- File naming conventions: Systematic naming to distinguish CAI/FAI, model, driving model, RCP, and period (e.g., CAI_HIST, CAI_<model>_<driving>_<RCP>_200601-209912.nc; FAI counterpart; AMFLOW and MMFLOW files with CAI/FAI prefixes).
- Temporal resolution options: CORDEX-SEA inputs specify three possible year-length conventions (365/366, 365, or 360 days per year) that affect annual maximum series length.
- Data characteristics: Ensemble approach means no single “preferred” projection; analyses should use the full ensemble to capture range of possible outcomes.
- Limitations: Not calibrated to individual catchments; cannot directly map to observed river flows; suitable for ungauged locations but river identification is limited to 1 km grid cells (catchments smaller than ~5 km² are not readily resolved).
- Data accessibility and tools: NetCDF with metadata headers; readable via GIS tools (ArcGIS, NCView) or programming tools (Python, Fortran); large ensemble size may complicate online storage.

## Validation, Uncertainty, and Interpretation
- Performance assessment: Model run evaluated against observed daily river discharge at gauges across Peninsular Malaysia using gridded precipitation and PE inputs; historical runs are climate-model realizations rather than exact observations, so comparisons are statistical rather than point-for-point.
- Uncertainty: High intrinsic uncertainty from climate projections and from non-calibrated hydrology; ensemble spread highlights variability across models and scenarios.
- Guidance for interpretation: Compare within the same CORDEX-SEA model and RCP across CAI/FAI; do not directly compare with observed historical flows; use ensemble range to assess potential flood/drought risks.

## Outputs, Use Cases, and Monitoring Implications
- Applications:
  - Planning for future floods and droughts at state/catchment and national scales.
  - Assessing climate-change impacts on river flows under multiple RCPs and artificial-influence scenarios.
  - Flood-frequency analysis by examining annual maximum flows; potential to fit generalized extreme value distributions and derive return-period curves.
- Practical considerations for policymakers:
  - Use the full ensemble to characterize uncertainty and to inform risk-based decision-making.
  - Recognize grid-scale limitation; results are suitable for planning at broader scales rather than local infrastructure sizing without higher-resolution data.
  - Data can support scenario planning, adaptation strategies, and resource management under different climate futures.

## Data Governance, Metadata, and Data Sharing
- Metadata: NetCDF files include headers with metadata; standard data organization facilitates interoperability.
- Data sharing and openness: Public sharing of underlying data is a consideration raised in monitoring contexts; while this dataset provides open NetCDF outputs, broader governance should address provenance, versioning, and metadata completeness to ease reuse.
- Data management implications for monitoring frameworks:
  - Establish clear provenance, data quality checks, and documentation for ensemble datasets.
  - Ensure metadata is machine- and human-readable to support governance and decision workflows.
  - Plan for storage and access of large ensemble outputs; provide tools or portals for efficient extraction of region-specific and period-specific subsets.

## Data Sources and Acknowledgements
- CORDEX-SEA climate inputs and regional ensemble information; references to CORDEX and related climate studies.
- Acknowledgement of the Malaysia-FIAS project and supporting institutions (NERC, Ministry of Higher Education of Malaysia) for funding and collaboration.

## References (selected)
- Bell et al. (2021); Crooks et al. (2014); Rameshwaran et al. (2021); Tangan et al. (2020); Jenkinson (1955); Martens et al. (2017); Oudin et al. (2005); van Vuuren et al. (2011).