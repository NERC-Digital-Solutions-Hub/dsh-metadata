# AAE 2019-2021: Average Accumulated Exceedance (AAE) of acidity and nutrient nitrogen critical loads by acid and nitrogen deposition for 2019-21

## Purpose and scope
- Provides 1x1 km raster datasets of the Average Accumulated Exceedance (AAE) for acidity and for nutrient nitrogen (N) critical loads due to acid and nitrogen deposition for the period 2019–2021.
- AAE summarises exceedances across habitats within each 1x1 km grid cell.

## How AAE is calculated
- For each habitat:
  - Exceedance (keq ha-1 year-1) × exceeded habitat area (ha) = AE (keq year-1).
- AAE = total AE across habitats in a grid cell ÷ total habitat area in that grid cell (ha).
- Units: AAE in keq ha-1 year-1.
- Conversion: for nutrient nitrogen, 1 keq ha-1 year-1 = 14 kg N ha-1 year-1.
- If deposition is below the critical load, AAE is set to zero.
- Acidity AAE combines sulfur (S) and nitrogen (N) deposition; nitrogen alone is not separable in keq units.

## Habitats included
- Acidity (acid_aae_2019-2021.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged coniferous and broadleaved woodland.
- Nutrient nitrogen (nutn_aae_2019-2021.tif): acid grassland, calcareous grassland, dwarf shrub heath, bog, montane, managed productive coniferous woodland, managed productive broadleaved woodland, unmanaged beech/oak/Scots pine woodland, other unmanaged woodland, dune grassland, saltmarsh.

## Data sources and inputs
- Deposition data: CBED (Concentration-Based Estimated Deposition).
- Land cover reference: UK CEH Land Cover Map 2019 1 km summary rasters.
- Habitat distributions and critical loads follow established UK methodologies.

## Calculation and methodology in context
- Based on UK Methods Report (Hall et al., 2015) and related CLRTAP frameworks.
- Critical loads:
  - Acidity: calculated via empirical approach for non-woodland mineral/organomineral soils; simple mass balance (SMB) for woodlands; peat soils use special treatment to reflect buffering and lack of alkalinity from weathering.
  - Freshwaters: FAB catchment-based model used for acidity; not included in the grid-based AAE calculations.
  - Nutrient nitrogen: empirical loads set under the UNECE CLRTAP framework, aligned to EUNIS habitat classes; latest revisions in 2022.
- Exceedances:
  - For acidity, determined by comparing S and N depositions to CLmaxS, CLminN, and CLmaxN; exceedance uses a "shortest distance" method across defined regions of the critical load function.
  - For nutrient nitrogen, exceedance is total N deposition minus the habitat-specific critical load range.
- Data are grid-based (1 km cells) and differ from catchment-based habitat maps; totals may not align with other habitat maps.

## Data structure and format
- Two raster files, each with one band:
  - acid_aae_2019-2021.tif (AAE for acidity, keq ha-1 year-1).
  - nutn_aae_2019-2021.tif (AAE for nutrient nitrogen, keq ha-1 year-1).
- Projection: British National Grid (EPSG:27700).
- Coverage differs between the two files due to habitat distributions.

## Quality, interpretation, and caveats
- Quality control aligned with international conventions (UNECE CLRTAP); detailed methodology documented in Hall et al., 2015.
- Interpretation notes:
  - Exceedance signals potential for harmful effects at long-term or steady-state conditions; not an immediate indicator of current damage.
  - Habitat areas used for AAE calculations may differ from other mapped habitat extents; totals may not be directly comparable across datasets.
  - Recovery from reduced deposition can be slow; chemical and biological recovery timescales may be long, especially for sensitive ecosystems.
- Data limitations:
  - May reflect data availability and habitat mapping constraints; not all UK habitats may be represented equally.

## Appendix and technical details
- Appendix I (Acidity critical loads for woodland): simple mass balance equation using Ca:Al ratio for mineral/organomineral soils; includes terms for weathering, calcium uptake, deposition, and hydrogen ion buffering.
- Notes on units and conversion, enabling translation to kg N ha-1 year-1 for nutrient data where applicable.

## Use and accessibility
- Datasets and their methods support analysis of spatial patterns in exceedances and inform policy decisions on deposition reductions and habitat protection.
- Documentation emphasizes traceability to national/international standards and encourages metadata-based discoverability and reproducibility.