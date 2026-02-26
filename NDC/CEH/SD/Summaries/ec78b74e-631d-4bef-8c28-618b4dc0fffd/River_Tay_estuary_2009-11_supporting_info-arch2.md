# River Tay estuary greenhouse gas and water chemistry data set

- A dataset documenting greenhouse gas concentrations and water chemistry for the River Tay estuary.
- Covers 10 sampling locations along the estuary, with sites numbered 1 (furthest upstream) to 10 (furthest downstream).
- Sampling period spans April 2009 to July 2011 (Harley et al. 2015 describes April 2009–August 2010; this dataset extends to July 2011).
- Locations are within 100 m of the provided UK grid reference for each site; axial surveys were conducted from a rigid inflatable boat at high tide.

## Sampling regime

- Axial surveys of the estuary conducted along 10 locations, starting at the upstream site at high tide.
- Greenhouse gas and water chemistry samples collected at each site.
- Sampling sites defined relative to UK grid references; exact locations shown in Figure 1 of Harley et al. (2015).

## Measurements and methods

- Physico-chemical parameters measured in situ at ~10 cm below surface using a Hydrolab QuantaProbe:
  - Dissolved oxygen (DO)
  - pH
  - Temperature
  - Conductivity
- Water samples collected in triplicate at each site using three plastic buckets.
  - Samples filtered (GF/F 0.7 µm) and analyzed in the lab for:
    - Total nitrogen (TN)
    - Dissolved inorganic nitrogen (DIN)
    - Ammonium (NH4+)
    - Nitrate (NO3−)
  - Nitrogen analyses performed colorimetrically on a SEAL AQ2 discrete analyzer.
  - Total suspended solids (TSS) determined by oven-drying GF/F filters at 105°C for 4 hours.
- Greenhouse gas sampling by headspace method (triplicate per site):
  - 40 mL estuary water equilibrated with 20 mL ambient headspace in a syringe.
  - Headspace samples injected into pre-evacuated 12 mL vials for GC analysis.
  - Gases measured: N2O, CH4 (via GC with ECD and FID) and CO2 (separate GC).
  - Dissolved gas concentrations corrected for water temperature and salinity (salinity inferred from conductivity).
  - Gas saturations calculated from dissolved gas concentration relative to atmospheric equilibrium water concentration.

## Nature and units of recorded values

- Data values reported to two decimal places.
- Missing values marked with an asterisk in the CSV.
- Key columns include:
  - Date, Time (GMT)
  - Site No. (1–10) and Site Name/Grid Ref
  - N2O-N (µg/L), N2O Sat (%)
  - CH4-C (µg/L), CH4 Sat (%)
  - CO2-C (mg/L), CO2 Sat (%)
  - Temperature (°C)
  - NO3-N (mg/L), NH4-N (mg/L), DIN (mg/L), TN (mg/L)
  - pH
  - DO (mg/L), DO Sat (%)
  - Conductivity (mS/cm), Salinity (ppt)
  - TSS (mg/L)

## Data quality and standardisation

- Data are collected and presented in a standardised, tabulated format suitable for longitudinal environmental monitoring.
- Triplicate sampling for both water chemistry and greenhouse gases supports precision assessment.
- Corrections applied for temperature and salinity ensure comparability of dissolved gas measurements.
- Clear documentation of units and site metadata facilitates cross-site and temporal comparisons.

## Uses for environmental monitoring and policy assessment

- Enables consistent assessment of estuarine water chemistry and greenhouse gas fluxes over time.
- Supports benchmarking and trend analysis to inform environmental health evaluations and policy performance.
- Data can be linked with other environmental datasets to enhance value beyond single-use analyses.

## Reference

- Harley, J.F., Carvalho, L., Dudley, B., Heal, K. V., Rees, R.M., Skiba, U., 2015. Spatial and seasonal fluxes of the greenhouse gases N2O, CO2 and CH4 in a UK macrotidal estuary. Estuarine, Coastal and Shelf Science.