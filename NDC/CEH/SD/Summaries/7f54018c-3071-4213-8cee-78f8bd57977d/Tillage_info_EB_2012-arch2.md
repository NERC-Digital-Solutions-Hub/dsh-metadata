# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

- Aim
  - Document fluxes of N2O from two adjacent grassland fields (tilled vs un-tilled) before and after a tillage event on 1 May 2012, using eddy covariance and chamber methods.
  - Compare management impacts under an intensively managed livestock system and quantify data quality and processing steps for environmental monitoring.

- Study site and management
  - Easter Bush, Scotland (temperate maritime climate; ~55°51'55"N, ~3°12'22"W).
  - Two fields (~5.4 ha each) with >20 years of intensive livestock production; grazing by sheep (≈0.7 LSU ha-1) and ~200 kg N ha-1 y-1 fertiliser historically.
  - Soil: clay loam, imperfectly drained (Macmerry soil, Rowanhill association), pH ~5.1; drainage system present but not functioning well, causing surface water during rains.
  - Management contrast: North field (un-tilled) grazed continuously; South field (tilled) underwent tillage on 1 May 2012 and was reseeded to ryegrass; fertilisation schedules differed (North received two 70 kg N ha-1 applications on 28 May and 9 Aug 2012; South received a single 70 kg N ha-1 on 9 Aug 2012).

- Experimental design
  - Parallel fields monitored before and after a tillage event to assess effect on N2O fluxes.
  - Tillage sequence: glyphosate pre-treatment (27 Apr 2012), plough to 30 cm (1 May), harrow, roll, reseed (3 May).
  - Field management events are detailed in the study’s Table 1.

- Instrumentation and data collection
  - Eddy covariance (EC)
    - Installed 27 Mar 2012 at field boundary; 2.4 m height mast.
    - Measurements: 3D wind (ultra-sonic anemometer) and concentrations of N2O, H2O, CO2 (quantum cascade laser).
    - Data cadence: 10 Hz; fluxes computed at 30 min intervals using covariance between N2O mixing ratio (χ) and vertical wind (w).
    - Processing and QC: double coordinate rotation, spike removal, block averaging, time-lag optimization; density corrections (Burba et al., 2012); frequency response corrections (Moncrieff et al., 1997); QC per Foken et al. (2005).
    - Field separation: data classified as from tilled vs un-tilled fields by wind direction; data outside clear separation were discarded due to equipment obstruction.
  - Chamber measurements
    - Static chambers: PVC cylinders (38 cm ID, 22 cm height), inserted 5 cm; 40-min closure with three 100 mL gas samples (0, 20, 40 min); analysis by GC with electron capture detector.
    - Dynamic chambers (QCL integration): 39 cm ID, 22 cm height, stainless collar into soil (≈5 cm). Closed system with ~6–7 L min-1 flow; ~22 s lag; 3-minute 1 Hz data used with linear and non-linear asymptotic regressions to estimate flux; best-fit method chosen per measurement.
    - Replication: 10 static chambers per field; dynamic chamber measurements conducted within the flux footprint (10–200 m from mast) and occasionally moved to avoid microclimate biases.
    - Detection limits: dynamic method ~0.04 nmol m^-2 s^-1 vs static ~0.4 nmol m^-2 s^-1.

- Data and file contents
  - Easter_Bush_EddyC_Tillage_2012: contains half-hourly EC fluxes and related meteorological variables (e.g., Tau, H, LE, co2_flux, h2o_flux, n2o_flux, wind_speed, wind_dir, u*, L, z-d/L, etc.).
  - Easter_Bush_Chambers_Tillage_2012: chamber-derived flux data and associated site conditions (location, method, chamber flux, air temperature, soil temperature, rainfall, etc.).

- Data processing and quality assurance
  - EC data: corrections for atmospheric density effects, sensor lag, and sensor response; high/low-frequency corrections; QA/QC to remove poor-quality data; careful separation of tilled vs un-tilled data based on wind direction to avoid misattribution.
  - Chamber data: flux calculations using dC/dt, air density, chamber volume, and footprint considerations; use of regression-based approaches to derive fluxes; cross-validation between static and dynamic chamber results.

- Relevance for environmental monitoring and data use
  - Demonstrates a standardised, multi-method approach to quantify soil N2O fluxes in agricultural systems, suitable for inclusion in environmental health and policy performance analyses.
  - Data are structured for integration into broader environmental datasets (maps, charts, time-series) and can be linked with other soil, climate, and management datasets to increase data value beyond single-use applications.
  - Highlights practical considerations for data accessibility and reuse, including clear documentation of field management events, instrumentation, processing steps, and quality controls.

- Key references for methods
  - Methods and corrections for eddy covariance and chamber techniques cited (e.g., Moncrieff et al., 1997; Burba et al., 2012; Foken et al., 2005; Levy et al., 2011; Pedersen et al., 2010; Skiba et al., 2013), ensuring standardized, reproducible data processing and uncertainty assessment.