# Supporting Documentation

- Site: Stordalen mire, subarctic peatland near Abisko, Northern Sweden (68°20' N, 19°03' E). Landscape is heterogeneous with freshwater lakes, pools, bogs, and vegetation classes (hummock shrubs, semiwet bog, wet bog pools, graminoid-dominated bog). Forest areas present as birch with very wet to dry parameters. Latitude/longitude are recorded for sampling points.

- Objectives for GIS context: Provide map-ready, multi-layer data to enable spatial exploration of methane fluxes, nutrient dynamics, soil moisture, and temperature across vegetation types and microhabitats.

## Spatial and Temporal Scope

- Campaigns: Three sampling periods in 2013 — June 16–27, August 11–22, September 16–29.
- Sampling units: 60 static chambers measured simultaneously at any time, with 64 total chamber locations (4 wetland chambers relocated during the study). Chambers 61–64 were permanently underwater and lacked PRS probes.
- Location data: Exact chamber positions documented in oneoff_data.csv; each chamber has a unique chamber_id for data joins.

## Data Collection and Measurements

- Static chamber design and deployment
  - 40 cm diameter opaque polypropylene chambers; 10 cm deep bases left in ground.
  - Lids sealed during 45-minute flux measurements; air samples collected (100 mL) four times per session and stored in 20 mL glass vials.
  - Soil temperature measured at 10 cm depth at four replicate points near chamber bases; in-chamber air temperature recorded at chamber height (subset coverage).
  - Volumetric soil moisture content (VMC) measured at four replicate points near bases.
  - Vegetation within each chamber visually recorded.
- Nutrient flux probes
  - Plant Root Simulator (PRS) cation and anion probes deployed adjacent to each of the 60 chamber bases (deployment mid-2013).
  - Probes recovered and analyzed for nutrient fluxes; results corrected for deployment length.
  - PRS data include NO3–N, NH4–N, cations (Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd) and total NO3–N + NH4–N; coordinates and vegetation class also captured.
- Instrumentation
  - Gas analysis: HP 5890 GC with electron capture detector (N2O) and flame ionisation detector (CH4).
  - In-situ sensors: Omega HH370 soil temperature probe; CS616 soil moisture reflectometer.
  - PRS probes from Western Ag Innovations Inc.

## Calibration, Quality Control, and Data Processing

- Calibration
  - Gas analyses calibrated with a 4-point standard set (CH4 and N2O) roughly every 20 samples.
- Flux calculation and QA
  - Fluxes computed with GCFlux version 2, selecting the best-fit model per chamber (linear, quadratic, or asymptotic) from multiple options.
  - Reported CH4 fluxes in nmol CH4 m‑2 s‑1; includes best-fit estimate, model specifics, and 95% CI.
- Data integrity notes
  - Some chambers lacked PRS data (e.g., 61–64 due to being underwater).
  - Weather/temperature/soil moisture readings are tied to chamber deployment times and locations for spatial correlation.

## Data Structures and Key Files (GIS-ready)

- RC Flux Data
  - RCfluxOutput.csv: CH4 fluxes calculated per chamber with multiple model fits.
  - Key fields: gasName, filename (raw GC data), flux_linear, flux_quadratic, flux_linear2nd, flux_quadratic2nd, flux_asymptotic, flux_HMR, flux_bestfit, ci95lo_linear, ci95hi_linear, ci95l_bestfit, ci95hi_bestfit, adjr2_linear, adjr2_quadratic, bestFitMethod, chamberID.
  - Units: nmol CH4 m‑2 s‑1; instantaneous fluxes.

- Chamber-Specific Parameters
  - oneoff_data.csv: per-chamber measurements (collected once per chamber), includes chamber_id and location details.
  - Nutrient and PRS data
    - Total_N_PRS, NO3-N, NH4-N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd; all PRS flux units in micrograms/10 cm2/burial length.
    - veg_class: site vegetation category per Table 2 mapping (hummock and tall shrub; semiwet; wet; tall graminoid; water; stone pits).
    - lat, long: spatial coordinates for each data point (sampling locations).

- Vegetation and Site Classification
  - Table 2 provides site class characteristics corresponding to vegetation types and, for forests, chamber groups (e.g., forest by parameters_daily.csv).

- Time-Series and Per-Chamber Variants
  - parameters_daily.csv: per-chamber CH4 data across measurement dates for forest (chamber 1–14), includes Date, chamberID, sm_vmc_mean, soil_temp, air_temp.

- References
  - Methods and prior work cited for chamber design, flux methodology, vegetation dynamics, and QA procedures.

## Vegetation and Site Context (GIS Considerations)

- Vegetation classes (from Table 2 mapping) used to categorize flux and nutrient data spatially.
- Forest vs. mire wetland contexts represented by separate chamber groups and parameter sets, enabling comparative GIS analyses across habitat types.

## Practical GIS Applications

- Integrate datasets via chamberID and time stamps to build spatiotemporal maps of CH4 fluxes.
- Create layer overlays:
  - CH4 flux intensity by chamber with model selection indicated (best-fit or preferred model).
  - Soil moisture (VMC) and soil temperature at 10 cm depth as contextual layers.
  - PRS-derived nutrient fluxes (NO3-N, NH4-N, total N, and cations/anions) as soil–plant interaction indicators.
  - Vegetation class / site type to assess habitat influence on fluxes.
- Temporal analyses
  - Time-series per chamber from daily CH4 flux estimates and corresponding environmental covariates.
  - Seasonal patterns across June, August, September campaigns.
- Data quality and provenance
  - Link raw GC data (filenames) to processed flux estimates and confidence intervals.
  - Note chambers with incomplete data (e.g., underwater chambers lacking PRS data) for gap-aware mapping.

## Limitations and Considerations

- Temporal scope limited to 2013 campaigns; some chamber locations were relocated or were submerged.
- Data contain gaps (e.g., some chambers missing PRS data; not all measurements every session).
- Calibration and model selection are documented, but users should reference GCFlux v2 methods when reproducing flux calculations.

## References (Methods and Context)

- Clough et al. 2015; Chamber Design guidelines for nitrous oxide chamber methodology.
- Jammet et al. 2017; Year-round CH4 and CO2 flux dynamics in subarctic ecosystems.
- Johansson et al. 2006; Vegetation and net radiative forcing in peatlands.
- Levy et al. 2011; Uncertainty quantification in static chamber flux measurements.
- Malmer, Johansson, et al. 2005; Vegetation and long-term peatland dynamics.