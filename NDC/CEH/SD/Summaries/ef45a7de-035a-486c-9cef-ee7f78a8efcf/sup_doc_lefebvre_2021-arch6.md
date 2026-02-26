# Supporting Model Documentation Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

## Overview
- Documents a combined Life Cycle Assessment (LCA) and carbon model to assess net greenhouse gas (GHG) balance for reforesting one hectare of goldmining-degraded soil in the Peruvian Amazon.
- Data and methods are described and referenced in the manuscript and its supplementary materials.
- No fieldwork or laboratory data were collected for this model; all inputs come from existing reports and literature.

## Data sources and types
- Data exclusively from existing reports and scientific literature; no new field measurements.
- LCA data: process values and emissions factors for the full supply/processing chain.
- Uncertainty analysis: Monte Carlo approach using distributions fitted to collected data.
- Carbon model components: above- and below-ground tree carbon, biochar degradation, and RothC soil carbon model.
- All data are described and cited in the manuscript or supplementary material; some values obtained via personal communication with team members.

## Modeling design and workflow
- Integrated model: LCA component adds carbon intensity across the process chain; carbon component models tree carbon, biochar degradation, and soil carbon.
- Tree and biochar parts are linear models; RothC uses differential equations.
- Implemented in the R programming language; no model calibration conducted.

## Data inputs and parameters (core data categories)
- Climate and meteorology
  - Table 1: monthly temperature, precipitation, evapotranspiration using ClimWAT/SPEI framework; location: Peruvian Amazon site.
- Soil characteristics
  - Table 2: baseline soil properties and carbon stocks for case plot and reference forest (pH, organic matter, CEC, texture components, bulk density, 0–20 cm carbon stock, etc.).
- Nursery inputs (for 1000 seedlings)
  - Table 3: quantities of semi-carbonized rice husk, sawdust, manures, compost, NPK and other fertilizers, fungicides; nursery electricity cost.
- Carbon modelling data (scenario parameters)
  - Table 4: planting density (1111 seedlings ha-1), biochar yield (30%), soil thickness (20 cm), DPM:RPM ratio, soil/clay content, degraded and adjacent forest soil carbon stocks, litter input dynamics, biochar carbon content and fractions, long-term persistence and loss.
- LCA data (emissions and logistics)
  - Table 5: spatial logistics (distances between biomass collection, biochar plant, reforestation plot, nursery, and boat transport); seedling weight; fuel and emission factors (gasoline, electricity, diesel loading, open dump of husks, etc.); methane, NOx, CO, and N2O factors for pyrolysis; open-dump emissions; nursery transport; electricity for nursery; team composition and labor factors; field work days; input-specific emission coefficients for nursery materials (sawdust, poultry/cow manure, compost, Basacote, Magnocal, DAP, NPK variants, potassium chloride, fungicides).
- Emission factors and literature references
  - Includes values for GWP CH4, N2O, CO, and CO2, plus facilities like RothC references, IPCC guidelines, and supplementary data sources.

## Climate and soil data details
- Climate dataset (Table 1): monthly averages by station; lat/long; temperature, precipitation, evapotranspiration ( Thornthwaite/SPEI methods).
- Soil data (Table 2): case study vs reference forest soil properties, including pH, organic matter, CEC, texture contents, bulk density, and calculated carbon stocks.

## Data structure and management
- Data entered directly into an R model file (.R); no external databases required.
- Quality control involved plotting data and model outputs to assess quality and coherence.

## Analytical methods and uncertainty
- Monte Carlo uncertainty analysis: applies distributions to input data as described in supplementary material.
- LCA calculations include process-level emissions factors and transport distances.
- Carbon modelling uses:
  - Tree carbon and biochar as linear models.
  - RothC soil carbon model using differential equations.
- No new analytical chemistry or field measurements; all analyses are model-based using literature-grounded inputs.

## Outputs and potential data products
- Quantified net GHG balance per hectare for the reforestation scenario.
- Uncertainty ranges derived from Monte Carlo analysis.
- Data and model outputs enable evaluation of carbon sequestration potential and inform decision-making for reforestation projects.

## Data provenance and governance
- All inputs are described and referenced within the manuscript or supplementary material.
- Some key data points (e.g., certain field/mechanical inputs) come from personal communications with project team members.
- Data quality validated through coherence checks and visual plausibility reviews.