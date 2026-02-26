# Historical (1950-2005) and projected (2006-2099) hydrological model (HMF-WA) estimates of monthly mean and annual maximum river flows across West Africa driven by CMIP5 projected climate data

- Executive snapshot
  - Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum river flows on a 0.1° × 0.1° grid across West Africa for historical and future periods.
  - Driven by bias-corrected CMIP5 climate data, with two future water-use scenarios and multiple RCPs to form an uncertainty envelope.
  - Aims to support climate-informed planning for floods and droughts, including across ungauged locations.

- What the dataset contains
  - Variables: monthly mean river flows (m3 s-1) and annual maximum of daily river flows (m3 s-1).
  - Temporal coverage: historical 1950–2005; future 2006–2099.
  - Spatial coverage: West Africa on a 0.1° × 0.1° grid (~10 km × 10 km), domain approx. lat 3°–26° N, lon -18°–25° E.
  - Ensemble: 29 historical realizations and 76 future realizations across 20 CMIP5 models and multiple RCPs (RCP2.6, RCP4.5, RCP8.5).
  - Climate forcing: bias-corrected CMIP5 climate variables (precipitation, near-surface air temperature, daily max/min temperature); potential evaporation derived from temperature.
  - Water-use scenarios: (i) population-change–driven water use (BC) and (ii) same as present day (WO) to bound possible impacts.
  - Not calibrated to individual catchments; designed for broad, regional/gridded consistency and ungauged areas.

- Technical details
  - Data format: NetCDF4 with three dimensions (Latitude, Longitude, Time).
  - File naming conventions:
    - Monthly mean flows: HMF-WA_MMFLOW_BC_<model>_<HIST/RCPl>_195001-200512.nc or HMF-WA_MMFLOW_BC_WO_<model>_<RCP>_200601-209912.nc
    - Annual maximum flows: HMF-WA_AMFLOW_BC_<model>_HIST_1950-2005.nc or HMF-WA_AMFLOW_BC_<model>_<RCP>__2006-2099.nc or HMF-WA_AMFLOW_BC_WO_<model>_<RCP>_2006-2099.nc
  - Time-resolution nuance: number of days per year may be 365/366 (Gregorian) or 360 (30-day months) depending on the CMIP5 model.
  - Access: data available via the dataset DOI and access page; terms and conditions described there.
  - Data sources: bias-corrected CMIP5 outputs (per Famien et al., 2018) plus AMMA-2050 context; observed river discharge data from GRDC used for performance assessments in the underlying study.

- Context and methodology
  - Part of AMMA-2050 regional hydrological modelling for West Africa, using the Hydrological Modelling Framework (HMF-WA) to simulate flows at grid scale, incorporating anthropogenic water use, wetlands, and endorheic features.
  - Two water-use scenarios provide an indicative envelope of potential future changes due to population and development.
  - Baseline climate inputs are bias-corrected to 0.5° × 0.5° across Africa; PE estimated from temperature.
  - Model performance (1981–2010) shows good performance for high-flow periods and lower performance for some small or flashy catchments; no catchment calibration to observed flows.

- How to use the data (applications)
  - Support planning for future floods and droughts at national and regional levels in West Africa.
  - Analyze climate-change impacts on river flows under different RCPs and water-use scenarios.
  - Flood-frequency analysis using annual maximum series (Gringorten plotting positions; L-moments fitting) to derive return-period curves.
  - Compare within the same CMIP5 model across future scenarios, while acknowledging ensemble uncertainty across models.
  - Useful for ungauged locations due to gridded, spatially consistent outputs; not suitable for deriving flows at very small catchments (< ~5,000 km2) with precision.

- Limitations and caveats for data leaders
  - Not directly comparable to observed historical river flows; designed for ensemble-based impact assessment.
  - Spatial resolution (~10 km) may not capture very small catchments; caution for catchments below ~5000 km2.
  - No individual CMIP5 member is deemed “preferred”; analysts should consider the full ensemble to understand uncertainty.
  - Bias correction narrows the uncertainty range; ongoing model development may shift projections with higher resolution or process fidelity.

- Provenance, quality, and metadata
  - Data are produced within the AMMA-2050 framework and are accompanied by metadata in NetCDF headers; includes model, RCP, period, and WO/BC designations.
  - Model performance assessed with historical observations (NSE and NSElog metrics) at numerous West African stations; broader caveats regarding calibration and regional heterogeneity remain.
  - Data sources and citations provided; usage requires citing the associated NERC/DFID FCFA dataset article and related references.

- Access, licensing, and governance
  - Data accessible via the provided DOI and AMMA-2050 data access pages; terms and conditions govern use and redistribution.
  - Proper citation required in any use: Rameshwaran et al. and AMMA-2050 documentation; acknowledgement of supporting institutions recommended.

- Data sources and references (highlights)
  - CMIP5 bias-corrected Africa dataset (Famien et al., 2018)
  - AMMA-2050 project context (UK NERC/DFID FCFA)
  - HMF-WA and related methodological foundations (Crooks et al., 2014; Bell et al., 2007)
  - Observed discharge data from GRDC for model evaluation
  - Related bias-correction and hydroclimate literature cited in the dataset documentation

- Acknowledgements
  - Supported by NERC/DFID FCFA; data preparation and submission efforts acknowledged; collaborators named in the dataset note.