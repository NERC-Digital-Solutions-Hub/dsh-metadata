# Methods: These 1x1 km data sets comprise the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2017-19

## Overview
- Present 1x1 km grid-square AAE values for acidity and nutrient nitrogen critical loads (2017–2019) derived from exceedances above habitat-specific critical loads.
- AAE aggregates exceedances across habitats within each grid square and normalises by total habitat area in the square.

## How AAE is calculated
- For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- Sum AE across all habitats within a 1x1 km grid square.
- AAE (keq ha-1 year-1) = total AE (keq year-1) ÷ total habitat area (ha) in the grid square.
- Acidity AAE expresses in keq ha-1 year-1; nutrient nitrogen AAE can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
- If deposition is below the critical load, AAE is set to zero.
- Acidity AAE reflects combined sulphur and nitrogen deposition; cannot be separated into S or N units.

## Habitats included
- Acidity (a): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
- Nutrient nitrogen (b): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data files and structure
- Files: acidhab_AAE_2017-19.csv (acidity) and nutnhab_AAE_2017-19.csv (nutrient nitrogen).
- Coverage differs by dataset due to habitat distributions.
- Each record includes:
  - East_m: Easting of the grid square centre (OSGB metres)
  - North_m: Northing of the grid square centre (OSGB metres)
  - Unique1km: Unique identifier for the 1x1 km square
  - AAE_keq: Average Accumulated Exceedance (keq ha-1 year-1)
  - CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland
- A linking key (Unique1km) enables joining acidity and nitrogen datasets for squares present in both.

## Units and data interpretation
- AAE_unit: keq ha-1 year-1 for both acidity and nutrient nitrogen (except conversion noted above for nitrogen).
- Conversion: 1 keq ha-1 year-1 = 14 kg N ha-1 year-1 for nutrient nitrogen; acidity values remain in keq ha-1 year-1 and cannot be split into S or N metals.
- Below-CL exceedances are recorded as zero AAE.

## Quality control and provenance
- Methods align with national/international standards developed under the UNECE CLRTAP.
- Detailed methodology report: Hall et al. (2015) Methods for calculation of critical loads and their exceedances in the UK.
- Data provenance and uncertainty information available; see metadata and related literature.
- Additional information on CBED deposition available from EIDC.

## Use and interpretation
- Critical loads maps are based on empirical/steady-state methods; exceedance indicates potential long-term harm, not immediate damage.
- Habitats and their areas used for CL/EX calculations may differ from other national habitat maps, affecting total habitat area sums.
- Reducing deposition below the CL does not guarantee immediate ecological recovery; chemical and biological recovery can involve long time lags.
- Data are intended for discovery, governance, and evidence-based decision-making within datasets where deposition impacts are assessed.

## Data availability, limitations, and governance considerations
- Coverage limited to areas with data available for CL calculations; may not correspond to other habitat distribution maps.
- Updates and maintenance procedures implied by ongoing monitoring programs; check for updated versions to reflect new data.
- Use with accompanying metadata: references, uncertainty notes, and methodological context to support proper interpretation and reuse.

## References
- Rowe, Sawicka, Mitchell, Smith, Dore, Banin & Levy (2019). Trends Report 2019: Trends in critical load and critical level exceedances in the UK. Defra-CEH contract report.
- Hall, Curtis, Dore, Smith (2015). Methods for the calculation of critical loads and their exceedances in the UK. Defra contract report.
- Additional sources: Trends Report updates and EIDC metadata on CBED deposition.