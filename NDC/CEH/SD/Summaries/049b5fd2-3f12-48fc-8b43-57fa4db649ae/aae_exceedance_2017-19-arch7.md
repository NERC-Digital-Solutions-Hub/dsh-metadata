# 1x1 km data sets comprising the Average Accumulated Exceedance (AAE) of acidity and of nutrient nitrogen critical loads by acid and nitrogen deposition for 2017-19

## Overview
- AAE summarizes exceedances across multiple habitats within each 1x1 km grid square.
- Two datasets: AAE for acidity and AAE for nutrient nitrogen, covering 2017–2019.
- Values are in keq per hectare per year (keq ha-1 year-1); zero when deposition is below the critical load.

## How AAE is calculated (method)
- For each habitat: AE (keq year-1) = exceedance (keq ha-1 year-1) × exceeded habitat area (ha).
- Sum AE across all habitats within a 1x1 km grid square.
- AAE = total AE / total habitat area in the grid square.

## Habitats included
- Acidity AAE habitats: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous woodland, unmanaged broadleaved woodland.
- Nutrient nitrogen AAE habitats: acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech woodland, unmanaged oak woodland, unmanaged Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data structure and fields
- Two files: acidhab_AAE_2017-19.csv (acidity) and nutnhab_AAE_2017-19.csv (nutrient nitrogen).
- Common grid linkage: Unique1km (unique 1x1 km grid square identifier) to connect acidity and nitrogen data where applicable.
- Spatial identifiers: East_m (centre Easting, OSGB grid), North_m (centre Northing, OSGB grid).
- CountryID: 1=England, 2=Wales, 3=Scotland, 4=Northern Ireland.
- AAE_keq: Average Accumulated Exceedance value for the square (keq ha-1 year-1).

## Coverage and interpretation
- UK-wide data with different coverage for acidity vs. nitrogen due to habitat distributions.
- Freshwater data (1752 sites) are not included in AAE calculations because they are catchment-based, not 1x1 km grid-based, and do not represent all UK freshwaters.
- Critical loads exceedance indicates potential long-term harm under steady-state assumptions; does not imply immediate damage or rapid recovery.

## Units, conversions, and caveats
- Acidity AAE: keq ha-1 year-1 (cannot be converted to kg of S or N).
- Nutrient nitrogen AAE: keq ha-1 year-1; can be converted to kg N ha-1 year-1 by multiplying by 14 (1 keq ha-1 year-1 = 14 kg N ha-1 year-1).
- Reducing deposition below the critical load does not guarantee immediate ecosystem recovery due to chemical and biological time lags.

## Quality control and provenance
- Methods aligned with UNECE CLRTAP (Long-Range Transboundary Air Pollution) standards.
- Detailed transparency on methods and data available (Hall et al., 2015).
- Related usage references include Trends Report (Rowe et al., 2019) and reviews of UK critical loads (Hall et al., 2015).

## Use in GIS and mapping
- Suitable for map-based visualization of spatial exceedance patterns at 1x1 km scale.
- The two datasets can be linked via Unique1km to compare acidity and nutrient nitrogen exceedances in the same grid squares.
- Notes when using maps: habitat maps and areas used for CL calculations may differ from other national habitat maps; ensure alignment with the appropriate UK habitat and deposition datasets.

## Fieldwork and calibration
- Fieldwork/instrumentation: Not applicable (N/A).
- Calibration steps/values: N/A.

## References
- Hall, J., Curtis, C., Dore, T., Smith, R. (2015). Methods for the calculation of critical loads and their exceedances in the UK.
- Rowe E, Sawicka K, Mitchell Z, Smith R, Dore T, Banin LF & Levy P (2019). Trends Report 2019: Trends in critical load and critical level exceedances in the UK.