# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Datasets of stable isotope compositions (δ18O, δ2H) and d-excess for waters within the Five Lakes of Mikata catchment.
- Sampling periods: March 2011–January 2012 and July 2020–July 2022.
- Sample types include precipitation (event-based), weekly river water, and weekly lake water; plus Lake Suigetsu water temperature and salinity profiles by depth on six dates (2020–2022).
- Additional data accompanying isotope data: total precipitation and average temperature during each subsampling period; Netatmo weather data (temperature, humidity, precipitation, wind) to explore climatic influences.
- Data purpose: assess whether catchment water composition reflects East Asian Monsoon variability.

## Data Collected
- Water samples: 463 lake/river samples; 120 rainwater samples.
- Lake Suigetsu water-column profiling: ~70 samples per date across depths from surface to 34 m.
- Weather and environmental context: Netatmo station readings; precipitation totals; mean temperatures.
- Sampling locations include Hasu River, Lake Mikata, and Lake Suigetsu; positions adjusted between campaigns but within the same depth range to reflect average surface conditions.

## Collection/Generation Methods
- Water collection: top ~50 cm of water; minimal headspace; occasional location changes due to accessibility; algae presence filtered with 50 µm PET filter.
- Rainwater sampling: on-event basis; silicon oil used to prevent evaporation; snowmelt samples collected and processed similarly.
- Depth-resolved water-column sampling at Lake Suigetsu on six dates; pre- and post-sampling measurements of temperature and salinity.
- Instruments and analyses:
  - Oxygen isotopes (δ18O) measured with Isoprime 100 IRMS using CO2 equilibration; standards CA-HI and CA-LO calibrated to VSMOW2.
  - Hydrogen isotopes (δ2H) measured with TC-EA-IRMS; samples converted to water vapor and then to H2 for analysis; same standards referenced to VSMOW.
  - d-excess calculated from δ18O and δ2H values.
- Quality and timing notes: occurrence of sampling-day constraints (weather, lake conditions) noted; precipitation data for the 2011–2012 period did not include accompanying water-column data.

## Data Structure & Content (Two CSV Files)
- mikatagoko_modernisotopes_results.csv
  - Contains isotope data (δ18O, δ2H, d-excess), total precipitation, and average temperature for each observation period.
  - Key fields include sample type/position, location, sampling depth (for water column samples), batch, sample number/code, corrected isotope values (versus VSMOW2), and time stamps.
- lakesuigetsu_tempsalinity_results.csv
  - Contains Lake Suigetsu water temperature and salinity by depth for six dates.
  - Fields include sampling date, depth, temperature (°C), and salinity (%).

## Data Quality & Validation
- Isotope values corrected against laboratory standards; reported standard deviations: δ18O ≈ <0.05‰, δ2H ≈ <0.5‰.
- Data reflect multiple influences beyond simple evaporation: precipitation chemistry, transit through the catchment, lake–sea interactions, and minor evaporation effects in lakes.
- Sampling adjustments and accessibility issues acknowledged; sampling locations remain representative of lake surface conditions.

## Metadata & Discoverability
- Detailed data dictionary embedded in the first CSV (field meanings, units, and data interpretation rules).
- Clear documentation on sampling campaigns, positions, and methods to support reproducibility and reuse.
- Data structured to support integration with broader hydrological and climatic analyses focused on monsoon variability.

## Relevance for Data Leaders
- Demonstrates end-to-end data stewardship: clearly defined collection protocols, rigorous analytical methods, and comprehensive metadata for discoverability and reuse.
- Highlights data governance considerations:
  - Managing data across multiple campaigns with varying sampling locations and periods.
  - Ensuring consistent metadata, units, and reference standards (VSMOW2) across datasets.
  - Providing accompanying contextual data (precipitation, temperature, weather station data) to support meaningful analysis.
- Identifies potential data gaps and coordination needs:
  - Gaps in precipitation-only data for the 2011–2012 period lacking water-column context.
  - Variability in sampling locations due to accessibility, underscoring the need for clear documentation of how changes affect comparability.
- Supports user-centered data practices:
  - Dataset designed to investigate climate–hydrology relationships (East Asian Monsoon variability) with suffixes for sample types and precise location codes, facilitating reuse by policy, researchers, and partners.
- Exemplifies collaboration potential within the wider data community to enhance system-wide understanding of catchment hydrology and isotopic records.