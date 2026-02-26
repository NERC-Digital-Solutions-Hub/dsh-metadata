# General description

- Global dataset of soil organic carbon (SOC) changes on agricultural land under different land-use and climate scenarios up to 2100.
- SOC changes are given as Mg C ha-1 yr-1 differences relative to a baseline business-as-usual (BAU) scenario with continuous tillage, no residue incorporation, and no organic amendments; annual averages over 2020–2100, presented for decadal periods (2020–2030, 2030–2040, ..., 2090–2100).
- Modeling approach: spatial ECOSSE model (version 6.2b) run monthly on a 0.5-degree grid; inputs include crop yields (wheat), fertiliser inputs, sowing/harvest dates, and soil management (tillage, residue management).
- Outputs are SOC_CH values (SOC_BAU minus SOC_SC) and are processed in R (v4.3.0); results are mapped and QA’d against literature to ensure plausibility.

## Data structure and files

- File naming pattern reflects management change and climate scenario (e.g., crop_notill_A1B.txt, crop_residincorp_A2.txt, crop_covercrop_residincorp_redtill_A1B.txt, crop_manure_A1B.txt, etc.).
- Table 2-type metadata included in each file:
  - Latitude, longitude
  - area_km2 (grid cell size)
  - LU_agr_nrs_grid_cell (agricultural land-use per grid cell)
  - SOC_20_30_MgC_ha_yr … SOC_90_100_MgC_ha_yr (SOC change per decadal interval; all in Mg C ha-1 yr-1, presented as difference to BAU)
- Each file describes the corresponding management change and climate scenario (A1B or A2).

## Modeling details

- ECOSSE model applied to each grid cell with site-specific inputs; runs until 2100.
- Grid-cell inputs include climate, soil (HWSD), land use (Hilda map), fertiliser inputs, wheat yield, sowing/harvest dates, and tillage/residue practices.
- Outputs are annual SOC totals in kg C yr-1; SOC_CH is calculated as SOC_BAU minus SOC_SC.
- 10-year period averages are reported for SOC_CH.
- Global and regional statistics and visual checks are performed for consistency with existing literature.

## Data inputs and provenance

- Climate data: Climate Research Unit, University of East Anglia (UEA CRU).
- Soil data: Harmonized World Soil Database (HWSD).
- Land use data: Hilda land use map (2019; cropland grid 0.01°).
- Fertiliser inputs: Pangaea dataset.
- Wheat yield: FAOSTAT (national/region-level data).
- Sowing/harvest dates: LUH dataset.
- Related references and datasets for manure application and supplementary materials provided (e.g., Gerber et al. 2016; Smith et al. 2010a,b).

## Data quality, governance, and reproducibility

- Quality assurance: model outputs mapped and visually screened; statistics computed to compare with literature to ensure results are within expected ranges.
- Provenance: explicit model version (ECOSSE 6.2b) and software used (R v4.3.0) with grid-cell-specific inputs; clear documentation of BAU baseline and management scenarios.
- Metadata coverage: grid geometry (latitude/longitude/area), land-use context, and decadal SOC change variables enable discoverability and reuse.
- Reproducibility considerations: description includes input data sources, model configuration, and processing steps; to reproduce, one would need ECOSSE, the same input datasets, and the R processing workflow.

## Data access and use considerations for Data Stewards

- Data transparency: detailed documentation of scenarios, BAU baseline, and management changes supports governance and auditing.
- Interoperability: 0.5° grid and standardized SOC change fields support integration with other regional/global datasets.
- Licensing and source data: relies on publicly available datasets (CRU, HWSD, Hilda, FAOSTAT, LUH, Pangaea); downstream reuse should reference these sources where applicable.
- Update and maintenance: dataset describes a fixed modeling run to 2100; future updates would require re-running ECOSSE with revised inputs or scenarios.

## Limitations and caveats

- BAU definition relies on continual tillage, no residue incorporation, and no organic amendments; results are contingent on this baseline.
- Climate scenarios are A1B and A2 (IPCC-SRES), which may differ from newer CMIP6 scenarios; users should consider scenario relevance.
- Spatial resolution fixed at 0.5° grid; localized variability may be underrepresented.
- Decadal averages smooth year-to-year variability; interpretation focuses on long-term trends rather than annual fluctuations.

## References

- Gerber JS, Carlson KM, Makowski D, Mueller ND, Garcia de Cortazar-Atauri I, Havlík P, et al. (2016) Spatially explicit estimates of N2O emissions from croplands; Global Change Biology.
- Smith J, Gottschalk P, Bellarby J, Chapman S, Lilly A, Towers W, et al. (2010a) Estimating changes in Scottish soil carbon stocks using ECOSSE. Clim Research.
- Smith J, Gottschalk P, Bellarby J, Chapman S, Lilly A, Towers W, et al. (2010b) Estimating changes in Scottish soil carbon stocks using ECOSSE. Clim Research.