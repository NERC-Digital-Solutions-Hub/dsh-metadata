# Supporting Model Documentation Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

## Overview
- A combined Life Cycle Assessment (LCA) and carbon balance model to determine net greenhouse gas (GHG) balance per hectare of reforesting goldmining-degraded soil in the Peruvian Amazon.
- Inputs and uncertainty analysis are described in the manuscript and its supplementary materials.
- Modelling setup uses existing data sources (reports and literature) rather than new field or laboratory data.

## Data Description
- LCA and carbon modelling data are organized into multiple datasets and tables:
  - Climate and soil data (Table 1): monthly meteorological values and derived PET; meteorological station data repeated for modelling; Thornthwaite PET calculated via R package SPEI.
  - Soil characteristics (Table 2): soil pH, organic matter, CEC, texture, bulk density, and initial carbon stocks.
  - Nursery inputs (Table 3): resources required to grow 1000 seedlings.
  - Carbon modelling data (Table 4): planting density, biochar yield/content, soil parameters, litter inputs, and carbon stock parameters used in RothC-like calculations.
  - LCA data (Table 5): life-cycle inputs and emission factors (distances, weights, fuel and electricity factors, manpower, and process emissions) used to compute cradle-to-plot impacts.
- Some inputs are sourced from personal communication (e.g., Jhon Farfan) and are noted as such.
- All data used for modelling and uncertainty analysis are described and referenced in the manuscript or supplementary material.

## Data Sources and Provenance
- Data are exclusively drawn from existing reports and scientific literature.
- Key data sources include climate datasets (ClimWAT), RothC soil carbon modelling references, LCA emission factors (IPCC guidelines, ecoinvent-based inputs), and various literature on tropical forests and biochar.
- Some values are provided via personal communication with project team members, impacting provenance transparency for those inputs.

## Modelling Approach and Data Processing
- The model combines an LCA framework with an above- and below-ground carbon balance, including a biochar degradation model and a RothC-like soil carbon model.
- Uncertainty analysis is performed using Monte Carlo methods with distributions assigned to input data as described in the supplementary material.
- Structural components:
  - Tree carbon and biochar degradation models are linear.
  - RothC soil carbon model uses differential equations.
  - All models are implemented in the R programming environment.
- No fieldwork or laboratory data were used; no model calibration or separate analytical methods were applied beyond the described modelling components.

## Data Structure and Access
- Data are directly entered into the model; the core deliverable is an R script (.R file) rather than a standalone dataset.
- Inputs include a combination of tabulated data (Tables 1–5) and parameters embedded within the code.
- Reproducibility requires access to the model code and the referenced data tables, as well as the manuscript and supplementary materials that describe data sources and methods.

## Data Quality and Validation
- Quality control involved plotting and visual checks to ensure data quality and representativeness.
- Model results were checked for coherence and internal consistency.
- Validation is limited to internal verification; external validation details are not provided in the documentation.

## Governance, Sharing, and Updates
- The documentation presents data inputs as part of a modelling workflow rather than a standalone public dataset.
- Sharing and reuse depend on access to the R model file and the input tables; some inputs rely on non-public sources (personal communications), which may affect reproducibility and metadata completeness.
- Updates would require revising input tables and re-running the Monte Carlo assessments within the same R-based workflow.

## Limitations and Uncertainties
- No field or lab data were used; all inputs are literature-derived or from project communications.
- Meteorological data are assumed to repeat across modelling periods (no new observational time series).
- Uncertainty ranges are embedded for several parameters (e.g., methane, NOx, CO emissions during pyrolysis; various fertiliser and amendment factors), as reflected in Table 5.
- Calibration steps were explicitly noted as absent; the approach relies on literature- and assumption-based inputs.

## Reuse Considerations
- Suitable for researchers needing an integrated LCA and soil carbon balance evaluation in tropical reforestation contexts, provided they have access to the R model and accompanying data tables.
- Users should document input provenance (including any personal communications), maintain consistent software versions, and clearly cite the manuscript and supplementary materials that describe data sources.
- Caution is advised when replicating results due to inputs from non-public sources and the lack of field-based calibration.