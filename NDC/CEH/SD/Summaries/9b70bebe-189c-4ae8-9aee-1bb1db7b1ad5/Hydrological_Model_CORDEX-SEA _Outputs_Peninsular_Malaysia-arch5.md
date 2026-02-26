# Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

- Scope and purpose
  - Provides ensemble estimates of monthly mean river flows and annual maximum daily flows on a 1 km grid across Peninsular Malaysia.
  - Covers historical (1971–2005) and projected future (2006–2099) periods.
  - Driven by CORDEX-SEA climate data; supports flood and drought planning under climate change.

- Data content and structure
  - Products: monthly mean flows (MM) and annual maximum flows (AM) in m3 s-1.
  - Spatial resolution: 0.008333° × 0.008333° (~1 km × 1 km).
  - Temporal structure: time dimension with monthly (MM) and annual (AM) records.
  - Ensemble: 13 historical realizations and 26 future realizations across three RCPs (RCP2.6, RCP4.5, RCP8.5).
  - Artificial influences: two scenarios for future simulations
    - CAI: current artificial influences (e.g., water transfers/diversions)
    - FAI: planned future artificial influences
  - Grid domain: Peninsular Malaysia, lat 1.2°–6.8° N, lon 99.5°–104.6° E.
  - File naming conventions: NetCDF format with explicit naming to distinguish MM vs AM, CAI vs FAI, model, driving model, RCP, and period (e.g., HMF-PM_MMFLOW_CAI_<model>_<driving>_RCP8.5_200601-209912.nc).

- Data provenance and methods
  - Model framework: Hydrological Modelling Framework - Malaysia (HMF-Malaysia), a physically-based grid-based hydrological model.
  - Driving data: CORDEX-SEA climate model outputs (precipitation, near-surface temperature, and daily max/min temperatures); potential evaporation sourced from GLEAM temperatures.
  - Calibration: not tuned to individual catchments; uses spatial datasets of physical/soil properties to configure hydrology.
  - Domain and calibration notes: designed for spatial consistency across the domain; performance assessed using observed daily river discharge at gauging stations (driven by gridded precipitation and PE data for validation).
  - Climate scenarios: six regional-climate-model realizations for each RCP (historical plus multiple future realizations) to form ensemble.

- Access, format, and usage guidance
  - Format: NetCDF with dimensions Latitude, Longitude, Time; metadata included in file headers.
  - Data access: CORDEX-SEA variables available from cordex.org (region-14south-east-asia-sea).
  - Ensemble interpretation: no single ensemble member is preferred; analyses should consider the full range of ensemble projections for each model and RCP.
  - Observed data comparison: simulated flows are climate-model driven and cannot be directly equated with observed historical river flows.
  - Spatial resolution caveat: 1 km grid cannot resolve catchments smaller than ~5 km².
  - Practical uses: planning for future floods and droughts at state/catchment scales; construct flood-frequency curves using annual maximum (AM) data; compare changes across RCPs and artificial-influence scenarios.

- Governance, metadata, and data management considerations
  - Data lineage: clearly documented within NetCDF headers and accompanying materials; references to original climate and hydrological modelling studies are provided.
  - Data updates and versions: multiple ensemble realizations and scenarios; users should track model/realization/version when integrating into workflows.
  - Documentation and usage notes: detailed guidance on file naming, dataset contents, and interpretation included; cautions about non-interpolatable comparisons to observed data and limitations in resolving small catchments.

- Data sources and acknowledgments
  - CORDEX-SEA climate variables; GLEAM for potential evaporation; references to Malaysia-FIAS project and supporting institutions.
  - Acknowledgements and references provide context for model development, climate datasets, and supporting prior work.

- Suggested applications and limitations
  - Applications: regional flood risk assessment, water-resource planning, and scenario analysis for Peninsular Malaysia under climate change.
  - Key limitations for stewardship: not calibrated to local catchments; ensemble-based uncertainty requires treatment; large data volumes limit online distribution; results are best used for ensemble-level insights rather than single-point predictions.