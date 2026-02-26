# Supporting Model Documentation Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

- Purpose: Describes a combined Life Cycle Assessment (LCA) and carbon balance model to determine net greenhouse gas (GHG) balance from reforesting one hectare of goldmining-degraded soil in the Peruvian Amazon.
- Modeling approach: 
  - LCA component with process-level emissions factors and a Monte Carlo-based uncertainty analysis.
  - Carbon component including above/below-ground tree carbon, biochar degradation, and soil carbon (RothC) modeling.
  - Tree carbon and biochar models based on literature; RothC uses differential equations; all data referenced in the manuscript or supplementary material.
- Implementation: All models implemented in R; no fieldwork or laboratory data were collected for this model.

## Data sources and provenance

- Data types and origins:
  - Climate and soil data used for modeling (Tables 1 and 2): meteorological values from ClimWAT database; station-specific values and monthly precipitation; soil properties including pH, organic matter, CEC, sand/clay/silt content, bulk density, and initial carbon stock.
  - Additional data for carbon modeling (Table 4) including planting density, biochar yield/content, soil thickness, litter inputs, and various soil/biomass parameters.
  - LCA data and emissions factors (Table 5): distances between production steps, weights, seedling characteristics, GWP factors, emission factors for fuels, electricity, labor, transportation, and inputs for nursery and field operations.
- References and evidence:
  - Data drawn from existing reports and scholarly literature; some values obtained via personal communication (e.g., Jhon Farfan) and are noted as such.
  - Data and uncertainties are described and referenced in the main manuscript or its supplementary material.

## Data processing and modeling methods

- Experimental design: No new sampling or field data collection; the model synthesizes existing data.
- Uncertainty analysis: Monte Carlo approach applied to the data distributions to quantify uncertainty in the LCA and carbon outcomes.
- Modeling components:
  - LCA: process-level emissions and carbon intensity across the supply chain.
  - Carbon model: above/below-ground tree carbon, biochar degradation, and RothC soil carbon dynamics.
- Model specifics:
  - Tree carbon and biochar models are linear.
  - RothC soil carbon model is implemented with differential equations.
- Software and reproducibility:
  - All models are implemented in the R programming environment.
  - Data and methods are documented within the manuscript and supplementary materials to support reproducibility.

## Data structure, storage, and accessibility

- Data organization: Data were directly entered into the model; the core model is an .R file.
- Data tables referenced: Table 1 (climate data), Table 2 (soil characteristics), Table 3 (nursery inputs), Table 4 (carbon modelling data), Table 5 (LCA data and emission factors).
- Accessibility: Information on data provenance and references is provided in the manuscript; some inputs rely on non-public communications (personal contact), which may affect full external accessibility.

## Data quality, validation, and limitations

- Quality control: Data were visually plotted and checked for quality and representativeness; model results were checked for coherence.
- Validation status: No field data collection, no calibration steps, and no separate analytical validation described.
- Assumptions and data gaps:
  - Climate data are repeated/assumed values for modeling.
  - Some soil data contain missing values or are derived from reference values.
  - No calibration performed; reliance on literature-based parameters and assumed conditions.
- Limitations: The approach depends on literature-derived parameters and assumptions, which may introduce uncertainty in real-world applicability.

## Implications for Data Leaders

- Emphasizes the importance of clear data provenance and cited data sources (including supplementary materials and, where applicable, personal communications) for complex, multi-model analyses.
- Demonstrates the need for transparent uncertainty handling (Monte Carlo) in data-driven modeling to support decision-making.
- Highlights the value of reproducible workflows (R-based) and explicit documentation of model structure, data inputs, and assumptions to enable co-ownership and wider system understanding.
- Underlines potential data gaps and accessibility issues (e.g., non-public or communicated inputs) that can hinder timely data availability and standardization across partners.