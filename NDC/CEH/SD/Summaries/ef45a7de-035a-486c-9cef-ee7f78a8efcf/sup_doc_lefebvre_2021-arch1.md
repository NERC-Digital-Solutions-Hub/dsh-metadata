# Supporting Model Documentation Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

## Overview
- A combined Life Cycle Assessment (LCA) model and carbon balance model to determine the net greenhouse gas (GHG) balance of reforesting one hectare of goldmining-degraded soil in the Peruvian Amazon.
- Based on Lefebvre et al. (2021) Scientific Reports; uses data described in the manuscript and supplementary material.
- LCA component includes process values and emissions factors; uncertainty analyzed via Monte Carlo methods.
- Carbon component includes an above- and below-ground tree carbon model, a biochar degradation model, and a RothC soil carbon model.

## Modelling approach and components
- LCA model: incorporates emissions factors for each process; uncertainty through Monte Carlo distributions applied to collected data.
- Carbon model: 
  - Tree carbon: above- and below-ground stocks from literature.
  - Biochar: degradation dynamics.
  - Soil carbon: RothC model (differential equations) used to simulate soil carbon changes.
- All models implemented in the R programming language.
- Data and uncertainty analyses are described and referenced in the manuscript or supplementary material.

## Experimental design and data collection
- No fieldwork or laboratory measurements were conducted for this model.
- Exclusively uses data available in existing reports and scientific literature.
- No calibration steps were reported.
- Analytical methods are not described as standalone procedures beyond the Monte Carlo uncertainty framework.

## Data sources, structure, and workflow
- Data are described in the manuscript and supplementary material; all data used are from published sources or direct communications with project contributors.
- The modelling workflow combines LCA data (emissions factors, process distances, energy use) with carbon modelling inputs (planting densities, litter inputs, biochar properties, soil parameters).
- Data structure: input data were directly entered into the model; the model itself is an .R file.

## Climate and soil data
- Table 1 provides climate data by month from ClimWAT for a meteorological station (Madre de Dios region, Peru): latitude, longitude, mean monthly temperatures, precipitation, and evapotranspiration; values assumed constant across modelling runs.
- Thornthwaite evapotranspiration calculated via R package SPEI.
- Table 2 lists soil characteristics for the case study plot and reference forest (pH, organic matter, CEC, sand/clay/silt content, bulk density, and soil carbon stocks).

## Soil carbon modelling data
- Table 4 provides inputs for the RothC-based carbon modelling:
  - Planting density (seedlings per ha), biochar yield, soil thickness, DPM:RPM ratio, clay content, degraded and adjacent forest soil carbon stocks, litter input ranges, biochar carbon content and fraction (labile vs recalcitrant), and long-term carbon loss from biochar.
  - Additional parameters include median tree density in old-growth tropical forest and various biochar-related assumptions.
- These values feed the RothC model and the biochar degradation framework used in the carbon balance calculation.

## LCA data and parameters
- Table 5 lists emission factors and data inputs for the LCA:
  - Distances: biomass collection to biochar plant; biochar plant to plot; nursery to plot; boat fuel to plot; seedling weight.
  - GHG factors for multiple inputs: CH4, NOx, CO, N2O, CO2 from various activities (fuel use, electricity, human labour, transportation, open waste of residues, loading operations).
  - Pyrolysis emissions: methane, nitrogen oxides, carbon monoxide from biochar production.
  - Nursery and field-work inputs: electricity for nursery, team size and weight, and days required for field work.
  - Fertilizers and amendments: various fertilizers and pesticides with emissions factors.
  - Open-source references include IPCC guidelines, RothC documentation, literature on biochar and tropical forests, and personal communications from project contributors.
- Notable values include GWP factors (e.g., CH4, N2O, CO) and energy/carbon intensities for equipment, transport, and processing.

## Quality control and reproducibility
- Data were visually inspected and plotted to assess quality and representativeness.
- Model results were checked for coherence with input data and expected trends.

## Data structure and miscellaneous
- All data were entered directly into the model; the model is implemented as an R script.
- The documentation references supplementary material for distributions and Monte Carlo implementation.