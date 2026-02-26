# Soil Gas Flux Measurements Data Schema

- A data schema documenting soil gas flux measurements (CO2, CH4, N2O) from static chamber experiments, including treatments with biochar and wetting, across multiple sites and timepoints. The dataset combines raw measurements with derived fields for analysis and mapping in GIS.

## Key identifiers and timing
- soilcoreno: Individual soil sample/core identifier
- timepoint: Timepoint of measurements
- dayfromstart, dayfromstartstring: Days since start (numeric and string)
- datetime: Date and time of measurement
- midpointday: Middle point between timepoints
- timeinterval, timeintervalstring: Time interval between consecutive measurements (numeric and string)

## Treatments and experimental design
- biochartreatment: Indicates un-amended or biochar-amended samples
- fulltreatname: Full name of the soil treatment (biochar and wetted)
- biocharweight: Dry biochar weight added
- biocharfraction: Proportion of biochar relative to dry soil weight
- wettingtreatment: Whether soil was periodically wetted to high water content
- temperaturetreatment: Soil temperature treatment
- nitrogentreatment: 15N-labeled nitrogen form (NH4+ or NO3-)

## Measurements (gas fluxes and primary measurements)
- mgCO2-Cfluxm2h1: CO2 flux (mg CO2-C per m2 per hour)
- log10co2: log10(flux + 1) for CO2, with negative-flux adjustment
- ugCH4-Cfluxm2h1: CH4 flux (mg CH4-C per m2 per hour)
- log10ch4: log10(flux + 1) for CH4, with negative-flux adjustment
- ugN2O-Nfluxm2h1: N2O flux (mg N2O-N per m2 per hour)
- log10n2o: log10(flux + 1) for N2O, with negative-flux adjustment
- CO2ppmt0, CH4ppmt0, N2Oppmt0: Static chamber headspace gas concentrations at t0 (ppm)
- tempair: Air temperature at the time of gas measurement
- gravwatercontentproportion: Gravimetric soil water content (as proportion)
- chambaream2: Static chamber area (m2)
- headvolm3: Chamber headspace volume (m3)
- datetime: Timestamp of measurement (redundant with timepoint context)

## Soil and physical properties
- drysoilweightg: Dry soil weight in the core (g)
- bulkdensitygcm3: Soil bulk density (g/cm3)
- postmixbulkdensity: Bulk density after soil mixing (g/cm3)
- particledensitygcm3: Particle density (g/cm3)
- totalporosity: Total porosity (derived from densities: 1 - bulk density/particle density)

## Site, scope, and context
- site: Site identifier where soil was sampled
- wfpsproportion: Water-filled pore space (derived from gravimetric water content, bulk density, and porosity)

## Derived and transformation notes
- log10 fields are calculated as log10(flux + 1)
- If a flux is negative, the absolute value of the negative flux is added to flux values before logging (to avoid non-positive inputs)

## Data usage considerations for GIS
- Use site and datetime fields to map spatial and temporal trends of gas fluxes
- Link sample IDs (soilcoreno) to spatial geometries for map-based visualisations
- Compare treatments (biochar, wetting, temperature, nitrogen) across locations
- Integrate with soil property fields (bulk density, porosity, water content) to explain spatial variation in fluxes

## Practical notes
- Data likely originate from multiple sources with varying resolutions; ensure harmonisation of units and scales before GIS integration
- Consider data cleaning and validation steps to handle missing values and ensure consistency across timepoints and sites