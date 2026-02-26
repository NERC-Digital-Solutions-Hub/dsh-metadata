# Impacts of experimental drought and plant trait diversity on floral resources and pollinator visitation

- A field-based experiment assessing how plant functional diversity and drought influence floral resources and pollinator activity, using standardized data collection and quality assurance to support long-term environmental monitoring.

## Study system and objectives

- Location: Wiltshire, UK on ex-arable calcareous grassland (Bromus erectus grassland type).
- Goals: quantify how drought and plant trait diversity affect (i) floral resources (flowering, nectar availability and quality) and (ii) pollinator visitation patterns; provide data suitable for monitoring environmental health and policy outcomes over time.
- Sites and design: Sown plant communities established in 2013 across 8 m x 8 m plots, arranged in a grid with 2 m gaps, replicated across six blocks.

## Experimental design

- Plant functional groups (FG) and diversity
  - FG1: deep tap roots, large leaves; expected low nutrient cycling and poor drought resistance.
  - FG2: long-lived, shallow roots, small rosettes; expected low nutrient cycling but fairly good drought resistance.
  - FG3: long-lived, shallow fibrous roots with thick, fleshy leaves; expected high nutrient cycling and fairly good drought resistance.
  - Seven community combinations formed by mixing FG1, FG2, and FG3; replicated across plots.
- Treatments
  - Drought (D): six-week period with rain exclusion via shelters, simulating extreme drought.
  - Control (C): ambient rainfall.
  - Roofed control (R): transparent roof with 5 cm holes to control for roof effects (temperature/light changes).
  - Drought shelters applied in 2015 and 2016 during two successive drought windows (late spring to mid-summer).
- Plot and block layout
  - 24 plots total (8 m x 8 m each), arranged in six blocks to control for spatial effects.
  - Each plot contains three subplots assigned to one of the three treatments (D, C, R), ensuring randomization within blocks.
  - From 2015 onward, rain shelters remained in place for the drought period (approximately six weeks).

## Data collected and measurements

- Floral resources
  - Floral resources recorded per focal plant species across subplots: number of flowers, flower diversity, and proportion of flowers with nectar.
  - Nectar measurements on three focal species (Lathyrus pratensis, Onobrychis viciifolia, Prunella vulgaris) selected for abundance and nectar accessibility.
  - Nectar volume measured with microcapillary tubes; nectar sugar concentration measured with a hand-held refractometer; sugar mass per flower over 24 hours calculated from volume and concentration.
  - Methods involved bagging racemes for 24 hours to assess standing crop plus 24-hour accumulation, then sampling up to three flowers per raceme for nectar metrics.
- Community-scale floral surveys
  - 1 m2 quadrats in the center of each subplot to count floral units (flowers that can be visited by pollinators without flying between units).
  - Flower species identification and floral-unit counts conducted; surveys carried out in two rounds on different days in July.
- Pollinator visitation
  - Observations in quadrats for 10 minutes per survey; recorded pollinator visits to flowers, visitor identity (to morphotype when possible), plant species visited, and number of floral units visited.
  - Two survey rounds conducted between July 18–22; surveys timed under suitable weather conditions (per Pollard & Yates 1993 guidelines).

## Data management and quality assurance

- Protocols and data handling
  - Standardized field protocols with dedicated datasheets; data entered into MS Access; routine checks for anomalies.
  - Linking fields across datasets to enable integration: PlotID, SubplotID, RacemeID, and SurveyID are consistent across datasets.
  - Ethics approval obtained from the University of Exeter CLES Penryn Research Ethics Committee (application 2016/1429).
- Datasets and metadata
  - Four primary data files:
    - NERCPropNectar.csv (nectar production per flower)
    - NERCNectar.csv (detailed nectar measurements per raceme/flower)
    - NERCFloralSurveys.csv (flowering communities and floral units)
    - NERCPollinatorSurveys.csv (pollinator visitation data)
  - Metadata describe variable definitions, units, and data quality notes (e.g., missing data in nectar concentration: 144 of 703 values in NERCNectar.csv; concentration data missing where nectar volumes were too small to read).
  - Data can be linked via PlotID, RacemeID, SubplotID, and SurveyID; context links to Fry et al. 2017/2018 datasets for Plot identifiers.

## Datasets and data quality notes

- NERCPropNectar.csv: nectar presence; fields include Raceme_ID, Plant_Species, Subplot_Type (D, C, R), CountWithNectar, TotalFlowersTested.
- NERCNectar.csv: absolute nectar metrics; fields include Plot_ID, Raceme_ID, ID, No_Floral_Units, Volume_Absolute (μl), Concentration_Absolute (mg/μl), Concentration_AverageBlanks, Sugar_Absolute, and Row.
  - Missing data: Concentration_Absolute missing for 144/703 values (~20%) due to insufficient nectar volume.
- NERCFloralSurveys.csv: floral survey results; fields include Plot_ID, FG, FG_Diversity, Date_Surveyed, Subplot_Type, SurveyID, TotalNumberOfPollVisits, and species-level floral-unit counts.
- NERCPollinatorSurveys.csv: pollinator visitation data; fields include Plot_ID, FG, FG_Diversity, Date_Surveyed, Subplot_Type, SurveyID, TaxonomicID, Pollinator_Species_Code, Plant_Species, No_Visits.
  - Note: observer error led to no surveys for subplot 14.C in the first pollinator round.

## Winklebury Hill experiment (context and linkage)

- Purpose: to test how plant communities with different functional traits influence carbon and nitrogen cycling in soils.
- Timeline: 2013–2016; seeds and plug plants established on bare chalk to form plant communities.
- Functional groups and expectations
  - Group 1: species with deep, thick tap roots, large leaves; lower carbon/nutrient cycling potential.
  - Group 2: small rosettes with shallow roots; intermediate cycling with better drought resistance.
  - Group 3: few deep roots but rapid carbon and nitrogen cycling; high microbial activity; potential for rapid turnover.
- Plot design
  - A grid of plots (7 across by 6 down) with multiple species per plot reflecting the three functional groups; repeated across rows to create replicated treatment structure.
- Overall aim: link plant functional traits to ecosystem processes such as soil carbon storage, nutrient cycling, and microbial activity.

## References

- Baldock KCR, Goddard MA, Hicks DM et al. (2015). Where is the UK's pollinator biodiversity? The importance of urban areas for flower-visiting insects. Proc. R. Soc. B.
- Corbet SA (2003). Nectar sugar content: estimating standing crop and secretion rate in the field. Apidologie.
- Fry et al. (2017, 2018). Ecosystem functions and vegetation data for Winklebury Hill, Salisbury Plain, UK (data records).
- Pollard E, Yates TJ (1993). Monitoring Butterflies for Ecology and Conservation.
- Prŷs-Jones OE, Corbet SA (1991). Bumblebees. The Richmond Publishing Co. Ltd.
- Rodwell JS (1992). British Plant Communities. Cambridge University Press.
- Yee TW (2010). The VGAM package for categorical data analysis. J Statistical Software.