# Seasonal river water temperatures and climatic drivers for 35 sites on 21 rivers and streams (1984 - 2007)

- Overview
  - Investigates how seasonal river water temperature (WT) relates to climatic drivers, with implications for ecology, water quality, and services (e.g., power plant cooling, recreation).
  - Addresses climate change context by exploring large-scale spatial and temporal variability in climate–WT relationships and the role of basin properties.
  - Combines observed WT with a consistent set of modeled climate data to enable multi-site synthesis across Great Britain.

- Data scope and provenance
  - 35 WT monitoring sites across 21 rivers within 16 basins, Great Britain, 1984–2007.
  - Six modeled climate variables matched within 1 km of each site; all variables are three-month seasonal averages.
  - WT data compiled from multiple CEH projects; climate data from the CHESS dataset (downscaled from MORECS data, with daily values for 1971–2007).
  - Data are prepared to support modelling of climate–WT associations and to inform hydrology, ecology, and management research.

- Dataset structure and key variables
  - Core columns and definitions:
    - UID: unique identifier
    - Year: data collection year
    - Season: season code (1 = winter, 2 = spring, 3 = summer, 4 = autumn)
    - Num Days: number of days used to compute the 3-month average
    - WT: 3-month average water temperature (°C)
    - AT: 3-month average air temperature (°C)
    - SWR: 3-month average short-wave radiation (W/m^2)
    - WS: 3-month average wind speed (m/s)
    - SH: 3-month average specific humidity (kg/kg)
    - P: 3-month average precipitation (kg/m^2/day; equivalent to mm/day)
    - LWR: 3-month average long-wave radiation (W/m^2)
    - Time: time index for modelling (e.g., 1.0 for winter 1984, 1.25 for spring 1984, etc.)
    - Dataset: dataset name
    - Basin, River, Site: geographic identifiers
    - NGR, Easting, Northing: British National Grid coordinates
  - All values represent 3-month seasonal averages derived from daily or daily-representative measurements.

- Seasonal derivation and data processing
  - Daily WT data were aggregated to daily values where possible; in some sites, spot measurements represented a single day.
  - Daily WT and climate data were aligned by date.
  - Seasonal averages were computed using standard definitions:
    - Winter: December of year y-1 to February of year y
    - Spring: March–May
    - Summer: June–August
    - Autumn: September–November
  - Time indices encode season and year, enabling consistent cross-site modelling.

- Data sources, methods, andReferences
  - Water temperature data from CEH and associated field studies (varied temporal resolutions; WT was not always the primary focus of source projects).
  - Climate data from CHESS, serving as forcing data for JULES and providing 1-km gridded, daily climate series.
  - References include foundational work on JULES, regional river temperature studies, and related hydrology/ecology research for context and methodological grounding.

- Data governance, quality, and usability considerations
  - Data harmonization across multiple projects enhances comparability but includes variability in measurement approaches and temporal resolution.
  - Spatial alignment to 1-km CHESS cells requires careful pairing of site data with climate forcing in analyses.
  - Metadata (unit definitions, season coding, and geographic descriptors) supports discoverability and reuse for climate–ecology modelling and policy-relevant assessments.
  - The dataset structure is designed to support scalable analyses across sites and basins, with clear provenance and documentation of processing steps.

- Relevance for data leaders and data strategy implications
  - Demonstrates integration of heterogeneous, multi-source data (observations + modeled climate) into a unified, comparable dataset.
  - Highlights importance of standardized temporal aggregation (3-month seasonal means) to enable cross-site comparisons.
  - Emphasizes rigorous metadata, spatial referencing, and clear documentation of data provenance to improve discoverability, reusability, and governance.
  - Provides a model for coordinating data from diverse projects to support large-scale analyses of environmental drivers and outcomes, informing climate adaptation and resource management decisions.