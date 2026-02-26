# Supporting Model Documentation Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

## Overview
- Hybrid modelling approach combining Life Cycle Assessment (LCA) and a carbon balance model to estimate net GHG balance per hectare for reforesting goldmining-degraded soil in the Peruvian Amazon.
- Uses existing data and literature (no new fieldwork) with uncertainty analysis.
- Outputs include above- and below-ground tree carbon, soil carbon (RothC), biochar degradation, and overall net GHG balance per hectare.
- Uncertainty assessed via Monte Carlo; models built in R.

## Modelling Approach
- LCA component with process-level emissions factors along the supply chain; carbon model with tree carbon, biochar degradation, and soil carbon components.
- RothC soil carbon model governs soil carbon dynamics (differential equations).
- Tree and biochar carbon models are linear; RothC is differential.
- Uncertainty relies on distributions applied to input data (as described in supplementary material).
- No model calibration performed.

## Data and Inputs
- Climate data: Table 1 provides latitude/longitude, annual temps, monthly precipitation, and evapotranspiration from ClimWat station near Puerto Maldonado; values assumed repeated across modelling.
- Soil characteristics: Table 2 compares case-study plot and reference forest (pH, organic matter, CEC, sand/clay/silt content, bulk density, and initial carbon stocks).
- Nursery inputs: Table 3 lists inputs for growing 1,000 seedlings (rice husk, sawdust, manures, compost, various fertilizers/fungicides), with nursery electricity and local energy price data.
- Soil carbon modelling data: Table 4 includes planting density (1111 seedlings/ha), biochar yield (30%), soil thickness (20 cm), DPM:RPM ratio (0.25), clay content, initial/adjacent soil carbon stocks, litter input bounds over time, biochar carbon content and fractions, and long-term carbon loss assumptions.
- LCA data: Table 5 enumerates distances (biomass to biochar plant, plant to plot, nursery to plot, boat fuel usage), seedling weight, GWP factors (CH4, NOx, CO, N2O), fossil fuel densities and emission factors, electricity and labour factors, transportation and field operation factors, and emissions associated with biochar production and disposal. References include literature and expert communications (e.g., Jhon Farfan).

## GIS/Spatial Considerations
- Inputs include explicit geographic coordinates and elevation; several distance-based parameters (transportation distances) that can be incorporated into map-based analyses.
- Climate and soil inputs are location-specific (case study plot vs reference forest), enabling spatially explicit mapping of carbon stocks and net GHG balance across potential reforestation sites.

## Uncertainty and Quality Control
- Uncertainty addressed via Monte Carlo distributions for input data.
- No field calibration; data are drawn from published reports and literature, with some author communications.
- Quality control involved plotting data and results to ensure coherence and representativeness.

## Software and Data Structure
- All models implemented in the R programming language.
- Data were directly entered into the model; the model itself is an .R file.
- Outputs are suitable for integration into GIS workflows for spatial visualization and decision support.

## Outputs and Applications
- Net greenhouse gas balance per hectare of reforested land, with decomposition of contributions from tree carbon, soil carbon (RothC), and biochar effects.
- Potential for map-based visualization of spatial variability in carbon sequestration potential to inform site prioritization and policy discussions.

## Limitations and Considerations
- No experimental design or field sampling; relies entirely on existing data and literature.
- Calibration and field validation are not part of the model.
- Some inputs use personal communications and assumed constants (e.g., climate repetition), which may affect spatial transferability.