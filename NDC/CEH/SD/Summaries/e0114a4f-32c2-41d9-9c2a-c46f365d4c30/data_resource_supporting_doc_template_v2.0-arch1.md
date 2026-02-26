# Emissions of Ammonia (NH 3 ) from Agriculture in South Asia in 2015

- Purpose: Provides gridded, annual NH3 emissions from agricultural sources in SAARC for 2015, at 0.1° x 0.1° resolution, masked to Afghanistan, Bangladesh, Bhutan, India, Maldives, Nepal, Pakistan and Sri Lanka.
- Scope: Bottom-up emissions by five agricultural sub-sectors to better represent South Asia with region-specific data.

## Data content

- Five GeoTIFF rasters representing NH3 emissions by sub-sector:
  - NH3_CRB_SouthAsia_2015_gm2_0.1.tif — crop residue burning
  - NH3_CRR_SouthAsia_2015_gm2_0.1.tif — crop residues left in fields
  - NH3_GRM_SouthAsia_2015_gm2_0.1.tif — livestock grazing and manure applications
  - NH3_MNM_SouthAsia_2015_gm2_0.1.tif — livestock management (housing, storage, slurries)
  - NH3_SFA_SouthAsia_2015_gm2_0.1.tif — synthetic fertiliser applications
- Units: grams of NH3 flux per square metre per year (g m^-2 yr^-1); NA for missing data.

## Spatial and temporal coverage

- Spatial: SAARC domain with coordinates xmin 60.5° to xmax 97.4°, ymin -0.7° to ymax 38.5°, using WGS84; 0.1° resolution; cells outside the eight countries set to NA.
- Temporal: Annual emissions for the year 2015.
- Production timeline: Datasets produced during 2022–2023; designed to reflect 2015 conditions.

## Methods and data sources

- Methodology framework: Bottom-up emissions following EDGARv6.1, IPCC 2006 Guidelines, IPCC 2019 Refinement, and EMEP/EEA guidebooks (2019, 2023), incorporating region-specific information.
- Sector-specific approaches:
  - CRB (crop residue burning): fraction burnt by crop per country; India-specific crop sets; emission factor (EF) is the mean of seven modified combustion efficiency values.
  - CRR (crop residues in-field): fraction left in field; EF determined by EEA Guidebook (2023) depending on crop material N content.
  - GRM (grazing/manure management) and MNM (housing, storage, slurry, yarding): nitrogen-flow approach; N excretion rates by livestock type; losses by management stage; surfaces distributed country-livestock-type.
  - SFA (synthetic fertilisers): total N fertiliser use by type and country; spatially distributed total N application; split into fertiliser types; NH3 emissions via EF by fertiliser type and field pH; Urea EF updated.
- Data integration: Uses country/region data (e.g., fertiliser use, livestock populations, crop areas) to produce spatially explicit NH3 surfaces reweighted to FAOSTAT totals and EarthStat crop surfaces.

## Input data and validation

- Key inputs include: crop distributions (EarthStat), FAOSTAT crop production and fertiliser data, country- and state-level crop area/yield data, crop residue parameters, fertiliser N content, livestock parameters, and soil pH (topsoil data), among others.
- Quality control: checks for extreme values and NA positions; totals checked against non-spatial calculations; cross-validation against other NH3 emission estimates.

## File format and naming conventions

- Format: GeoTIFF raster files.
- Naming conventions: sector-specific NH3_SouthAsia_2015_gm2_0.1.tif files as listed above.
- Spatial unit and metadata: cells represent g NH3 m^-2 yr^-1; NA values indicate missing data.

## Considerations for analysts

- Use cases: regional NH3 inventories, sectoral attribution, model validation, and policy-relevant emissions mapping in South Asia.
- Strengths: regionally tailored inputs, alignment with international inventory methodologies, and sub-sector granularity.
- Limitations and uncertainties:
  - Dependence on literature-based emission factors and regional data quality; potential uncertainties in crop burning fractions, EF selections, and N-content assumptions.
  - Data represent 2015 and were produced in 2022–2023, so users should consider temporal mismatches with other datasets.
  - Boundary definitions and NA areas may affect comparability with administrative or different geographic delineations.

## References and methodological underpinning

- Extensive references to EDGARv6.1, IPCC guidelines (2006, 2019), EMEP/EEA guidebooks (2019, 2023), FAOSTAT, EarthStat, and a broad set of crop, fertiliser, and livestock data sources.