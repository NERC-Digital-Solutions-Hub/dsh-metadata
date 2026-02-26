# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1

## Overview and purpose
- Dataset provides national estimates of Broad Habitat area change (Habitats 1–17) in Great Britain for 1990–1998–2007, derived using the 2007 ITE Land Classification.
- Outputs are summarized by Land Class and Broad Habitat, with change measured in 000s hectares between two survey years.
- Each row includes the mean change, 95% confidence interval (lower and upper limits), and significance at the 5% level.
- The main file described is CS1990_98_07_Broad_Habitat_Change.csv.
- All use of Countryside Survey (CS) data must be acknowledged.

## Data structure and content
- Columns:
  - YEAR_FROM: Year of the starting survey
  - YEAR_TO: Year of the ending survey
  - LAND_CLASS: ITE Land Class code
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat name (e.g., Broad Habitat 1 = Broadleaved, Mixed and Yew Woodland)
  - MEAN_CHANGE: Mean change in area (000s ha) between the two years
  - LOWER_95PCT_LIMIT: Lower bound of the 95% CI (000s ha)
  - UPPER_95PCT_LIMIT: Upper bound of the 95% CI (000s ha)
  - SIG_5PCT: Significance at 5% level (Yes/No)
- Broad Habitat codes (examples):
  - 1 = Broadleaved, Mixed and Yew Woodland
  - 2 = Coniferous Woodland
  - 3 = Boundary and Linear Features
  - 4 = Arable and Horticulture
  - 5 = Improved Grassland
  - 6 = Neutral Grassland
  - 7 = Calcareous Grassland
  - 8 = Acid Grassland
  - 9 = Bracken
  - 10 = Dwarf Shrub Heath
  - 11 = Fen, Marsh, Swamp
  - 12 = Bog
  - 13 = Standing Open Waters and Canals
  - 14 = Rivers and Streams
  - 15 = Montane (1998–2007 only)
  - 16 = Inland Rock
  - 17 = Urban

## How to use and potential outputs
- Create national- and Land Class–level dashboards or reports showing changes in area by Broad Habitat across the three-time points.
- Enable self-service exploration of which habitat types expanded or contracted between 1990–1998 and 1998–2007, by land class.
- Assess statistical significance of observed changes using the SIG_5PCT flag and accompanying 95% CIs.
- Combine with additional data sources (e.g., local planning, policy contexts) to interpret drivers of change.

## Data quality, methodology, and caveats
- National estimates are derived from the Countryside Survey 1 km square sampling framework and mapped using the ITE Land Classification (2007) with methodology documented in referenced technical reports.
- Uncertainty is provided via 95% confidence intervals for each change estimate.
- Mapping methodology and data provenance are described in multiple references (e.g., Maskell et al., 2008; Barr et al.; Bunce et al.; Scott, 2007).
- The dataset is a product of the Countryside Survey and relies on the 2007 Land Classification; users should consult the cited methodological documents for details on data processing and classification decisions.

## Acknowledgement and licensing
- Acknowledgement required: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Countryside Survey data are ©/NERC-CEH; all rights reserved. Include the standard acknowledgement in publications and outputs.

## References and further reading
- Countryside Survey website and reports (UK 2007) for background, methodologies, and data generation.
- Key methodological and data references:
  - Scott, W.A. (2007) CS Technical Report No. 4/07 (statistical methods for national estimates from 1 km squares)
  - Carey et al. (UK 2007) CS reports and companion technical reports
  - Bunce et al. (ITE Land Classification of GB 2007) and associated datasets
  - Maskell et al. (2008) CS Technical Report No. 1/07 – Field Mapping Handbook
  - Barr, J. (1990s–1998) – Countryside Survey habitat mapping methodologies
  - Jackson, D.L. (2000) – Biodiversity Habitat Classification guidance
- Access to full methodologies and datasets via the Countryside Survey portal and associated publications (e.g., CS_UK_2007_TR1.pdf, CS_UK_2007_TR4.pdf).