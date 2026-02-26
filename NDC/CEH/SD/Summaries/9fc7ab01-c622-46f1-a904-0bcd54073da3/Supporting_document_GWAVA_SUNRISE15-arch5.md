# GWAVA Modelling- SUNRISE1.5

- A large-scale hydrological modeling dataset for the Upper Narmada Basin using the GWAVA 5.0 model, producing daily grid-cell outputs of runoff, aquifer level, and various demand components under historical baseline and future climate scenarios.
- Data are organized as 12 CSV files covering baseline history, climate scenarios, and crop substitution scenarios (paddy replacing wheat) across multiple time windows and climate projections.

## Model scope and data governance context

- Model: Global Water Availability Assessment (GWAVA), a semi-distributed gridded water resources model that estimates local runoff per grid cell using a probability-distributed soil moisture storage (PDM) framework, plus surface and groundwater storage components.
- Spatial and temporal resolution: Upper Narmada Basin modeled at 0.125-degree grid; daily timesteps; grid has 318 sub-cells in the upper basin and 653 cells overall in the basin.
- Forcings and demands: Includes anthropogenic stresses via a demand-driven routine (domestic, industrial, agricultural; irrigation is crop-type and planting-month dependent). Domestic and livestock demands are user-defined and static in time, while irrigation demands are dynamic.
- Outputs included: total runoff (totQ), aquifer level (aqlevel), and various demand components (urban/rural/domestic, livestock, industrial, irrigation) plus unfulfilled demand metrics.

## Climate projections and ensemble data

- Climate ensemble: A wide CMIP6-derived set of climate models from multiple modeling centers used to represent future climate for GWAVA runs.
- Model families represented (examples): ACCESS1-0, ACCESS-CM2, ACCESS-ESM1-5, BCC-CSM1-1, BCC-CSM2-MR, CanESM2, CanESM5, CCSM4, CESM1-BGC, CNRM-CM5, CSIRO-Mk3.6.0, EC-Earth3, EC-Earth3-Veg, GFDL-CM3, GFDL-ESM2M, IPSL-CM5A-LR, IPSL-CM5A-MR, MIROC5, MIROC-ESM, MPI-ESM-LR, MPI-ESM-MR, MPI-ESM1-2-HR, NorESM2-LM, NorESM2-MM, INM-CM4-8, INM-CM5-0, MRI-ESM2-0 among others.
- Scenarios and periods: Data include projections under Representative Concentration Pathways (RCP) 4.5 and 8.5, with outputs covering periods such as 2021-2099 and earlier baselines (e.g., 1970-2013, 1981-2013). Specific files document total runoff and aquifer level across these scenarios.

## Quality control and model validation

- Calibration: GWAVA was calibrated at 13 gauging stations using SIMPLEX auto-calibration with four parameters.
- Validation: Performed on the same 13 stations and 100 groundwater wells using an independent time period.
- Performance metric: Kling-Gupta Efficiency (KGE) reported per sub-catchment with values ranging approximately from 0.32 to 0.86, indicating varying multi-site performance across sub-catchments (e.g., high KGE for Manot, Patan, Hoshangabad; lower in some others).
- Implications for stewardship: Transparent calibration/validation metrics support assessment of model reliability across regions; potential data quality issues flagged in accompanying notes (e.g., one file shows an error note).

## Data structure and key files (12 CSVs)

- 1. Narmada_Baseline_1981_2013.csv
  - Baseline daily (1981-2013) grid-cell data.
  - Variables include: xll, yll (grid coordinates); year, timestep (Julian day); totQ; aqlevel; urban_dems; rural_dems; livestock_dems; industrial_dems; irrigation_dems; unfulfilled demand variables (uf_*).

- 2. Narmada_Paddy_1981_2013.csv
  - Baseline daily data for period 1981-2013 with crop-paddy substitution note (similar variables as above).

- 3. Upper_Narmada_Baseline_1970_2013.csv
  - Daily total streamflow (totQ) for the upper Narmada baseline period (1970-2013).

- 4. Upper_Narmada_Climate_2028_2060.csv
  - Daily totQ under future climate scenarios for the upper Narmada (climate-driven total runoff per grid cell).

- 5. Narmada_climate_45_totQ_2021_2099.csv
  - Daily totQ under RCP4.5 for 2021-2099 (multi-model ensemble outputs across grid cells).

- 6. Narmada_climate_85_totQ_2021_2099.csv
  - Daily totQ under RCP8.5 for 2021-2099 (multi-model ensemble outputs across grid cells).

- 7. Narmada_climate_45_aqlevel_2021_2099.csv
  - Daily aquifer level under RCP4.5 for 2021-2099.

- 8. Narmada_climate_85_aqlevel_2021_2099.csv
  - Daily aquifer level under RCP8.5 for 2021-2099.

- 9. Narmada_climate_paddy_45_totQ_2021_2099.csv
  - Total runoff under RCP4.5 for 2021-2099 with wheat-to-paddy substitution.

- 10. Narmada_climate_paddy_85_totQ_2021_2099.csv
  - Total runoff under RCP8.5 for 2021-2099 with wheat-to-paddy substitution.

- 11. Narmada_climate_paddy_45_aqlevel_2021_2099.csv
  - Aquifer level under RCP4.5 for 2021-2099 with wheat-to-paddy substitution.

- 12. Narmada_climate_paddy_85_aqlevel_2021_2099.csv
  - Aquifer level under RCP8.5 for 2021-2099 with wheat-to-paddy substitution.

- Data fields (examples across files): xll, yll, year, timestep; totQ (total runoff, m3/s); aqlevel (aquifer depth, m below ground); urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems; uf_* (unfulfilled demands). The climate-paddy variants introduce scenario-specific totals and aquifer metrics reflecting crop substitutions.

- Data notes: Some entries include missing references or inconsistencies in file naming (e.g., 1.3.2 notes an error reference; 1.3.11/1.3.12 show atypical header formatting), which data stewards should address in curation and metadata.

## Data sharing, updates and governance considerations

- Dataset lifecycle: The model includes a mechanism to respect sharing limitations and supports updates, indicating a governance posture for versioning and provenance.
- Documentation needs: For robust stewardship, ensure a complete metadata record, including model version (GWAVA 5.0), calibration/validation periods, grid definition (0.125-degree), coordinate reference, units, and scenario definitions; capture data lineage from CMIP6 sources to GWAVA outputs.
- Data accessibility: Outputs are organized as CSVs with explicit variable definitions and units; consider publishing to a data portal or catalogue with explicit access rights, licensing, and update schedules.
- Interoperability considerations: The large set of models and multiple scenarios necessitates harmonized metadata and consistent variable naming to ease discoverability and reuse by diverse data users.

## Limitations and caveats

- Some files contain notes indicating missing or inconsistent references (e.g., “Error: Reference source not found” in Paddy baseline file).
- Certain file naming/format entries (especially in the Paddy-related climate files) show formatting irregularities, signaling the need for careful data curation and validation during ingestion and sharing.

## Acknowledgements and provenance

- Acknowledges CMIP6 and the World Climate Research Programme, the ESGF data archive, and supporting funding agencies for model outputs and data distribution.