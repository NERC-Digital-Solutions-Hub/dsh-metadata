# Banded Mongoose Research Project

## Scope and Purpose
- Long-term study of wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda since 1995.
- Typical population: 10–12 social groups, ~20 adults per group, plus offspring.
- Aim: observe life history, reproductive behavior, and intergroup interactions; derive metrics such as mortality from intergroup conflict, fitness benefits from intergroup conflict, and how intergroup interactions relate to female estrus.

## Study Population and Field Methods
- Location: Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
- Group structure: 10–12 groups occupying distinct territories; regular visits to record group composition, births, deaths, reproductive status, and intergroup interactions (IGIs).
- Individual identification: unique marks via fur shave patches (adults) or dye marks (pups); frequent trapping every two months.
- Tracking: 1–2 individuals per group fitted with radio collars (≈30 g) for group localization.
- Habituation: most groups habituated to observers at distances <5 meters.
- Field cadence: groups visited every 1–3 days for at least 20 minutes.
- Reproduction: estrus synchrony; pregnancy monitoring; birth dates recorded; pups marked around 30 days; tissue samples taken for genetic analysis (~2 mm tail tips).
- Genetics: parentage determined using a microsatellite panel (43 markers; 35 markers for subset); to assign maternity/paternity with 90–95% probability.
- Data capture tools: Psion II data loggers (until 2014) and Mongoose 2000 app on Samsung tablets; data stored in MS Access database.
- Calibration: field instruments calibrated to factory settings.

## Data Collection Instruments and Calibration
- Data collection apps: Mongoose 2000; handles data integrity checks.
- Calibration: factory settings for field instruments.
- Data integration: offspring genotypes and life-history data linked via MS Access and custom R scripts for quality checks.

## Analytical Methods
- Mortality from intergroup conflict (male and female):
  - Adults (>1 year) with deaths from intergroup fighting (n = 19; 17 males, 2 females) from Jan 2000 to Dec 2015.
  - Exposures computed as mongoose-years (males: 1,171; females: 728).
  - Mortality rate per group: deaths divided by exposure, times 100, calculated separately for each sex.
- Fitness benefits from intergroup conflict (males and females):
  - Lifetime extra-group offspring (LEGO) and lifetime reproductive success (LRS) computed for adults observed after Jan 2000.
  - LEGO: number of offspring conceived with extra-group partners.
  - LRS: total offspring over lifetime (within- and extra-group).
  - Parentage assigned genetically with probabilities 90% (full 43-marker panel) or 95% (35-marker subset).
  - Additional metrics: total lifetime IGIs experienced and age at death.
- Frequency of intergroup conflict with female estrus:
  - IGIs (Jan 2000–Mar 2019) categorized by focal vs. rival group estrus state.
  - Estrus states: FE RE, FE RNE, FNE RE, FNE RNE.
  - For each focal–rival pair with estrus data (n = 539 IGIs), counts of IGIs by estrus state and total days pairs spent in each state.

## Quality Control and Data Structure
- Quality assurance:
  - Mongoose 2000 app includes internal checks (e.g., presence requirement for data collection).
  - Data QA via MS Access queries and custom R code to detect inconsistencies (e.g., duplicate death records).
- Data structure:
  - Three CSV files:
    - Mortality rates from intergroup conflict (columns include group.id, sex, death, exposure, mortality.rate).
    - Fitness benefits from intergroup conflict (columns include sex, lego, lrs, number.igis, age.at.death).
    - IGI frequency by estrus state (columns include focal.group.id, rival.group.id, focal.rival.estrus.state, number.igis, days.in.estrus.state, olre, unique observation identity).