# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2017-19

- Purpose and scope
  - Provide 1x1 km grid-based AAE data for acidity and nutrient nitrogen critical loads due to deposition for 2017–2019.
  - AAE summarizes exceedances across multiple habitats within each grid square.

- How AAE is calculated
  - For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
  - AAE (keq ha-1 year-1) = total AE across habitats in a grid square ÷ total habitat area in that square.
  - Values expressed in keq ha-1 year-1; for nutrient nitrogen, AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
  - If deposition is below the critical load, AAE is set to zero.
  - Acidity AAE represents a mix of sulphur and nitrogen compounds and cannot be expressed as kg of S or N separately.

- Habitats included
  - Acidity: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, and certain woodland types (productive and unmanaged coniferous and broadleaved woodlands).
  - Nutrient nitrogen: adds several woodland types (unmanaged beech, oak, Scots pine, and other unmanaged woodland), dune grassland, and saltmarsh, in addition to the habitats used for acidity.

- Data sources and context
  - Methods and data derived following the UK CLRTAP framework; detailed methods available in Hall et al. (2015) Methods Report.
  - Summary exceedance statistics by habitat and country published in Trends Report (e.g., Hall et al. 2017) and as a UK Biodiversity Indicator (B5a) on pollution pressure.
  - Freshwater exceedances (1752 sites) exist but are not included in the AAE calculation because they are catchment-based, not grid-based.

- Data structure and linking
  - Two separate files: acidhab_AAE_2017-19.csv (acidity) and nutnhab_AAE_2017-19.csv (nutrient nitrogen).
  - Grid reference: 1x1 km squares with an East_m and North_m centre coordinate (OSGB grid, metres).
  - Unique1km: unique identifier for each grid square; allows linking acidity and nitrogen datasets where both have data for the same square.
  - CountryID codes: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.

- Quality control and provenance
  - Values derived from methods agreed at national/international CLRTAP meetings; transparent methods documented in Hall et al. (2015).
  - Metadata and uncertainties described in related documents; CBED deposition data available via EIDC.

- Use and interpretation guidance
  - Exceedance indicates potential for long-term harm under steady-state assumptions; current exceedance does not imply immediate damage.
  - Habitat maps and grid-area calculations may differ from other national habitat maps; total habitat areas used for acidity and nutrient nitrogen may not align perfectly with alternate maps.
  - Recovery from reduced deposition involves chemical and biological time lags; reductions below the critical load do not guarantee rapid ecosystem recovery.
  - Outputs are intended to support data exploration, enable self-serve analyses, and inform discussions on data creation and sharing.

- Access and references
  - Primary references: Hall et al. 2015 (Methods for calculating critical loads and exceedances); Rowe et al. 2019 (Trends Report 2019: Trends in critical load and critical level exceedances).
  - Data and methods tied to UK EIDC resources and CEH metadata.
  - Related summaries and indicators available in the Trends Report and UK Biodiversity Indicator materials.