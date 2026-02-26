# Dataset: Small rodent dynamics at Lathkill Dale SSSI, Derbys, 1971-2005

## Overview
- 35 years of 6-monthly population sampling for adult and juvenile bank voles (Myodes glareolus) and wood mice (Apodemus sylvaticus) in a Derbyshire ash woodland.
- Accompanied by annual and seasonal ash fruit-fall measurements and a winter severity metric.
- Includes a 4-year experiment with supplementary ash fruit in two winters to aid interpretation.

## Study setting and species
- Location: Lathkill Dale, Derbyshire, England; ash Fraxinus excelsior woodland dominating the canopy.
- Area studied: control grid of 0.45 ha; additional nearby experimental area for fruit-addition experiments.
- Species: bank vole (Myodes glareolus) and wood mouse (Apodemus sylvaticus).

## Data collection and variables
- Trapping regime: live-trapping (catch-mark-release) on a grid with 90 Longworth traps over two 24-hour periods, about every six months from 1971 to 2005.
- Population measures: density indices based on total marked adults; juveniles assessed in May/June; estimates validated against model-generated population estimates.
- Environmental measures:
  - Winter severity: mean minimum daily temperature from December to March.
  - Ash fruit-fall: dry-weight edible ash seeds per square meter, collected Sep–Mar (or Apr), with sub-totals for Sep–Dec and Dec–Mar/Apr.
- Experimental manipulation: in 1981-82 and 1984-85, 60 kg of heat-sterilized ash fruit distributed to a nearby 0.45 ha grid to create a controlled fruit-fall augmentation.
- Data columns (examples):
  - Year of data collection, winter severity, ash fruit-fall by season, trapping dates, counts of adults/juveniles, population estimates (Zippin), and weather/fruitfall comments.

## Modelling approach and design
- Objective: explain between-year variations in reproductive and population growth rates for both species.
- Method: state-space modelling applied to long-term live-trapping data; density indices validated against model-derived population estimates.
- Juvenile and adult data are analyzed separately for May/June and November/December timepoints.
- Temperature and fruit-fall used as predictors; density-dependence tested for winter and summer growth rates.
- Experimental fruit additions used to interpret fruit-fall effects on demography and to distinguish food vs. weather influences.

## Key findings
- September–March fruit-fall is the major driver of bank vole spring reproductive rate and population growth in winter and the following summer.
- September–March fruit-fall has a weaker influence on wood mouse spring reproductive rate; December–March fruit-fall shows some influence on wood mouse summer growth.
- Winter severity affects bank vole winter growth and wood mouse spring reproductive rate; neither species breeds in winter.
- Density-dependence significantly influences winter and summer growth rates for both species.
- Ash fruit addition experiments support the role of autumn–winter fruit-fall in bank vole winter demography; fruit-fall effects can last a year or more.
- Long-term modelling reveals interspecific variation but emphasizes:
  - Independent food and weather influences on bank vole demography (contrasting some Polish studies).
  - Delayed, sometimes multi-year, effects of fruit-fall on bank vole demography.
  - The importance of density dependence in rodent populations.
- Annual ash fruit fall reached up to 22.52 g m^-2 edible seed; higher values occur in oak woodlands but are shorter-lived, potentially explaining the lack of winter breeding in this system.

## Data files and structure
- Six primary data files (and their descriptive focus):
  - FlowerdewApodemusData041212csv.csv: wood mouse and environmental data (1971–2005) with yearly June data, winter severity, fruit-fall, trap counts, and density estimates.
  - FlowerdewApodemusExData040613Controlcsv.csv: wood mouse data (1981–1985) on the control area; includes November/December and May/June trapping counts.
  - FlowerdewApodemusExData040613Experimentalcsv.csv: wood mouse data (1981–1985) on the experimental area; includes November/December and May/June counts.
  - FlowerdewMyodesData291112csv.csv: bank vole and environmental data (1971–2005) with November/December and May/June trapping counts, winter severity, fruit-fall, and density estimates.
  - FlowerdewMyodesExData040613Controlcsv.csv: bank vole data (1981–1985) on the control area; includes trapping data and density estimates.
  - FlowerdewMyodesExData040613Experimentalcsv.csv: bank vole data (1981–1985) on the experimental area; includes trapping data and density estimates.
- Each file documents the layout of the respective dataset, including year, collection dates, trap counts (adults/juveniles), population estimates, and notes on weather and fruitfall.
- Data collection spans long-term, with both control and experimental (fruit addition) comparisons to disentangle ecological drivers of rodent demography.