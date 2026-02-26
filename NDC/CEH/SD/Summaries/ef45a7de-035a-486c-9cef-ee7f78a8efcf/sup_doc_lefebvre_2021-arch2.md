# Assessing the carbon capture potential of a reforestation project - DOI 10.1038/s41598-021-99395-6 Lefebvre et al. 2021

## Overview
- A combined Life Cycle Assessment (LCA) and carbon balance model to determine the net greenhouse gas (GHG) balance of reforesting one hectare of goldmining-degraded soil in the Peruvian Amazon.
- Uses data and methods described in Lefebvre et al. (2021) to estimate net GHG balance and carbon capture potential.
- Includes an uncertainty analysis (Monte Carlo) and focuses on both above- and below-ground carbon pathways, biochar degradation, and soil carbon dynamics (RothC).
- All inputs are drawn from existing reports and scientific literature; models are implemented in R; no field data were collected for this modelling.

## Modelling approach and components
- LCA component
  - Contains process values and emission factors for the full supply chain (biomass collection, biochar production, nursery operations, transportation, energy use, open waste handling, etc.).
  - Emissions factors cover CH4, NOx, CO, CO2, N2O, electricity, fuels, labor, and transportation.
  - Distances between stages (biomass collection → biochar plant, plant → plot, nursery → plot) are specified; data sources include personal communications and literature; some factors derived from ecoinvent and other databases.
  - Incorporates an uncertainty analysis via Monte Carlo sampling; results are produced without field measurements.
- Carbon model
  - Includes an above- and below-ground tree carbon model, a biochar degradation model, and a RothC soil carbon model.
  - Tree carbon and biochar degradation models are linear; RothC uses differential equations for soil carbon turnover.
  - Biochar characteristics: carbon content ~87.6%, with 5% labile and 95% recalcitrant fractions; C losses and litter dynamics modeled over time.
  - Time horizon and interactions with soil, litter input, and biochar amendments feed into net GHG balance estimation.
- Data integration
  - LCA results inform the carbon balance components; output is a net GHG balance per hectare for the reforestation scenario.

## Data inputs and sources
- Climate and soil data
  - Climate: ClimWAT/meteorological data (monthly averages, station metadata), with Thornthwaite PET calculated via R (SPEI package).
  - Soil characteristics: case study plot vs reference forest (pH, organic matter, CEC, sand/clay/silt fractions, bulk density, carbon stock).
  - Meteorological assumptions: values assumed to be recurring for modelling runs.
- Nursery and field data
  - Nursery inputs for 1,000 seedlings (semi-carbonized rice husk, sawdust, manures, compost, NPK/fertilizers, fungicides, etc.).
  - Nursery electricity and cost data (historical price references).
- Carbon modelling data (Table 4)
  - Planting density: 1111 seedlings ha−1.
  - Biochar yield and carbon content; litter inputs; soil thickness; DPM:RPM ratio; soil carbon stock and litter dynamics.
  - Biochar properties: labile vs recalcitrant fractions; carbon losses over 100 years.
  - Reference values for adjacent forest soil carbon stock and old-growth forest benchmarks.
- LCA data (Table 5)
  - Distances among stages (biomass → biochar plant, biochar plant → plot, nursery → plot), fuel and electricity factors, weights of seedlings, equipment and labor factors, and emission factors for fuels, electricity, transportation, and nursery activities.
  - Pyrolysis emissions (CH4, NOx, CO) with uncertainty ranges; emissions associated with open-dump waste.
  - Inputs for materials (fertilizers, amendments, pesticides), with kg CO2-e per unit for each input.
- References and data provenance
  - Data described or referenced in the manuscript and supplementary materials; several inputs cited as personal communications from project team members.

## Uncertainty, calibration, and analytical methods
- Uncertainty analysis
  - Monte Carlo method applied to collected data to quantify the uncertainty in the LCA and carbon balance outputs.
  - Distributions and ranges are described in the supplementary material.
- Calibration and measurements
  - No field data were collected for this model; no calibration steps were applied.
  - No separate analytical methods beyond those embedded in the LCA and RothC modelling approaches.
- Modelling environment
  - All models implemented in the R programming language; components are linear (tree carbon, biochar) or differential (RothC).

## Implementation and data structure
- Model implementation
  - The modelling work is described as an integrated LCA plus carbon dynamics framework; all inputs are assembled from existing sources and embedded into the model.
- Data structure
  - Data were directly entered into the model; the model itself is an .R file.
  - Outputs are designed to express net GHG balance per hectare, along with uncertainty estimates.

## Quality control and data accessibility
- Quality control
  - Data were visually plotted and checked for representativeness and coherence of results.
- Accessibility and reuse
  - Inputs are thoroughly referenced in the manuscript and supplementary materials.
  - The document emphasizes standardised data inputs and the potential for integration with other datasets, highlighting opportunities for broader data sharing and portal integration to enhance data accessibility.

## Relevance to environmental monitoring and policy assessment
- Standardised, data-driven approach
  - Demonstrates how to quantify environmental health and policy performance (GHG balance of reforestation) in a consistent, transparent format.
- Uncertainty quantification
  - Provides a framework to propagate input uncertainties through to final net GHG balance, aiding risk assessment and decision making.
- Data integration potential
  - The structured data inputs (climate, soils, nursery activities, LCA factors, and carbon dynamics) are suitable for coupling with other environmental datasets and monitoring systems.
- Practical considerations for monitoring
  - Highlights the need for accessible underlying data and model transparency to enable replication, validation, and longitudinal monitoring of policy-driven restoration projects.