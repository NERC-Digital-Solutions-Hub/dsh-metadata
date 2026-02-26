# Nitrous oxide fluxes and associated soil measurements from a mixed livestock farm

## Overview
- Investigates soil N2O fluxes using a high-precision dynamic closed chamber system and a quantum cascade laser (QCL) gas analyser at Easter Bush Farm Estate, Midlothian, UK.
- Timeframe: measurements from autumn 2012 to summer 2013, across four seasonal periods.
- Scope: >500 flux measurements across the farm; 457 soil measurements accompanying most flux measurements.
- Site and management context: 20 fields representing arable fodder crops and grazing pasture; fields accessible for flux measurements.

## Experimental Design and Data Collection
- Measurement approach: dynamic chamber methodology with a 7 L chamber, CO2 response used to check for leaks, and a mobile QCL analyser mounted in a vehicle.
- Chamber setup: circular chamber (39 cm diameter) placed on stainless steel collars inserted 5 cm into soil; 30 m radius for chamber placement.
- Instrumentation: pump circulated air between chamber and QCL gas analyser; measurement period per flux event about three minutes.
- Data captured at the following levels: measurement date, season/period, unique measurement ID, field, plot type, plot description, GPS coordinates (E/N), soil temperature, water-filled pore space (WFPS), bulk density, soil porosity, VWC, pH, NH4+, NO3-, total C and N.
- Soil sampling: two soil types collected at 457 locations (5 cm depth) immediately after flux measurement; samples frozen to -18°C, later analysed for pH, NH4+, NO3-, bulk density, moisture, and total C/N.
- Sample handling: soil samples for bulk density measured with a 7.4 cm diameter, 5 cm deep ring; wet chemistry and instrumental analyses performed after storage.

## Soil Measurements and Laboratory Analyses
- pH: measured in water using standard soil pH protocol.
- Inorganic N: NH4+ and NO3- extracted with 1 M KCl; analysed with Bran and Luebbe AutoAnalyser.
- Soil physical properties: bulk density, porosity, volumetric water content (VWC), WFPS calculated from bulk density; moisture content by oven drying.
- Soil chemistry: total carbon (Tot_C) and total nitrogen (Tot_N) via grinding samples for elemental analysis.
- Sample handling: immediate post-measurement sampling; samples stored at -18°C and analysed within two months.

## Data Structure and Metadata
- File name: Farm_Flux_and_Soil.
- 21 data fields include:
  - Date (dd/mm/yyyy)
  - Period (season and year)
  - Measurement_ID
  - Field
  - Plot type
  - Plot Description
  - GPS_E (easting)
  - GPS_N (northing)
  - Soil_T (°C)
  - SMAv (WFPS %)
  - BD_density (g cm^-3)
  - BD_Porosity
  - BD_VWC
  - BD_WFPS
  - pH
  - NH4N (g NH4+-N kg^-1)
  - NO3N (g NO3--N kg^-1)
  - Tot_C (g C kg^-1)
  - Tot_N (g N kg^-1)
  - Flux (µg N2O-N m^-2 h^-1)
  - Flux_Error (µg N2O-N m^-2 h^-1; 95% CI)
- Units provided for each field; date, period, and measurement identifiers support traceability and reproducibility.
- Data volume: 500+ flux measurements with 457 accompanying soil measurements across 20 fields.

## Analytical Methods and Quality Control
- Flux calculation: performed with the HMR package in R, employing multiple estimation methods and selecting the most appropriate fit per chamber set.
- Leak check: unstable CO2 responses led to data discard for those measurements.
- Data characteristics: flux and soil variables exhibit a log-normal distribution; outliers retained due to a lack of evidence deeming them unreliable.
- Documentation and references: methods and QA steps aligned with established literature (Cowan et al. 2014, 2015, 2017; Levy et al. 2011; Pedersen et al. 2010; Rowell 1994).

## Data Management, Accessibility and Reuse
- Metadata richness supports discoverability: measurement IDs, precise locations, temporal context, plotting descriptions, and instrument configurations.
- Data sharing readiness: dataset is organized for uploading to data portals and catalogues; provenance and methodological transparency are provided via detailed references.
- Reproducibility: use of established analytical tools (HMR in R) and published methodology enhances replicability and future reuse.

## Data Stewardship Considerations and Challenges
- Heterogeneous data sources and formats across field measurements, requiring consistent metadata standards.
- Timely data transfer from field to storage and handling large volumes of measurements.
- Ensuring complete metadata (plot descriptions, GPS coordinates, measurement IDs) to enable discoverability and reuse.
- Maintaining data provenance and versioning as methodologies or sites evolve or are expanded in follow-up studies.

## References
- Cowan, N.J., et al. 2014. An improved method for measuring soil N2O fluxes using a quantum cascade laser with a dynamic chamber.
- Cowan, N.J., et al. 2015. Spatial variability and hotspots of soil N2O fluxes from intensively grazed grassland.
- Cowan, N.J., et al. 2017. Nitrous oxide emission sources from a mixed livestock farm.
- Levy, P.E., et al. 2011. Quantification of uncertainty in trace gas fluxes measured by the static chamber method.
- Pedersen, A.R., et al. 2010. A comprehensive approach to soil-atmosphere trace-gas flux estimation with static chambers.
- Rowell, D.L. 1994. Soil science: methods and applications.