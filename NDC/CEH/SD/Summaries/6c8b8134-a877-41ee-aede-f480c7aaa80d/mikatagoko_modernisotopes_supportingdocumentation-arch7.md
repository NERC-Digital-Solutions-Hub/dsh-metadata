# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Provides stable isotope data (δ18O, δ2H) and d-excess for waters in the Five Lakes of Mikata catchment.
- Time periods: March 2011–January 2012 and July 2020–July 2022.
- Sample types: precipitation (event-based), weekly river water, weekly lake water; accompanying precipitation totals and average temperatures per subsampling period.
- Lake Suigetsu depth profiles include water temperature and salinity on six dates across 2020–2022 to assess stratification and hydrological processes.
- Study purpose: investigate whether catchment water composition records East Asian Monsoon variability.

## Data Collection and Methods
- Samples: 463 lake/river water samples collected weekly (2011/12 and 2020/22) from Hasu River, Lake Mikata, and Lake Suigetsu.
- Precipitation samples: 120 samples collected on an event basis; rainfall captured with a custom funnel and glass bottle; silicon oil used to prevent evaporation; snowfall samples collected from pristine snow.
- Weather data: automated Netatmo weather station for temperature, humidity, precipitation amount, and wind.
- Water-column profiling: conducted ~quarterly at six dates with depth-stratified sampling (surface to 34 m) using a sealable van Dorn sampler; temperature and salinity measured with a Hydrolab DS5 (high-resolution dates) or a TOA-DKK WQC-24 (August 2021).
- Analytical methods:
  - δ18O measured by Isoprime 100 IRMS with CO2 equilibration; standards CA-HI and CA-LO used for calibration to VSMOW2; typical SD < 0.05 ‰.
  - δ2H measured by TC-EA-IRMS with liquid autosampler; samples run in duplicate; SD < 0.5 ‰.
  - d-excess calculated from δ18O and δ2H (deviations from the Global Meteoric Water Line).
- Data corrections: laboratory standard corrections; data affected by precipitation amount, transit through catchment, lake–Sea of Japan interactions, and evaporation; sampling location changes deemed not to bias isotope values substantially.

## Data Content and Structure
- Two CSV files:
  - mikatagoko_modernisotopes_results.csv: isotope data (δ18O, δ2H, d-excess), plus total precipitation and average temperature for each observation period.
  - lakesuigetsu_tempsalinity_results.csv: water temperature and salinity by depth for Lake Suigetsu on six dates (2020–2022).
- Key fields (as described in the dataset documentation):
  - Sample Type (LakeRiver, Rainwater, Column)
  - Location and Sampling Position
  - Sampling Depth (for water-column samples)
  - Dates and times of vessel setup/sealing (precipitation samples)
  - Corrected δ18O and δ2H (with reference to VSMOW2)
  - d-excess
  - Total Precipitation and Average Temperature (for precipitation samples)
  - Sampling Date, Depth, Water Temperature, Water Salinity (Lake Suigetsu data)
- Sampling locations include Hasu River, Mikata, Suigetsu, with multiple reference codes and notes detailing accessibility and changes over time.

## Spatial and Temporal Coverage
- Spatial: Hasu River, Lake Mikata, Lake Suigetsu (plus surrounding catchment references and sampling positions around each site).
- Temporal: two main periods (2011/12 and 2020/22); precipitation data aligned to specific sampling windows; lake water-column profiles across six dates within 2020–2022.
- Depths: water-column samples from surface to 34 m, with finer resolution near the surface and deeper ranges as described.
- Associated data: concurrent weather data (temperature, precipitation) to support interpretation of isotope signals.

## Quality, Uncertainty, and Limitations
- Quality control: samples corrected using laboratory standards; cross-referenced against international standards (VSMOW2, SLAP2, GISP).
- Uncertainties: δ18O typical SD < 0.05 ‰; δ2H typical SD < 0.5 ‰.
- Potential influences: precipitation composition and amount, catchment transit times, interactions with Sea of Japan, lake evaporation, and sampling-location changes between periods (not expected to skew results beyond the intended representativeness).

## GIS and Data Utilization Opportunities
- Map and analyze spatial patterns of isotope composition across lakes and catchment features.
- Integrate isotopic data with precipitation and temperature data to explore monsoon-related variability.
- Use depth-resolved temperature and salinity data from Lake Suigetsu to study lake mixing and surface–deep water interactions in a GIS context.
- Combine with time-stamped sampling to build spatiotemporal isotope surfaces or time-series visuals for policy, stakeholders, or public audiences.
- Data structure supports linking to other GIS layers via sampling location codes and coordinates, enabling multi-layer analyses.

## Data Files and Access Details
- mikatagoko_modernisotopes_results.csv: isotope data, precipitation totals, and average temperatures by observation period.
- lakesuigetsu_tempsalinity_results.csv: depth-resolved temperature and salinity data for Lake Suigetsu across six sampling dates.
- Sampling locations and codes are documented to facilitate geospatial integration and reproducibility.