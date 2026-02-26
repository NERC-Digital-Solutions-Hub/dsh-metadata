# Supporting Model Documentation Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

## Overview
- A combined Life Cycle Assessment (LCA) and carbon balance model to determine the net greenhouse gas (GHG) balance of reforesting one hectare of goldmining-degraded soil in the Peruvian Amazon.
- Integrates process-level emissions, above-/below-ground tree carbon, biochar degradation, and soil carbon dynamics (RothC) to evaluate carbon capture potential.

## Modelling components
- LCA model: processes and emission factors across the production-to-planting chain; supports calculation of overall carbon intensity of the reforestation activity.
- Carbon model: includes an above- and below-ground tree carbon model, a biochar degradation model, and a RothC-based soil carbon model.
- Uncertainty analysis: Monte Carlo method applied to propagate data and parameter uncertainties; distributions described in supplementary material.
- Implementation: all models implemented in R; tree carbon and biochar models are linear; RothC uses differential equations.
- Data provenance: all data used for modelling are described and referenced in the manuscript or its supplementary material.

## Experimental design and data sources
- Experimental design/sampling: The modelling study does not involve new field sampling; it relies on data from existing reports and scientific literature.
- Calibration: No calibration of the models reported.
- Analytical methods: No separate analytical method beyond modelling framework described.
- Fieldwork and laboratory data: None; no new field measurements.

## Data inputs and structure

- Climate and meteorology (Table 1)
  - Location details, latitude/longitude, yearly average temperature, and monthly precipitation from ClimWAT; values assumed constant for modelling.
  - Thornthwaite PET calculated using the R package SPEI.
- Soil characteristics (Table 2)
  - Case study plot and reference forest: pH, organic matter, CEC, sand/clay/silt, bulk density, and initial carbon stock (0–20 cm); several fields provided as calculated or placeholder values.
- Nursery inputs (Table 3)
  - Elements required to grow 1,000 seedlings (e.g., semi-carbonized rice husk, sawdust, manure, compost, various fertilizers, fungicides); electricity cost for nursery reported.
- Soil carbon modelling data (Table 4)
  - Planting density, biochar yield, soil thickness, litter input ranges, carbon content and fractions of biochar (labile vs recalcitrant), RothC-related parameters, soil carbon stocks (degraded vs adjacent forest), litter turnover times, and related references.
- LCA data (Table 5)
  - Distances between biomass collection, biochar plant, reforestation plot, and nursery; seedling weight; fuel and electricity emission factors; human labour and transportation factors; process-specific emissions (e.g., biochar pyrolysis methane, NOx, CO factors with specified uncertainties); transportation and field-work days; weights and unit conversions; data sources include literature and personal communications (e.g., Jhon Farfan).
- Data provenance and references
  - Many parameters sourced from peer-reviewed literature; several values obtained via personal communication; all data are described and referenced in the manuscript or supplementary material.

## Modelling details and data processing

- Data usage
  - exclusively uses data from existing reports and scientific literature; no new field data were collected.
- Process integration
  - LCA provides carbon intensity for the process chain; carbon model provides carbon stocks and turnover (tree and soil dynamics, including biochar effects).
- Uncertainty
  - Monte Carlo analysis with distributions described in the supplementary material; accounts for variability in key inputs (e.g., biochar effects, emission factors).
- Modelling specifics
  - Tree carbon and biochar degradation models: linear relationships.
  - Soil carbon model: RothC, solved via differential equations.
  - Software environment: R.
  - Data inputs are directly entered into the model; the model itself is an .R file.

## Quality control and data governance

- Quality assurance
  - Data plotted and visually checked for quality and representativeness; model results checked for coherence.
- Data structure and documentation
  - Data are directly entered into the model; documentation and references provided; supplementary material includes modelling details.
- Data openness and governance considerations
  - Some data rely on personal communications and may limit public sharing; authors note that all data used are described or referenced in the manuscript or supplementary material.
- Reproducibility
  - Complete modelling workflow implemented in R with documented inputs; references and sources are cited to support traceability.

## Limitations and considerations

- No field validation or calibration reported.
- Several inputs depend on literature values or author communications; certain pH and other micro-parameters are partially incomplete in the tables.
- Some emission factors (e.g., pyrolysis-related CH4, NOx, CO) include large uncertainty ranges.
- Public accessibility of all underlying data may be constrained by data provenance sources (e.g., personal communications).

## Implications for monitoring frameworks

- Emphasizes the value of integrating LCA with biophysical carbon models (forest carbon, soil carbon, and biochar dynamics) for policy evaluation and decision-making.
- Demonstrates robust uncertainty quantification (Monte Carlo) as a core component of evaluating net GHG balance.
- Highlights data governance considerations relevant to monitoring: transparent data provenance, detailed metadata, linkage to supplementary materials, and explicit notes on data accessibility and potential sharing barriers.
- Underlines the importance of clear documentation and reproducible code (R-based model) to enable scrutiny, replication, and iteration in monitoring frameworks.