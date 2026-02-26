# Field Study Sites:

- Data collected from six field sites across Scotland and the Amazon, spanning multiple years to capture seasonal and flow-condition variability.
- Within each site, measurement locations covered a range of flow intensities.

## Study sites and sampling

- Scotland
  - River Kelvin (RK): 335 km2 semi-urban catchment; 18 m a.s.l.; measurements in a 30 m reach near the River Clyde confluence.
  - Drumtee Water (DW): headwater, peat-dominated catchment (9.6 km2), up to 260 m elevation; measurements in a 19 m reach.
- Amazon
  - Main Trail (MT): catchment ~5 km2; active only during the rainy season; channel 4–7 m wide.
  - New Colpita (NC): perennial small stream; catchment ~7 km2; channel 4–7 m wide.
  - La Torre river (LT): catchment ~2000 km2; channel 40–80 m wide near confluence with Tambopata river.
  - Tambopata river (TP): catchment ~14,000 km2; channel ~200 m wide near sampling point; predominantly rainforest with some small-scale agriculture and gold mining.

## Measurements and sampling periods

- RK and DW: weekly to biweekly from June 2012–December 2013, covering all seasons.
- MT, NC, LT, TP: field campaigns Feb–Apr 2011, Sept–Dec 2011, and Mar–May 2012; included wet and dry season conditions.
- Number of data points per parameter by site listed (see Table 1 in the dataset).

## CO2 efflux measurements

- Method: floating chamber (volume 0.0029 m3) with LI-840A infrared CO2/H2O analyzer; internal circulation with Schego pump (0.3–1.0 L min-1); CO2 accumulation tracked for four minutes, three replicates.
- Flux calculation: F_CO2 = (dCO2/dt) × (V / (R T S)); where dCO2/dt is the slope of CO2 in the chamber (μatm s−1), V is chamber volume, T is air temperature, S is chamber surface area.
- Surface state: qualitative assessment of water surface (smooth/medium/rough) used to indicate disturbance and potential gas exchange; wind speed not directly measured.
- Amazon data: near-surface flow velocity measured at three replicates below chamber; Fr and Re not available for MT/NC/LT/TP sites.

## Hydraulic parameters

- UK sites: velocity measured with Valeport flow meter (50 mm impeller) at 20% and 80% depth; 60 s averaging; at least three additional heights to identify outliers.
- Parameters derived:
  - Mean velocity (ū, m s−1)
  - Froude number (Fr), indicator of surface disturbance and gas exchange potential
  - Reynolds number (Re), indicator of turbulence and mixing, relevant to transfer of CO2-enriched water to the surface
- Notes: Fr = ū / sqrt(gH); Re calculated per standard formulations; in the Amazon sites, Re and Fr were not available.

## Water chemistry and dissolved inorganic carbon

- Water chemistry analyzed at the time of flux deployment to support CO2 flux models.
- pH measurement
  - DW: continuous in-situ pH logging (30-minute resolution) with In-Situ Troll 9000.
  - RK: pH calculated from a discharge–pH relationship due to equipment malfunction (n=10; R2=0.72) using upstream monitoring data; no significant tributaries between sites and monitors verified.
  - MT, NC: pH, conductivity, and temperature logged at 15-minute resolution with Troll 9500.
  - LT, TP: spot measurements of pH, conductivity, and temperature with Troll 9500; deployed >20 minutes to equilibrate.
- Temperature: air and water temperatures recorded (DW, RK) or via Troll probes (MT, NC, LT, TP).
- Dissolved inorganic carbon [DIC]: water samples collected within 15 minutes of flux measurement; triplicate samples stored in pre-acidified exetainers and analyzed within ~6 months using Gas Bench/Delta V Plus.
- pCO2: calculated from [DIC], pH, and temperature.
- Calibration and QA:
  - Troll 9000: calibrations ~every 5 weeks (two-point, pH4/pH7); field cleaning after each calibration.
  - Troll 9500: calibrations ~monthly (two-point); electrolyte top-up as needed; field cleaning weekly.
  - [DIC] standards run (six standards) with drift monitored by mid-range standard.

## Data structure and units

- Data stored in a single CSV file: CO2 efflux and hydraulic data for two Scottish and four Amazonian streams 2011-2013.
- 11 columns:
  1) Date (dd/mm/yyyy)
  2) Region (Amazon Basin or Scotland)
  3) Site (stream name)
  4) Mean CO2 efflux (μmol CO2 m−2 s−1)
  5) Standard deviation of mean CO2 efflux
  6) Flow (m s−1)
  7) Water depth (m)
  8) pCO2 (μatm)
  9) [DIC] (mM C)
  10) pH
  11) Water temperature (°C)
- Missing values indicated as NA.

## Quality control and data gaps

- Missing data:
  - DIC and pCO2 data missing for June 2012–January 2013 at DW and RK due to non-collection period.
  - MT dried up during Sep–Nov 2011; no samples possible.
  - Other gaps due to equipment failure, high flow limiting access.
- Data quality:
  - All values within method detection limits when collected.
  - RK pH data downgraded to calculated relationship due to instrument failure; R2 0.72 with discharge data.
  - Data availability and metadata allow reproducibility and cross-site comparisons with documented uncertainties.

## Analytical usage and considerations

- This dataset enables analyses of:
  - Correlations between CO2 efflux and hydraulic parameters (ū, Fr, Re) across different stream types and climates.
  - Influence of water chemistry (pCO2, pH, [DIC], temperature) on gas exchange rates.
  - Seasonal and catchment-scale variability in CO2 outgassing in tropical rainforest versus peatland and semi-urban streams.
- Caveats:
  - Incomplete Fr/Re data for Amazon sites; some pH measurements are model-derived rather than direct.
  - Data gaps require careful handling in analyses (e.g., imputation or site-specific modeling).
  - Chamber-based fluxes assume uniform surface conditions; surface state is qualitatively assessed.

## References

- Documentation and methods references included (field and laboratory protocols, calibration, and analytical approaches) for CO2 flux measurements, DIC analysis, pH/temperature instrumentation, and related hydrological calculations.