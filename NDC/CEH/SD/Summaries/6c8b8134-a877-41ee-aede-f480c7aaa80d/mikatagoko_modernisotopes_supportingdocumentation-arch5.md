# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Dataset of stable isotope compositions (δ18O, δ2H) and d-excess for waters in the Five Lakes of Mikata catchment, spanning March 2011–January 2012 and July 2020–July 2022.
- Sample types include event-based precipitation, weekly river water, and weekly lake water; plus water temperature and salinity profiles with depth in Lake Suigetsu during 2020–2022.
- Purpose: to determine if catchment water composition reflects East Asian Monsoon variability.

## Collection and Generation Methods
- Sampling regime:
  - Lakes and rivers: 463 samples collected weekly across two intervals; sampling locations adjusted between intervals but within similar depth ranges to reflect average surface conditions.
  - Precipitation: 120 rainwater samples collected on an event basis; snowfall samples collected from pristine areas.
- Field procedures:
  - Water samples collected from top ~50 cm; algae filtered when present.
  - Rainwater collected with a 3D-printed funnel and glass bottle holder; silicon oil added to prevent evaporation; samples processed with a Teflon pipette.
  - Automated weather data via Netatmo station (temperature, humidity, precipitation) to accompany isotope data.
  - Lake Suigetsu water-column profiling approximately quarterly: sampling at the centre of the lake from surface to 34 m depth with a van Dorn sampler and a Hydrolab DS5 for temperature/salinity.
- Analysis and standards:
  - Oxygen isotopes (δ18O) measured by Isoprime 100 mass spectrometer with CO2 equilibration; calibrated to VSMOW2 using internal standards CA-HI and CA-LO; typical precision <0.05 ‰.
  - Hydrogen isotopes (δ2H) measured in duplicate by TC-EA-IRMS with five replicates per sample; calibrated to VSMOW using CA-HI/CA-LO; typical precision <0.5 ‰.
  - d-excess calculated from δ18O and δ2H (standard relation used to assess evaporation effects relative to the Global Meteoric Water Line).
- Data context: precipitation, river, lake data complemented by temperature and depth-resolved water chemistry data for Lake Suigetsu.

## Sampling Locations, Dates, and Structure
- Sampling periods:
  - 2011–2012: March 2011 to January 2012 (lake/river focus; precipitation data limited to pilot context for this period).
  - 2020–2022: July 2020 to July 2022 (comprehensive lake, river, and precipitation data with depth profiles for Lake Suigetsu).
- Location metadata and depth data are recorded; tables provide codes for Hasu River, Mikata, Suigetsu, and various Mikata sampling sites with precise coordinates and notes on accessibility.

## Data Files and Structure
- mikatagoko_modernisotopes_results.csv
  - Contains isotope data (δ18O, δ2H, d-excess) plus total precipitation and average temperature for each observation period.
  - Fields include sample type (lake/river/rain), sampling location, sampling depth (where applicable), vessel dates/times, corrected isotope values on the VSMOW2 scale, and related metadata (batches, sample numbers, location notes).
- lakesuigetsu_tempsalinity_results.csv
  - Contains water temperature and salinity by depth for Lake Suigetsu across six dates within the 2020–2022 interval.
  - Fields include sampling date, sampling depth, temperature (°C), and salinity (%).

## Quality Control
- Lab corrections performed against internal standards; results anchored to international references (VSMOW2, SLAP2, GISP).
- Accuracy influenced by:
  - Precipitation composition and amount.
  - Transit times through the catchment and lake-sea interactions.
  - Minor evaporation effects in processing.

## Data Limitations and Considerations for Data Stewards
- 2011–2012 precipitation data and water-column data are not accompanied by full precipitation/water-column metadata consistent with later intervals (pilot study scope).
- Sampling location changes between intervals are within comparable depth ranges, but some local input effects may not be fully captured.
- Metadata-rich design supports discovery, provenance, and reuse, with explicit coordinates, sampling depths, dates, and method details.

## Governance and Stewardship Implications
- The dataset is well-structured for sharing and interoperability, with:
  - Clear variable definitions, units, and data types.
  - Provenance through batch and sampling metadata, methods, and calibration references.
  - Versioned, reproducible measurement and calculation workflows (δ18O, δ2H, d-excess).
- Recommendations for data stewards:
  - Maintain and publish these two CSV files with full metadata and versioning.
  - Ensure linkage to sampling site coordinates, depths, and dates for traceability.
  - Provide clear documentation of any changes in sampling locations and intervals to support reproducibility and comparability across periods.
  - Consider integration with broader isotope datasets and monsoon-variability studies to maximize reuse.