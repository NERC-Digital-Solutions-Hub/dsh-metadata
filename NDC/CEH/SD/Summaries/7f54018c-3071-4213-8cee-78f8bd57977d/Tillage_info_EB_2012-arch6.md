# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

## Study overview
- Investigates fluxes of N2O from two adjacent 5.4 ha fields in Easter Bush, Scotland, before and after a tillage event on 1 May 2012.
- Climate: temperate maritime; ~921 mm annual rainfall; ~9°C average temperature (2001–2011).
- Fields: tilled (South Field) vs un-tilled (North Field); both managed for intensive livestock production for ≥20 years, mainly grazed by sheep; typical fertiliser regime ~200 kg N ha⁻¹ yr⁻¹.
- Tillage and management events included glyphosate pre-kill, ploughing to 30 cm, harrowing, rolling, and reseeding with ryegrass; fertilisation continued as usual in the un-tilled field but was reduced in the tilled field after tillage.

## Experimental design
- Two measurement approaches employed in parallel:
  - Eddy covariance setup on 27 March 2012 to capture continuous ecosystem-scale N2O fluxes.
  - Static and dynamic chamber techniques to measure soil N2O fluxes at discrete times.
- Data collection windows encompassed pre- and post-tillage periods to assess short- and medium-term responses.

## Data collection methods

### Eddy covariance measurements
- Instrumentation:
  - 3-axis ultrasonic anemometer (WindMaster Pro) at 2.4 m height.
  - Quantum cascade laser (QCL) analyser for N2O, H2O, CO2 at 10 Hz.
- Data processing:
  - Fluxes computed at 30-minute intervals using the covariance of gas mixing ratio (χ) and vertical wind speed (w): Fχ = ĥχ′w′.
  - Processing steps included double coordinate rotation (vertical and crosswind), spike removal, block averaging, and time lag removal by covariance maximisation.
  - Corrections for system frequency response (high and low-frequency losses) using Moncrieff et al. (1997) methods.
  - Density fluctuation corrections applied on a half-hourly basis (Burba et al., 2012).
  - Quality control per Foken et al. (2005); data were categorized and filtered to remove poor-quality measurements.
- Data attribution and exclusions:
  - Initial field assignment: flux data with wind directions 180–270° attributed to the tilled field; wind directions >330° or <100° attributed to the un-tilled field.
  - Data outside these allocations (obstructions by cabin/fence) discarded.

### Chamber measurements
- Static chambers:
  - PVC cylinders, 38 cm ID, 22 cm height; inserted 5 cm into soil; ~20.4 L headspace.
  - Procedure: chambers closed for 40 minutes; three 100 mL samples collected (t = 0, 20, 40 min).
  - Volume and ground area corrections performed; N2O flux calculated from rate of concentration change (dC/dt) using F = (dC/dt) × (ρV/A).
- Dynamic chambers (with QCL):
  - Chamber diameter ~39 cm, height ~22 cm; placed on soil via collars (≈5 cm depth) for at least 15 minutes before measurement.
  - Connection to instrument: ~30 m of tubing; flow rate ~6–7 L min⁻¹; ~22 s lag time.
  - Fluxes calculated from 1 Hz data over 3 minutes using both linear and non-linear regression methods; best-fitting method selected per measurement.
  - Detection limit for dynamic chamber method ≈ 0.04 nmol m⁻² s⁻¹ (much lower than static chamber method, ~0.4 nmol m⁻² s⁻¹).

## Data processing and quality control

- Eddy covariance corrections and processing:
  - Time lags and coordinate rotations applied; spike removal; lag optimization via covariance.
  - Density corrections and frequency response corrections applied.
  - Data quality filtered to exclude poor-quality flux measurements (category 2 in the cited scheme).
- Field delineation:
  - Flux data initially separated by wind direction to assign to tilled vs un-tilled fields; obstructions led to data loss in some periods.
- Data products produced:
  - Time-series fluxes (30-minute blocks) for N2O, CO2, H2O, along with meteorological variables (wind speed, wind direction, friction velocity u*, Monin-Obukhov length L, (z-d)/L, Bowen ratio, etc.).
  - QC metrics and corrections stored alongside flux data.

## Datasets and variables

- Easter_Bush_EddyC_Tillage_2012:
  - Time-stamped eddy covariance data including:
    - tau, corrected momentum flux
    - H (sensible heat flux), LE (latent heat flux)
    - co2_flux, h2o_flux, n2o_flux
    - wind_speed, max_wind_speed, wind_dir
    - u*, TKE, L, (z-d)/L, bowen_ratio
  - Both uncorrected and corrected values available.
- Easter_Bush_Chambers_Tillage_2012:
  - Chamber measurements with fields including:
    - Location, Field name, Method (Chamber method), Flux (nmol N2O m⁻² s⁻¹)
    - Date, Time
    - Air_Temperature, WC (soil water content), Air_pressure, PAR
    - Soil_Temperature, Rainfall
- Table 1: Field management events for tilled and un-tilled fields in 2012 (dates of key activities: pre-tillage glyphosate, tillage date, harrowing, sowing, fertiliser applications, grazing events).

## Challenges and considerations
- Patchy data due to environmental and equipment constraints; some data discarded due to obstructions affecting wind measurements.
- Delineation between tilled and un-tilled fields relies on wind direction, which can introduce data selection biases during certain periods.
- Static chamber measurements can be influenced by microclimate within chambers; dynamic chamber method offers improved sensitivity but requires careful lag and regression method selection.

## Potential data uses and applications
- Cross-validation of eddy covariance N2O fluxes with chamber-based measurements.
- Analysis of N2O flux responses to tillage, fertiliser timing, grazing, and seasonal changes.
- Development of data products (dashboards, self-serve analyses) to explore soil-atmosphere N2O exchange across management practices.
- Integration with broader policy or land-management studies in agricultural systems to improve data-driven decision-making.