# CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13

- Purpose of the dataset
  - Document field measurements of CO2 efflux and hydraulic data to understand controls on gas exchange in fluvial systems across different catchments and seasons (2011–2013).
  - Provide a multi-site, multi-parameter dataset suitable for evaluating environmental health monitoring approaches and informing policy-relevant assessments of carbon dynamics in freshwater networks.

- Study sites and sampling design
  - Scotland
    - River Kelvin (RK): 335 km2 semi-urban catchment; sampling reach ~30 m, near the Clyde estuary confluence; variable land use with agricultural and urban influence.
    - Drumtee Water (DW): headwater peat-dominated catchment (9.6 km2); sampling reach ~19 m; rough grazing land use.
    - Periodicity: RK and DW sampled regularly from June 2012 to December 2013 (weekly to every three weeks), spanning all four seasons.
  - Amazon (Tambopata National Reserve, Peru)
    - Main Trail (MT): catchment ~5 km2; active mainly during the rainy season; channel width 4–7 m.
    - New Colpita (NC): small perennial stream; catchment ~7 km2; channel width 4–7 m.
    - La Torre river (LT): catchment ~2000 km2; channel width 40–80 m near sampling point.
    - Tambopata river (TP): catchment ~14,000 km2; near confluence with Tambopata; channel width ~200 m.
    - Periodicity: MT, NC, LT, TP sampled Feb 2011–May 2012 (three campaigns) to capture wet/dry season water level variations; MT specifically during the rainy season.
  - Across sites, measurement locations were chosen to capture a range of flow intensities.

- CO2 efflux measurements
  - Method: floating chamber (volume 0.0029 m3) with closed-loop LI-840A CO2/H2O analyzer; internal circulation with a small pump (0.3–1.0 L min-1).
  - Procedure: four-minute accumulation, three replicate measurements per site/visit.
  - Flux calculation: F_CO2 = (δCO2/δt) × (V / (R × T × S)) where δCO2/δt is the slope of CO2 accumulation (μatm s-1), V is chamber volume, T is air temperature (K), S is surface area of chamber.
  - Additional site-specific notes: near-surface flow velocity measured at chamber position in the Amazon sites; Fr and Re not computed for MT/NC/LT/TP due to unavailable data at those sites.

- Hydraulic parameters
  - Velocity measurement: Valeport flow meter (50 mm impeller) with 60-second averages, taken at 20% and 80% of flow depth and at least three other depths to identify outliers.
  - Key hydraulic metrics:
    - Mean velocity (ū, m s-1) as depth-averaged condition at the measurement point.
    - Froude number (Fr) as a proxy for surface disturbance and gas exchange potential.
    - Reynolds number (Re) as turbulence/mixing indicator and potential transport of CO2-rich water.
  - UK sites (RK, DW): detailed Fr and Re included.
  - Amazon sites: Fr and Re were not available for MT, NC, LT, TP.

- Water chemistry and gas measurements
  - pH and temperature: measured or logged to support pCO2 and DIC calculations.
    - DW: continuous pH logging (30-minute resolution) using In-Situ Troll 9000; continuous measurement avoided lab-induced artifacts.
    - RK: pH calculated from a discharge–pH relationship due to instrument issues (calibration data from a station upstream).
    - MT/NC: pH, conductivity, and temperature logged at 15-minute resolution with Troll 9500.
    - LT/TP: spot measurements of pH, conductivity, temperature at the time of CO2 flux measurement with Troll 9500; extended log-in deployment (>20 minutes) for equilibration.
  - Dissolved inorganic carbon ([DIC]) and pCO2:
    - Water samples collected within ~15 minutes of flux measurement in triplicate for [DIC] (acidified to preserve samples) and stored cold; [DIC] analyzed within ~6 months using Gas Bench/Delta V Plus.
    - pCO2 calculated from [DIC] with pH and temperature data, following established methods.
  - Troll calibrations:
    - Troll 9000: calibration approximately every 5 weeks (two-point, pH4/pH7); field cleaning and maintenance performed with soft brushes.
    - Troll 9500: calibration approximately every month (two-point, pH4/pH7); in-field electrolyte checks and routine cleaning.

- Data structure and quality control
  - Data file: a single spreadsheet titled “CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-13” (CSV format); 11 columns per record; missing values indicated as NA.
  - Columns included:
    - Date, Region (Amazon/Scotland), Site, Mean CO2 efflux (μmol CO2 m-2 s-1), SD of mean CO2 efflux, Flow (m s-1), Water depth (m), pCO2 (μatm), [DIC] (mM C), pH, Water temperature (°C).
  - Data completeness and gaps:
    - DIC data missing for June 2012–January 2013 at DW/RK due to timing of sample collection.
    - MT dried up in Sep–Nov 2011; MT/NC/LT/TP data gaps reflect seasonal/access limitations or equipment issues.
    - Some sites lacked Fr/Re values (Amazon) due to data availability.
  - Data quality controls: standard instrument calibrations, drift monitoring for DIC standards, multi-replicate measurements, and documentation of missing data and reasons.

- References and context
  - Methodological and calibration references for measurement approaches, gas flux calculations, water chemistry, and data handling (e.g., Frankignoulle 1988; Stumm & Morgan 1996; Waldron et al. 2014; Long et al. 2015; Abril et al. 2015; SEPA data, 2015).

- Relevance for monitoring frameworks
  - Demonstrates a structured approach to collecting, documenting, and quality-checking multi-parameter environmental data across diverse catchments.
  - Highlights practical challenges in data availability, metadata completeness, and harmonization across sites, which are critical considerations for monitoring framework design.
  - Provides a concrete example of linking hydrology (flow, depth, velocity, Fr, Re) with gas exchange (CO2 flux, pCO2, DIC) and water chemistry to inform policy-relevant carbon dynamics in freshwater ecosystems.