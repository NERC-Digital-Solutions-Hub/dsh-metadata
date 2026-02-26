# Supporting documentation for data

## Overview of the Clocaenog field site
- Automated manipulation experimental site in Clocaenog Forest, North East Wales (53°03'19''N, -03°27'55''W).
- Purpose: investigate potential climate changes for upland moorland habitat over the coming decades.
- Features: replicated drought and warming treatments; roof technology powered by solar and wind.
- Habitat: upland west-atlantic moorland dominated by Calluna vulgaris (heather) >60% of plant biomass; other species include Vaccinium myrtillus and Empetrum nigrum.
- Data series, methods, and changes summarized in related supporting documentation.

## Measurements and cadence
- Measurements are taken fortnightly and cover:
  - Rainfall (mm)
  - Plot-level rain throughfall (mm)
  - Water table depth (cm)
  - Soil respiration (mg CO2-C m-2 hr-1)
  - Soil temperature (°C)
  - Soil moisture (vol%)
  - Photosynthetic active radiation (PAR; µmol m-2 s-1)
- Data are collected per plot (10+ plots referenced for depth measurements; some maximum depths listed per plot).

## Measurement methods and data handling by parameter

- Rainfall
  - Measured with a ground-level storage rain gauge (funnel diameter 12.7 cm).
  - Rain accumulated over two weeks; holiday periods may extend to 3–4 weeks.
  - Storage gauge data preferred over AWS data due to robustness (less downtime/power loss).
  - Hourly data not always required; data remain robust for bi-weekly summaries.

- Throughfall
  - Collected bi-weekly using a funnel (16.8 cm diameter) and a 3000 mL bottle per plot.
  - Throughfall data require calculations to align with site-wide annual rainfall; use percent difference relative to site rainfall.
  - Data points lost or compromised (e.g., funnel detachment) are excluded and flagged as NA.
  - Seasonal/annual data derived by applying throughfall percent changes to site rainfall data.

- Water table depth
  - Measured bi-weekly with water-permeable tubes installed to bedrock (installed 2009).
  - Depths recorded with a tape and head torch; field sheets then entered into a raw data master file.
  - Maximum detectable depths specified per plot (e.g., plot-specific cm limits).

- Soil respiration
  - Measured bi-weekly with three opaque soil collars per plot (20 cm diameter; installed 5–10 cm deep in 1999).
  - Respiration includes both heterotrophic and autotrophic components; vegetation around collars kept intact.
  - In 2013, larger collars installed for automated measurements at one collar per plot.
  - From 2014, measurements use an infrared gas analyser (EGM4) linked to SRC-1 chamber; 120-second sampling.
  - Data processing: raw data converted to mg CO2-C m-2 hr-1; conversion from g CO2 m-2 hr-1 to mg CO2-C m-2 hr-1 using a factor (0.272727 × 1000).
  - Three measurements per plot averaged; unrealistically high values excluded.

- Soil temperature, soil moisture, PAR
  - Measured near soil respiration chambers with handheld devices (digital thermometer for temperature; Theta Probe ML3 for moisture; pyranometer for PAR).
  - Measurements linked with plot-level micro-meteorological data and AWS data to support robust analysis.
  - Prefer micro-meteorological and AWS data over handheld measurements, though plot-level variation may still be informative.
  - Data collected on field sheets and transferred to Excel; values averaged per plot.

## Data processing, quality, and integration considerations
- Field data are consolidated into Excel tables; per-plot averages produced for analysis.
- Data quality emphasis: exclude implausible outliers (e.g., in soil respiration) and flag missing values as NA where appropriate.
- Data integration: micro-meteorological and AWS datasets are recommended to complement plot-level measurements, ensuring more accurate interpretation of spatially variable responses.
- Data transformation notes include the specific conversion for soil respiration units and the method to derive site-appropriate rainfall figures from throughfall data.

## Spatial and GIS relevance
- Per-plot measurements (with explicit depth and climate-related variables) enable spatial analyses across the study plots within Clocaenog Forest.
- Coordinates and plot-level data support map-based visualization of spatial patterns in rainfall partitioning, groundwater table dynamics, soil respiration, and surface radiation.
- Documentation highlights the importance of data provenance, consistent data standards, and clear handling of missing or compromised data for reliable GIS mapping and analysis.