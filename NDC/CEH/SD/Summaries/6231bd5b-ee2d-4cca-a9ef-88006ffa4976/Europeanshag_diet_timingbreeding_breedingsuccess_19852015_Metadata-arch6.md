# JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

- This document delineates three related datasets on European shag phenology and diet, designed to support data discovery, combination, and exploration for insights into phenology mismatch with prey availability (sandeel). The datasets provide structured variables and clear definitions to enable self-serve analysis and data products.

## Dataset 1: JAE_Keogan_Europeanshag_phenologymismatch_shagdataset

- Scope and purpose
  - Captures phenology mismatch indicators for European shag across years, linking nesting timing to reproductive output and environmental context.
- Key variables (with definitions)
  - year: calendar year
  - laydate: day first egg in nest was laid (day of year from Jan 1)
  - day first egg in nest was laid (laydate)
  - chicks.fledged.first: number of chicks fledged in the first clutch
  - failedeggsfirst: number of failed eggs (up to four) in the first clutch
  - Mean.Lay: average lay date in each year
  - relative.lay: nest lay date relative to annual mean lay date (in days)
  - SST.past: average February/March SST in year -1
  - SST.present: average February/March SST in the current year
  - pop.size: population size in breeding pairs
  - yearcentre: year centered around the study’s average year
  - chicks.fledged.all: number of chicks fledged from all clutches
  - failedeggsall: number of failed eggs from all clutches
- How this supports data use
  - Enables cross-year comparisons of nesting timing, clutch outcomes, and environmental context (SST, population size) to assess mismatch dynamics.
  - Provides a foundation for linking phenology to reproductive success and climate indicators.
  
## Dataset 2: JAE_Keogan_Europeanshag_phenologymismatch_dietdataset

- Scope and purpose
  - Documents diet-related sampling across years, enabling analysis of prey (sandeel) contribution relative to phenology and colony timing.
- Key variables (with definitions)
  - Year: calendar year
  - Date: day of sample collection (since Jan 1)
  - Age: whether the sample is from a chick or an adult
  - SST: average February/March SST in the current year
  - yearcentre: year centered around the study’s average year
  - meandate: average date of sample collection in each year
  - datediff: sample collection date centered around the average annual sample collection date
  - SE1:SE0_proportion: proportion of 1+ sandeels relative to all sandeels in the sample
  - logitSE1:SE0: the above proportion after logit transformation
- How this supports data use
  - Facilitates analysis of diet composition over time and its relationship to phenological timing and environmental conditions.
  - The centered date metrics support temporal alignment with other datasets for integrated analyses.

## Dataset 3: JAE_Keogan_Europeanshag_phenologymismatch_bivariatedataset

- Scope and purpose
  - Combines species (shag or sandeel) with reproduction and diet-related metrics to explore relationships in a bivariate framework.
- Key variables (with definitions)
  - Year: calendar year
  - Species: shag or sandeel
  - chicks.fledged: number of chicks fledged
  - failedeggs: number of potential failed eggs
  - sandeelproportion: proportion of 1+ sandeels relative to all sandeels in the sample
  - dayofyear: day of laying for shags or day of sample collection for sandeels
  - Mean.Lay: average lay date in each year
  - Relative: day of year (either lay date or sample collection date) centered around the average lay date
- How this supports data use
  - Enables integrated analyses of reproductive output and diet across species and years, allowing examination of how diet proportions relate to nesting timing and success.

## Cross-cutting considerations

- Alignment and integration
  - Consistent year-based indexing and the use of yearcentre/relative metrics support cross-dataset joins and comparative analyses.
- Data formats and typical challenges
  - Multiple datasets with different formats and centered variables; some measures are relative to annual baselines, requiring careful interpretation during integration.
- Potential data products for Data Support
  - Self-serve dashboards or pivot-table-driven reports showing: phenology metrics vs. SST and population size; diet composition trends (sandeel proportion) across years; relationships between fledging success and diet with year-centered timing.
- Data quality and usage notes
  - As with long-term ecological datasets, expect patchy data across years or formats; leverage “understand the ask” and iterative prototyping to refine outputs and promote reuse.