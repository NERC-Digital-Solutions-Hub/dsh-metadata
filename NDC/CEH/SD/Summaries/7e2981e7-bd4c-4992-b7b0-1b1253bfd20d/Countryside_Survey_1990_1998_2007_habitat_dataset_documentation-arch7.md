# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1 Version: 1: 11-11-2014

- Overview
  - National estimates of Broad Habitat change (Habitats 1–17) between year pairs defined by YEAR_FROM and YEAR_TO, calculated using the 2007 ITE Land Classification.
  - Change summarized by Land Class; provides mean change and 95% confidence interval bounds.
  - Significance flag (SIG_5PCT) indicates whether change is significant at the 5% level.
  - Data derived from Countryside Survey UK (CS) data and related methodologies; mapping methodology described in referenced literature.

- Data structure and columns
  - YEAR_FROM (number): start year of survey interval
  - YEAR_TO (number): end year of survey interval
  - LAND_CLASS (number): ITE Land Class identifier
  - BROAD_HABITAT (number): Broad Habitat code (1–17)
  - BROAD_HABITAT_NAME (text): Broad Habitat name
  - MEAN_CHANGE (number): mean change in area for the Broad Habitat (000s ha) between the two years
  - LOWER_95PCT_LIMIT (number): lower bound of 95% CI (000s ha)
  - UPPER_95PCT_LIMIT (number): upper bound of 95% CI (000s ha)
  - SIG_5PCT (text): Yes/No, whether change is significant at 5% level

- Habitat codes and names ( Broad Habitat 1–17)
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

- Coverage, purpose and usage
  - National-level estimates derived from the Countryside Survey, intended for understanding broad habitat change across Great Britain.
  - Useful for GIS mapping of change by Broad Habitat across specified year intervals and for comparing by Land Class.
  - Resolution reflect the CS methodology and 1 km sampling framework; not a high-resolution local dataset.

- Data provenance and methodology
  - Source: Countryside Survey data (NERC – Centre for Ecology & Hydrology)
  - Land Classification system: ITE Land Classification (2007)
  - Methodology and national estimate generation described in CS technical and statistical reports (e.g., Scott 2007; Bunce et al. 2007; Maskell et al. 2008)
  - Mapping methodology and foundational classifications documented in referenced literature and CS reports

- How to use in GIS
  - Join to ITE Land Classification 2007 maps and associated broad habitat layer to visualize spatial patterns of change.
  - Use MEAN_CHANGE for magnitude, and LOWER_95PCT_LIMIT/UPPER_95PCT_LIMIT for uncertainty.
  - Use SIG_5PCT to highlight statistically significant changes.
  - Consider national-scale nature of estimates; validate with local data if applying to fine-scale analyses.

- Acknowledgement and data rights
  - All use of Countryside Survey data must be acknowledged with the following text:
    - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
    - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

- Key references
  - Countryside Survey: UK 2007 reports and datasets (carey et al.; scott 2007)
  - ITE Land Classification of Great Britain 2007 (Bunce et al. 2007)
  - Field mapping and methodology documents (Maskell et al. 2008; Barr 1998; Barr et al. 1990–1998)
  - Guidance on biodiversity/habitat interpretation (Jackson 2000)
  - CS Technical Reports (e.g., CS_UK_2007_TR4.pdf for statistical derivation)