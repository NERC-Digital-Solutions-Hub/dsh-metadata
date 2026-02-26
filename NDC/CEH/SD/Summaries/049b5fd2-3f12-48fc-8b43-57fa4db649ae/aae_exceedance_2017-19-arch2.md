# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2017-19.

- Purpose and scope
  - Provide 1x1 km AAE data sets for acidity and nutrient nitrogen critical loads due to deposition for 2017–2019.
  - Enable monitoring of environmental health and policy performance across grid squares, linked to habitat sensitivity.

- How AAE is calculated
  - For each habitat within a 1x1 km grid square:
    - AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - Sum AE over all habitats in the grid square.
  - AAE (keq ha-1 year-1) = total AE / total habitat area (ha) in the grid square.
  - If deposition is below the critical load, AAE is set to zero.
  - For nutrient nitrogen, AAE values can be converted to kg N ha-1 year by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year).
  - Acidity exceedance represents a mix of sulfur and nitrogen compounds; expressed in keq ha-1 year-1 only.

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed (productive) coniferous woodland, managed (productive) broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
  - Nutrient nitrogen: all acidity habitats plus unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

- Data sources and references
  - UK Methods Report (Hall et al, 2015) provides full description of methods for calculating UK critical loads and exceedances.
  - Summary exceedance statistics and Trends Reports (e.g., Hall et al, 2017; Rowe et al, 2019) include broader context and freshwater coverage.
  - CBED deposition data and Critical Loads data available from the EIDC.

- Quality control and interpretation notes
  - Methods are aligned with national/international guidance from UNECE CLRTAP; detailed transparency in Hall et al. 2015.
  - Critical loads/exceedances are based on steady-state or empirical methods; exceedance indicates potential long-term harm, not immediate damage.
  - Habitat distribution maps used for critical loads/exceedances may differ from other national habitat maps; total habitat areas may differ between acidity and nitrogen calculations.
  - Reducing deposition below the critical load does not imply immediate ecological recovery; chemical and biological recovery can be slow and time-lagged.
  - Uncertainties exist in habitat mapping and critical loads; see Hall et al. 2015 and accompanying metadata.

- Data structure and availability
  - Two files: acidhab_AAE_2017-19.csv (acidity) and nutnhab_AAE_2017-19.csv (nutrient nitrogen).
  - Coverage differs between the two files due to habitat distributions.
  - Unique1km field provides a unique identifier for each 1x1 km grid square; allows linking acidity and nitrogen data for the same squares when present in both sets.
  - Key fields:
    - East_m, North_m: center coordinates in OSGB grid (metres).
    - Unique1km: unique grid square identifier.
    - AAE_keq: Average Accumulated Exceedance value (keq ha-1 year-1).
    - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.

- File structure references
  - acidhab_AAE_2017-19.csv for acidity data.
  - nutnhab_AAE_2017-19.csv for nutrient nitrogen data.
  - Table 1 describes the data fields and their meanings.

- Additional information
  - Access to critical loads and CBED deposition data via EIDC; meta-data and documentation available through CEH/CLDM resources.
  - Timescale considerations: AAE reflects long-term exceedance potential rather than immediate ecosystem response.