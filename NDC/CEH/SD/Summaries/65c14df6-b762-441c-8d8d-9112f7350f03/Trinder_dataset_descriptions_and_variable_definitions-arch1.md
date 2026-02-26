# Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina

## Overview
- A collection of datasets describing germination, flowering time, reproduction, and pedigree for Festuca ovina plants, collected at Buxton Climate Change Impacts Laboratory (BCCIL), Derbyshire, UK.
- Aimed at identifying correlations between climate treatments, soil depth, and life-history traits; enabling parentage analyses and predictive insights into climate-driven evolutionary change.

## Datasets and main variables

- Trinder_Fovina_Germination_data_1.csv
  - Germination-related: Full_ID, Mat_Clone, Mat_Block, Mat_Climate, Mat_Mean_SD, Well, Coldate, Weight.mg, Prep, Germ (TRUE/FALSE), Last_obs, Germ_obs, Last_obs_days, Germ_obs_days, Planted.

- Trinder_Fovina_Germination_data_2.csv
  - Subset with paternal parentage: Full_ID, Weight.mg, LHWeight, Germ_obs_days, Mat_Clone, Mat_Climate, Mat_Mean_SD, Mat_Block, Pat_Clone, Pat_Climate, Pat_Mean_SD, Pat_Block, Combi_Climate (C_C, C_D, D_C, D_D).

- Trinder_Binary_microsatellite_parentage_analysis.csv
  - Microsatellite genotype data in binary (PRESENCE/ABSENCE) form for parentage and genetic analyses; columns include TNN.NNN loci with numeric fragment-length bins; -9 denotes missing data.

- Trinder_BCCIL_F0_F1_Pedigree.csv
  - Pedigree information for F0 and F1 individuals; Full_ID, Mat_Clone, Pat_Clone (estimated), Prob (posterior probability of paternal clone identification).

- Trinder_Fovina_Reproductive_Data.csv
  - Reproductive output: Pat_Clone, Pat_Block, Pat_Climate, Pat_Mean_SD, No_Sire (number of F1s sired), Flw_No (flowering tillers produced).

- Trinder_Fovina_Flowering_time.csv
  - Summarised flowering times for paternal lines from deep-soil treatment; Parental_Clone, Genotype, Block, Treatment, Mean_SD, Day_mean_2012, Day_min_2012, Day_mean_2013, Day_min_2013 (and related Julian Day metrics).

- Trinder_Common_Garden_Flowering_Time_2012.csv
  - Common garden 2012 flowering time for parental clones; tagID, Species (Festuca ovina), Genotype, Parental_Clone, SD (Deep/Shallow), Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

- Trinder_Common_Garden_Flowering_Time_2013.csv
  - Common garden 2013 flowering time for parental clones; same structure as 2012 dataset (Day_Min, Day_Max, Day_Median, Day_Range).

## Key climate and experimental design features across datasets
- Experimental variables include:
  - Mat_Climate and Pat_Climate: maternal and paternal climate treatments.
  - Combi_Climate: combined parental climate origin (C_C, C_D, D_C, D_D).
  - SD: soil depth treatment (Deep = 12 cm; Shallow = 5 cm) used in common garden and flowering time data.
  - Block/Bay/Location: spatial design within BCCIL common gardens and microcosms.
  - Treatments span control vs drought-like conditions (C vs D).

## Cross-dataset linkages and analysis opportunities
- Link maternal and paternal lineages through Mat_Clone and Pat_Clone to study genetic and maternal/paternal contributions to:
  - Germination success and timing (Germ_obs_days, Germ, Last_obs_days).
  - Early-life traits under climate and soil depth treatments.
  - Flowering time variation across years (2012, 2013) and in common garden settings.
- Pedigree and microsatellite data (Trinder_BCCIL_F0_F1_Pedigree.csv and Trinder_Binary_microsatellite_parentage_analysis.csv) enable:
  - Parentage validation, estimation of paternal contributions (Prob), and genetic analyses of trait heritability.
- Reproductive output (Trinder_Fovina_Reproductive_Data.csv) combined with flowering time (Trinder_Fovina_Flowering_time.csv and Common Garden flowering data) supports:
  - Associations between flowering phenology and siring success (No_Sire, Flw_No).
  - Climate- and soil-depth-driven shifts in reproductive strategy.

## Data provenance and accessibility notes
- All datasets are linked to the Buxton Climate Change Impacts Laboratory (BCCIL) in Derbyshire, UK.
- Data are described with explicit variable definitions, treatment codes, and date formats to facilitate reproducible analyses.
- Some datasets contain formatting irregularities in descriptions (notably in Trinder_Fovina_Flowering_time.csv), but the core variables and codes (Parental_Clone, Block, Treatment, Day/Mean metrics) are consistently defined across files.

## Analytical considerations and potential limitations
- Data include multiple hierarchical levels (seed, maternal/paternal lines, blocks, treatments), enabling mixed-effects modeling but requiring careful handling of non-independence.
- Local scale focus (BCCIL) may limit generalizability but is well-suited for climate-vegetation interaction analyses.
- The combination climate variable (Combi_Climate) provides insight into interaction effects between maternal and paternal environments.
- Missing data and coding (e.g., -9 in microsatellite data) require appropriate imputation or robust analytical strategies.

## Practical uses for analysts
- Identify correlations between climate/soil-depth treatments and:
  - Germination timing and success.
  - Flowering time shift across years and in common gardens.
  - Reproductive output and siring success.
- Leverage pedigree and microsatellite data to partition genetic and maternal/paternal contributions to observed trait variation.
- Build predictive models of reproductive and life-history trait evolution under climate change scenarios using the Maternal/Paternal Climate, soil depth, and block-level effects.