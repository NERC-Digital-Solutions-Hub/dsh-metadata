# Population count data from a resource degradation and temperature variation population dynamics experiment in the Plodia -Venturia host-parasitoid interaction

## Overview
- Datasets from a multi-generation microcosm experiment investigating how daily stochastic temperature fluctuations and host-resource degradation affect population dynamics of Plodia interpunctella (host) and Venturia canescens (parasitoid).
- Experimental scope: roughly six host generations in laboratory conditions using stock cultures; parasitoids from a parthenogenetic asexual strain.
- Data capture includes host and parasitoid counts, life-stage counts, and weekly mortality across treatments.

## Experimental design
- Full factorial design combining:
  - Temperature: Constant (Cst) vs Variable (Var) around a mean of 26°C. Var fluctuates daily between 22.3°C and 30.2°C (mean 26°C, SD ~1.5°C; AR(1) = 0.02).
  - Resource degradation (diet): 0, 25, 50, 75% of wheat germ replaced by methyl cellulose (indigestible bulking agent).
- Microcosms:
  - 48 total: 3 replicates for each combination of microcosm type, temperature, and diet (Pi vs PiVc) (3 × 2 × 2 × 4).
  - Microcosm setup: 15 male and 15 female fifth instar larvae per container, 83 g of assigned resource; maintained at 26°C until initial pupation, then subjected to their temperature treatment.
  - Biocontrol dynamics: In PiVc (host-parasitoid) microcosms, two newly emerged adult parasitoids added after week 9.
- Monitoring and duration:
  - Experiment runs 262 days.
  - Weekly monitoring from week 9 to week 37; daily/weekly counts of deaths, life stages, and pupae recorded.
  - Diet section replacements and counts conducted in half-sections of the oldest diet replaced weekly.

## Datasets included
- VariableTemperatureTimeSeries_DQE.csv
  - Variables: DAY (day in the temperature time series), Date, Week (experimental week), Temp (temperature in °C).
- Pop-counts-data_DQE.csv
  - Population_code: microcosm ID encoding species (Pi or PiVc), temperature treatment (Cst/Var), diet level (0–75), and replicate.
  - Population_observation: unique ID per population per monitoring week.
  - Treatment: combined microcosm type, temperature, and diet.
  - Population_Replicate: replicate number (3 per microcosm condition).
  - Temperature: Cst or Var.
  - Diet: 0, 25, 50, 75 (percent replaced by methyl cellulose).
  - Species: Pi (host alone) or PiVc (host-parasitoid).
  - Experimental_week / Experimental_day
  - Monitoring_week
  - Section_replaced: which diet section was replaced weekly (half-section counted for data collection).
  - Number_dead_Pi / Number_dead_Vc: weekly deaths of host and parasitoid.
  - Number_Pi_L1-L3_instars / Number_Pi_L4-L5_instars: counts of early and late host instars.
  - Number_Pi_pupae / Number_Vc_pupae: counts of host and parasitoid pupae.
  - Observer_Diet-AdultsCounts / Observer_LarvalCounts: data collectors for diet replacement and counts.
  - Comments: additional notes.

## Data schema and variables
- Two CSV files capture complementary data: environmental time series and population counts across microcosms.
- Population_code encodes species, temperature treatment, and resource degradation level with replicate information embedded.
- Detailed weekly and experimental-day granularity supports temporal analyses of host-parasitoid dynamics under environmental variability and resource stress.

## Data collection and time frame
- Baseline: Microcosms initiated with adult hosts; constant conditions for initial development before assignment to treatment.
- Monitoring schedule: Weekly live counts of adults, larvae instars, and pupae; weekly removals of dead adults/parasitoids.
- Diet management: Replenishment of a portion of the resource every week; six diet sections per microcosm analyzed over time.

## Quality control and provenance
- Data entry checks performed; outliers rechecked during initial data analysis.
- Data and methods grounded in established protocols (referenced in accompanying notes): Begon, Sait & Thompson (1995); Boots (2011); Cameron et al. (2007).

## Usage notes and governance
- Appropriate for analyses of how temperature variability and resource degradation influence host-parasitoid population dynamics in a controlled setting.
- Important considerations for reuse:
  - Align interpretations of Diet (0–75%) and Temperature (Cst/Var) with dataset encoding in Population_code.
  - Ensure temporal alignment between Experimental_week/day and Monitoring_week for time-series analyses.
  - Take into account that data derive from laboratory microcosms, which may limit extrapolation to natural environments.
  - Check for any missing values or notes in the Comments field that may indicate measurement anomalies.
- Suggested data governance practices:
  - Maintain data provenance by preserving the two-file structure and the Population_code encoding.
  - Include metadata describing experimental setup, counting methods, and treatment definitions in any data release.
  - Document any future updates, corrections, or versioning to preserve auditability. 

## References
- Begon, M., Sait, S.M. & Thompson, D.J. (1995) Persistence of a parasitoid-host system Refuges and generation cycles. Proceedings of the Royal Society B-Biological Sciences, 260, 131-137.
- Boots, M. (2011) The evolution of resistance to a parasite is determined by resources. American Naturalist, 178, 214-220.
- Cameron, T.C., Wearing, H.J., Rohani, P. & Sait, S.M. (2007) Two-species asymmetric competition: effects of age structure on intra- and interspecific interactions. Journal of Animal Ecology, 76, 83-93.