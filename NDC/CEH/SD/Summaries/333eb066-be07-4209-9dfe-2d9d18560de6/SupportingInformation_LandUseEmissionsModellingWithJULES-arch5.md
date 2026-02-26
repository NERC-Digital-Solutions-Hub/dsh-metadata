# Background, Experiment Design and Analytical Methods

- Purpose: Document the dataset used in Harper et al. (2018) that investigates carbon cycle implications of land-use change for Paris climate targets, using two BECCS/forest scenarios and climate-driven pathways to assess land-based mitigation.

- modeling chain:
  - JULES (Joint UK Land Environment Simulator) v4.8 for large-scale land-surface processes, with multi-layer soil carbon.
  - IMOGEN climate–carbon emulator to pattern-scale CMIP5 GCMs (34 models) onto a prescribed temperature pathway.
  - Outputs designed to understand land-based climate mitigation under specified warming targets.

- Experimental design:
  - Factorial setup with three temperature pathways and four model configurations, yielding 12 simulations (reported in six directory structures representing combinations of warming pathway and land-use scenario):
    - Temperature pathways: 1.5°C, 2°C, and 2°C with CO2 from the 1.5°C pathway (to isolate climate vs CO2 fertilization effects).
    - Land-use scenarios: IM19 (IMAGE SSP2-SPA0-RCP1.9) and IM26 (IMAGE SSP2-SPA2-RCP2.6).
  - Directory examples include 1p5deg_IM19, 1p5deg_IM26, 2deg_IM19, 2deg_IM26, 2deg_IM19_1p5CO2, 2deg_IM26_1p5CO2.

- Data provisioning and scope:
  - Available outputs cover 2000–2099; historical/earlier periods (1850–1999) exist in a linked dataset (Harper/Comyn-Platt, 2018) for context.
  - Related data and model inputs are stored in dedicated datasets and linked via DOIs.

## Data Structure and Variables

- Main file types (NetCDF, self-describing):
  - CarbonStocks: gridbox-level vegetation carbon (cv), soil carbon (cs_gb), fractional cover (frac), net primary productivity (npp), harvest, BECCS pool (ccs_gb), crop fractions (Frac_agr, Frac_biocrop), pasture, wood products, and CO2 concentration (co2_ppmv).
  - WaterCycle: soil temperature (t_soil), soil moisture (smcl), soil moisture fraction (Swet_tot), moisture flux (Fqw_gb), sensible heat flux (Ftl_gb), wetlands fraction (fwetl), runoff, water table depth (zw).
  - Ancillary files: initial/boundary conditions, grid definitions, CO2 concentrations, non-CO2 radiative forcing, and land-cover datasets for IM1.9/IM2.6 scenarios.
- Time and space:
  - Variables with time, latitude, longitude dimensions (and additional dimensions for PFTs where applicable).
  - 2000–2099 data in CarbonStocks and WaterCycle; 1850–1999 data stored in linked dataset.
- Variable details:
  - Examples include cv (gridbox total vegetation carbon, kg m-2), cs_gb (gridbox soil carbon, kg m-2), npp (kg m-2 s-1), ccs_gb (BECCS pool carbon, kg m-2), co2_ppmv (ppmv), t_soil (K), Fqw_gb (kg m-2 s-1), and others.
- NPP and tile-based calculations:
  - Grid boxes comprise 17 tiles (13 plant types and 4 non-veg tiles); NPP per PFT must be weighted by frac to obtain grid-box totals.

## Metadata, Provenance, Documentation

- Provenance and lineage:
  - Main reference: Harper et al. (2018) Nature Communications; data cited in data papers by Harper et al. and Comyn-Platt et al. (2018).
  - IMOGEN and JULES model versions and associated literature cited for context (Huntingford, Cox; Harper et al.; Taylor et al.).
- File naming and organization:
  - NetCDF files named BL_CEN_<centre>_MOD_<model>_<scenario>.CarbonStocks.2000-2099.nc and .WaterCycle.2000-2099.nc.
  - Scenarios identified as 2deg, 1p5deg, and 2deg_IM19/IM26 with potential 1.5CO2 adjustments.
  - Directory structure mirrors the land-use and CO2 experiments.
- Documentation and references:
  - Appendix includes table of climate modelling centres and GCM names used by IMOGEN (CMIP5 centers and models).
  - Extensive notes on data structure, variable definitions, and interpretation (including NPP calculation guidance).

## Access, Reuse and Reproducibility

- Data accessibility:
  - NetCDF files are readable with standard tools (R, Python, nco, etc.).
  - Linked datasets and DOIs provided for CMIP5 GCM outputs and historical data (EIDC DOIs provided).
  - Appendix and rose-suites list offer reproducibility resources; rose suites are available via the Met Office code portal (registration required).
- Reproducibility considerations:
  - Ancillary files enable replication of the JULES-IMOGEN experiments (grid, initial CO2, prescribed CO2 for special experiments, non-CO2 forcing inputs, land-cover initializations).
  - Explicit guidance on calculating grid-box totals from tile-level outputs (NPP and other variables).

## Related Resources and Appendices

- Linked datasets and DOIs:
  - CMIP5 GCM outputs used by IMOGEN stored at EIDC (doi provided).
  - Outputs from 1850–2000 available via linked dataset (doi provided).
- Appendix content:
  - List of rose suites for IM1.9 and IM2.6 experiments (registration required).
  - Comprehensive table of CMIP5 centres and corresponding GCM names used in IMOGEN (matches CMIP5 portal nomenclature).

## Data Stewardship Considerations

- Data complexity and interoperability:
  - Large, multi-model, multi-scenario dataset with multiple systems/formats; ensure consistent metadata, versioning, and provenance tracking.
- Metadata and metadata quality:
  - Given the detailed variable definitions and calculation notes (e.g., NPP weighting by frac), maintain explicit guidance within metadata to support correct use.
- Access and updates:
  - Provide stable DOIs for linked datasets; ensure ancillary files remain accessible to enable reproduction.
- Governance and governance-readiness:
  - Dataset aligns with established Earth system modeling workflows; ensure ongoing clarity of model versions, scenario definitions, and directory mappings for future users.