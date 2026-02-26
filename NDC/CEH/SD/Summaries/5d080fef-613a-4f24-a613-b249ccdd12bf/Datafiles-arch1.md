# Datafiles

## Overview
- A catalog of datafiles describing rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, and runoff across three sites.
- Sites: semi-mature forest, reforested young forest, and degraded grassland.
- Includes raw and processed data, with high-frequency measurements (5–10 minutes) and daily runoff data, spanning roughly 2014–2015.
- Supplementary meta-files describe the study setup and data collection methods.

## Study sites and time frame
- Semi-mature forest site
- Young forest site (reforested tree fallow)
- Degraded grassland site
- Primary data period concentrated around 2014-10 to 2015-09 (with specific start/end dates varying by dataset)

## Data files and categories

- Meta and study description
  - Datafiles.rft: overview of files and available time periods
  - Study Sites.rtf: information on the three study sites
  - Methods.rtf: brief description of data collection methods and data contents

- Rainfall data (5-minute or raw/processed)
  - Forest_Rainfall_raw.csv: raw rainfall for semi-mature forest (2014-10-03 to 2015-09-30)
  - Forest_Rainfall_processed.csv: 5-minute rainfall for semi-mature forest (2014-10-01 to 2015-09-30)
  - ReforestedTF_Rainfall_raw.csv: raw rainfall for young forest site (period around 2014–2015)
  - ReforestedTF_Rainfall_processed.csv: 5-minute rainfall for young forest site
  - Degradedland_Rainfall_raw.csv: raw rainfall for degraded grassland (2014–2015)
  - Degradedland_Rainfall_processed.csv: 5-minute rainfall for degraded grassland (2014–2015)

- Micrometeorology (weather data)
  - Forest_micrometeorology.csv: 10-minute weather data for semi-mature forest (2014-10-15 to 2015-09-30)
  - ReforestedTF_micrometeorology.csv: 10-minute weather data for young forest site (2014-10-15 to 2015-09-30)
  - Degradedland_micrometeorology.csv: 5-minute weather data for degraded grassland (2014-10-01 to 2015-10-01)

- Throughfall (water reaching the ground)
  - Forest_Throughfall_automatic.csv: 5-minute throughfall data from gutters at semi-mature site (2014-10-01 to 2015-09-30)
  - Forest_Throughfall_manual.csv: throughfall data from manual gauges at semi-mature site (2014-10-01 to 2015-09-30)
  - ReforestedTF_Throughfall_automatic.csv: throughfall data for young forest site (2014-10-01 to 2015-09-30)
  - ReforestedTF_Throughfall_manual.csv: manual throughfall data for young forest site (2014-10-01 to 2015-09-30)

- Stemflow (water flowing down stems)
  - Forest_Stemflow_raw.csv: raw stemflow data for semi-mature site (2015-02-16 to 2015-09-30)
  - Forest_Stemflow_processed.csv: processed stemflow data for semi-mature site (2015-02-16 to 2015-09-30)
  - ReforestedTF_Stemflow_raw.csv: raw stemflow data for young forest site (2015-02-17 to 2015-09-30)
  - ReforestedTF_Stemflow_processed.csv: processed stemflow data for young forest site (2015-02-17 to 2015-09-30)

- Sapflow (sap flux density estimates)
  - Forest_Sapflow_raw.csv: temperature data used to estimate sap flux density for semi-mature forest (2014-10-01 to 2015-10-01)
  - Forest_Sapflow_processed.csv: sap flux density and sap flow data for semi-mature forest (2014-10-01 to 2015-10-01)
  - ReforestedTF_Sapflow_raw.csv: sapflow raw data for young forest site (2014-10-01 to 2015-09-30)
  - ReforestedTF_Sapflow_processed.csv: sapflow processed data for young forest site (2014-10-01 to 2015-10-01)

- Soil moisture (raw and processed)
  - Forest_Soilmoisture_raw.csv: raw soil moisture data for semi-mature forest (2014-10-15 to 2015-10-01)
  - Forest_Soilmoisture_processed.csv: processed soil moisture data for semi-mature forest (2014-10-15 to 2015-10-01)
  - ReforestedTF_Soilmoisture_raw.csv: raw soil moisture data for young forest site (2014-10-01 to 2015-10-15)
  - ReforestedTF_Soilmoisture_processed.csv: processed soil moisture data for young forest site (2014-10-01 to 2015-10-01)
  - Degradedland_Soilmoisture_raw.csv: raw soil moisture data for degraded grassland (two entries with different start/end dates)
  - Degradedland_Soilmoisture_processed.csv: processed soil moisture data for degraded grassland (two entries with different dates)

- Overland flow / runoff
  - Forest_Overlandflow.csv: daily runoff data for semi-mature forest site
  - ReforestedTF_Overlandflow.csv: daily runoff data for young forest site
  - Degradedland_Overlandflow.csv: daily runoff data for degraded grassland site (two entries corresponding to different date ranges)

- Soil heat flux (degraded site)
  - Degradedland_Soil_Heat_flux.csv: soil heat flux data for degraded grassland (two entries corresponding to date ranges)

## Data organization and use
- Datafiles, Study Sites, and Methods provide context and data collection details.
- Data are organized by site and by data type, with both high-frequency (5–10 minutes) and daily measurements.
- Suitable for cross-site comparisons, hydrological process analyses, and correlating climate variables with soil- and plant-scale responses.