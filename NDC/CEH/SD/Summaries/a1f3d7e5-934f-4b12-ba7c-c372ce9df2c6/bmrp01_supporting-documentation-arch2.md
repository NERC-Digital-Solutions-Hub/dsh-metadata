# Sampling regime and collection methods

- Study system and scope
  - The Banded Mongoose Research Project examines wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Ongoing since 1995; 10–12 social groups typically, each with ~20 adults plus offspring.
  - Individuals are uniquely marked for long-term identification; pups marked and sampled for genetic analyses to determine parentage.
  - Groups are habituated to observers; some members carry radio collars for group localization.

- Data collection and field procedures
  - Regular trapping every two months to maintain identification marks.
  - Groups visited every 1–3 days for at least 20 minutes to record group composition, life history, and reproductive behavior.
  - Birth dates recorded during pregnancy; pups marked around 30 days after emergence from the den; 2 mm tail-tip tissue samples collected for genetic analyses.
  - DNA genotyping uses 43 microsatellite markers (or 35 for a subset).
  - Intergroup interactions (IGIs) recorded ad libitum during visits; IGIs defined as sighting and subsequent vocalizing, chasing, and/or fighting between groups.

- Field instrumentation and data capture
  - Data recorded with Psion II LZ data loggers (until 2014) and later with a bespoke Mongoose 2000 app on Samsung tablets.
  - Data imported into a Microsoft Access database; radio collars weigh ~30 g with 20 cm antenna.
  - Instruments calibrated to factory settings.

- Analytical methods and focal outputs
  - Mortality from intergroup conflict (males vs females)
    - Adults (>1 year) who died due to intergroup fighting between 2000–2015 (n = 19; 17 males, 2 females).
    - Analysis restricted to groups with >5 years of detailed life-history data (10 groups total).
    - Exposure calculated in mongoose-years (male: 1,171; female: 728).
    - Mortality rate per group computed as D/E × 100 (D = deaths, E = exposure).
  - Fitness benefits from intergroup conflict
    - For adults with lifetime data since Jan 2000: lifetime extra-group offspring (LEGO) and lifetime reproductive success (LRS).
    - LEGO = offspring conceived with extra-group partners; LRS = total offspring across lifetime.
    - Paternity/maternity assignments from genetic pedigrees with 90% (full 43-marker) or 95% (subset 35-marker) confidence.
    - Outputs include total IGIs experienced and age at death per individual.
  - Frequency of IGIs by female estrus state
    - IGIs observed 2000–2019 categorized by focal vs rival group estrus state.
    - States: FE RE (focal estrus, rival estrus); FE RNE (focal estrus, rival non-estrus); FNE RE (focal non-estrus, rival estrus); FNE RNE (both not in estrus).
    - For 539 IGIs with estrus data, counts are summed by the estrus state and by days the focal-rival pair were observed in that state.

- Quality control and data integrity
  - Mongoose 2000 app includes internal consistency checks (e.g., presence required to record further data).
  - Data validated with MS Access queries and custom R scripts to detect inconsistencies (e.g., duplicate death records).

- Data structure and accessibility
  - Data stored as three CSV files:
    - Mortality rates from intergroup conflict (group, sex, death, D, exposure, mortality.rate, exposure, etc.).
    - LEGO and LRS data (sex, lego, lrs, number.igis, age.at.death).
    - IGI frequency by estrus state (focal.group.id, rival.group.id, focal.rival.estrus.state, number.IGIs, days.in.estrus.state, olre).
  - Outputs represent standardized, time-bounded datasets suitable for cross-study comparisons and long-term monitoring.
  - Data are prepared and structured to support uploading to appropriate data portals, aligning with standard environmental monitoring practices.

- Timeline and scope of datasets
  - Intergroup mortality: 2000–2015.
  - LEGO, LRS, and IGI exposure data: 2000–2019 (with lifetime measures for individuals).
  - Estrus-state analysis covers IGIs from 2000–2019.