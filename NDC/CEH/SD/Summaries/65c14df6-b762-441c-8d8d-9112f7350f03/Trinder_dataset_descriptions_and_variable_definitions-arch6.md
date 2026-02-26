# Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina .

- Overview
  - A collection of datasets and variable definitions describing germination, reproductive traits, flowering time, and pedigrees for Festuca ovina from Buxton Climate Change Impacts Laboratory (BCCIL), aimed at exploring climate-driven evolutionary changes in life-history traits.
  - Data support focus: organizing, validating, and enabling combining of data from multiple sources to facilitate analysis and data products for researchers.

- Datasets and core purpose
  - Trinder_Fovina_Germination_data_1.csv
    - Germination-related data for F1 Festuca ovina seeds; key fields include Full_ID, Mat_Clone, Mat_Block, Mat_Climate, Mat_Mean_SD, Well, Coldate, Weight.mg, Prep, Germ, Last_obs, Germ_obs, Last_obs_days, Germ_obs_days, Planted.
  - Trinder_Fovina_Germination_data_2.csv
    - Subset of germinated/planted seeds with paternal information; includes Weight.mg, LHWeight, Germ_obs_days, Mat_Clone, Mat_Climate, Mat_Block, Pat_Clone, Pat_Climate, Pat_Mean_SD, Pat_Block, Combi_Climate.
  - Trinder_Binary_microsatellite_parentage_analysis.csv
    - Microsatellite genotype data in binary presence/absence form for parentage analysis; Full_ID plus locus-based columns (e.g., TNN.NNN) with -9 indicating missing data.
  - Trinder_BCCIL_F0_F1_Pedigree.csv
    - Reconstructed pedigree for F0 and F1 individuals; Full_ID, Mat_Clone, Pat_Clone, Prob (posterior probability for paternal clone identification).
  - Trinder_Fovina_Reproductive_Data.csv
    - Reproductive characteristics of P0 individuals; Pat_Clone, Pat_Block, Pat_Climate, Pat_Mean_SD, No_Sire (offspring sired), Flw_No (flowering tillers produced).
  - Trinder_Fovina_Flowering_time.csv
    - Summarised flowering time data for parental clones; Parental_Clone, Genotype, Block, Treatment, Mean_SD, Day_mean_2012, Day_min_2012, Day_mean_2013, Day_min_2013 (note: 2013 fields partly described with formatting irregularities).
  - Trinder_Common_Garden_Flowering_Time_2012.csv
    - Flowering time data in 2012 for parental clones in the common garden; tagID, Species, Genotype, Parental_Clone, SD, Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.
  - Trinder_Common_Garden_Flowering_Time_2013.csv
    - Flowering time data in 2013 for parental clones in the common garden; similar structure to 2012 dataset.

- Key data structure and integration points
  - Unique identifiers and lineage
    - Full_ID uniquely identifies F1 seeds/plants; Mat_Clone (maternal line), Pat_Clone (paternal line) link to parental plants.
  - Experimental metadata
    - Mat_Block, Mat_Climate; Pat_Block, Pat_Climate; Combi_Climate to capture parental climate origins and cross-combinations (C_C, C_D, D_C, D_D).
  - Pedigree and genetics
    - Pedigree built from microsatellite data (binary presence/absence per locus) and parentage probabilities; cross-dataset links via Full_ID, Mat_Clone, Pat_Clone.
  - Phenotypes and time-to-event data
    - Germination outcomes (Germ), germination timing (Germ_obs_days, Last_obs_days), seed/seedling size (Weight.mg, LHWeight).
    - Reproductive output (No_Sire, Flw_No) and flowering times (Day_Min, Day_Max, Day_Median, Day_Range) across years and experimental conditions.
  - Common garden and field-derived timing
    - Flowering time summaries for 2012 and 2013 from common garden experiments, enabling cross-year comparisons under standardized conditions.
  - Data formats and units
    - Dates in dd/mm/yyyy; Julian days for flowering times; soil depth values (SD) indicating Deep or Shallow; categorical/ordinal representations for seed mass (LHWeight) and other factors.
    - Missing data indicated (e.g., -9 in microsatellite data); some descriptive fields include minor formatting inconsistencies in the text.

- Data use and product potential
  - Build self-service data products (dashboards, pivot-style summaries) to explore:
    - Germination success by Mat_Climate, Mat_Block, and Combi_Climate.
    - Reproductive output and flowering time by paternal/maternal climate origin and cross combinations.
    - Pedigree-informed analyses linking genetic background with life-history trait variation across climate treatments.
  - Enable cross-dataset analyses by linking F0/F1 pedigree with germination, flowering time, and reproductive data via Full_ID and parental clones.
  - Provide provenance and guidance for data interpretation, given multiple years, treatments, and experimental settings.

- Data quality, standards, and support needs
  - Heterogeneous data across datasets and years; standardization of variable naming and units would aid integration.
  - Ensure consistent handling of dates and Julian day conversions when merging time-based metrics.
  - Maintain clear mapping between Combi_Climate and individual parental climate terms to support robust climate-origin analyses.
  - Document and handle missing data appropriately, especially in microsatellite presence/absence datasets (-9).

- Access, provenance, and context
  - Data originate from Buxton Climate Change Impacts Laboratory (BCCIL), Derbyshire, UK.
  - Datasets are designed to support analysis of climate-driven evolutionary changes in reproductive and early-life-history traits in Festuca ovina, with explicit links between germination, reproduction, flowering phenology, and genetic pedigree across environmental treatments.