# Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Aims and study design
- Deploy a high-precision flux chamber system to measure N2O fluxes at Easter Bush Farm Estate, Midlothian, UK.
- Conduct four seasonal measurement periods during 2012–2013; >500 flux measurements across the farm; 457 soil measurements paired with flux measurements.
- Selection of 20 fields representing a variety of management practices, including arable crops for fodder and grazing pastures.

## Measurement system and protocol
- Use a high-precision dynamic closed chamber system with a pump and a compact quantum cascade laser (QCL) analyser mounted in a vehicle for mobile measurements.
- Chamber: circular, 39 cm diameter; inserted 5 cm into soil with stainless steel collars.
- Sampling: 3-minute measurement period with air circulated between chamber and QCL via 30 m tubing to enable a 30 m radius around the vehicle.
- Flux calculation: based on the rate of change of gas concentration (dc/dt), volume, and air density; 95% confidence intervals calculated from regression integration.
- Quality checks: regression fit inspected for chamber leaks via CO2 response; data with unstable signals discarded.

## Soil measurements and sampling
- Two soil sampling types collected at 457 measurement locations: soil cores 5 cm deep for chemical and physical analyses; undisturbed cores for bulk density and moisture content assessments.
- Samples processed after collection: soil pH (in H2O) and inorganic N species (NH4+ and NO3−) via KCl extraction; total carbon and nitrogen contents via elemental analysis; soil moisture and bulk density derived from oven-dried samples.
- Water-filled pore space (WFPS) and other soil properties calculated from measured and derived values (e.g., bulk density, porosity, volumetric water content).
- Sampling and analysis followed established soil science methods; details referenced from Rowell (1994) and related sources.

## Variables and data structure
- Data file: Farm_Flux_and_Soil
- Key fields (21 total):
  - Date; Period (season/year); Measurement_ID; Field; Plot type; Plot Description
  - GPS_E (easting); GPS_N (northing)
  - Soil_T (soil temperature)
  - SMAv (WFPS %)
  - BD_density (bulk density, g cm^-3)
  - BD_Porosity (porosity)
  - BD_VWC (volumetric water content)
  - BD_WFPS (WFPS %; calculated)
  - pH (soil pH)
  - NH4N (ammonium content, g NH4+-N kg^-1)
  - NO3N (nitrate content, g NO3−-N kg^-1)
  - Tot_C (total carbon content, g C kg^-1)
  - Tot_N (total nitrogen content, g N kg^-1)
  - Flux (N2O flux, µg N2O-N m^-2 h^-1)
  - Flux_Error (95% CI of N2O flux)
- Units and measurement details are explicitly defined to support reproducible analyses.

## Analytical methods and quality control
- Fluxes calculated with the HMR package in R, using one of five methods per chamber set to best fit the data.
- Each regression examined for potential chamber leaks via CO2 response; unstable signals lead to data exclusion.
- Due to log-normal distribution and multiple flux sources, outliers in flux and soil variables were retained when not deemed unreliable.
- Dataset supports analyses of distribution characteristics (log-normal) and cross-variable relationships.

## Context, scope, and reproducibility
- Location: Easter Bush Farm Estate near Penicuik, Midlothian; operated by Scotland’s Rural College (SRUC) and the University of Edinburgh for commercial and research purposes.
- Timeframe: measurements conducted between autumn 2012 and summer 2013.
- References provided for methodological foundations (dynamic chamber N2O measurements, flux estimation methods, and related soil analyses) to enable replication and comparison with prior work.

## Implications for analysis and use
- The dataset enables exploration of spatial and temporal patterns in soil N2O fluxes in relation to management practices, soil properties, and environmental conditions.
- Potential analyses include: correlating N2O flux with soil moisture, pH, inorganic N pools, and soil C/N; evaluating seasonal effects; hotspot identification across fields.
- The documented metadata and QC procedures support robust statistical modeling and reproducibility, including potential development of predictive models or hotspot analyses.