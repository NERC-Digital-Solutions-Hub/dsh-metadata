# Broad Habitat area estimates of change for Great Britain, summarized by ITE Land Class 1

## Overview
- National estimates of Broad Habitat change between 1990, 1998 and 2007, calculated using the 2007 ITE Land Classification.
- Data derived from Countryside Survey (CS) and summarized by Land Class to show how areas of Broad Habitat have changed over time.
- Mapping methodology and classifications are described in multiple referenced sources.

## What the dataset contains
- Time periods: YEAR_FROM and YEAR_TO (survey years).
- Land classification: LAND_CLASS (ITE Land Class), BROAD_HABITAT, BROAD_HABITAT_NAME.
- Change metrics: MEAN_CHANGE (change in area, in 000s hectares) between the two years; LOWER_95PCT_LIMIT and UPPER_95PCT_LIMIT (95% confidence interval for the change).
- Significance: SIG_5PCT (Yes/No) indicating statistical significance at the 5% level.
- Dataset identifier: CS1990_98_07_Broad_Habitat_Change.csv.
- Acknowledgement requirement: All CS data usage must be acknowledged.

## How changes are estimated
- Estimates are produced for each Broad Habitat (1–17) across Land Classes, aggregating national totals.
- Uses the 2007 ITE Land Classification framework (Bunce et al. 1996; Bunce et al. 1981; Bunce et al. 2007; Jackson 2000).
- National estimates are derived from the Countryside Survey 1 km survey sample squares.
- Mapping methodology and data processing described in related CS technical reports and publications.

## Data fields and Broad Habitat classifications
- YEAR_FROM / YEAR_TO: Year of Survey (from and to).
- LAND_CLASS: ITE Land Class identifiers (e.g., Bunce et al. references).
- BROAD_HABITAT / BROAD_HABITAT_NAME: Broad Habitat code and name.
- MEAN_CHANGE: Mean estimated change in Broad Habitat area (000s ha) between the two years.
- LOWER_95PCT_LIMIT / UPPER_95PCT_LIMIT: 95% confidence interval for the change.
- SIG_5PCT: Indicates whether the change is statistically significant at 5%.

Broad Habitat categories (examples):
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

## Data access, usage, and governance
- Acknowledgement: Data must be acknowledged as Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Copyright: Countryside Survey ©, with Database Right/Copyright held by CEH.
- References and publications: Extensive CS technical reports and peer-reviewed papers underpin the dataset (e.g., Scott 2007; Bunce et al. 2007; Maskell et al. 2008; Barr 1998/1990; Jackson 2000).

## Relevance for Monitoring Frameworks
- Objective alignment: Provides standardized, policy-relevant measures of habitat change over time at national scale.
- Use cases:
  - Track policy impacts on Broad Habitat extent across key habitat classes.
  - Identify significant gains or losses in habitat types to inform future management and land-use planning.
  - Inform dashboards and reports with quantified changes and uncertainty bounds.
- Data governance notes:
  - Requires clear data provenance (CS data origin) and proper metadata.
  - Facilitates transparency via confidence intervals and significance indicators.

## Key references and sources
- Countryside Survey: UK 2007 (Carey et al.)
- ITE Land Classification of Great Britain 2007 (Bunce et al.; Bunce et al. 1996; Jackson 2000)
- Methodology and field mapping references (Maskell et al. 2008; Barr 1998; Barr 1990; Scott 2007)
- Related CS technical reports and habitat mapping handbooks (CS UK 2007 TR1; CS UK 2007 TR4)