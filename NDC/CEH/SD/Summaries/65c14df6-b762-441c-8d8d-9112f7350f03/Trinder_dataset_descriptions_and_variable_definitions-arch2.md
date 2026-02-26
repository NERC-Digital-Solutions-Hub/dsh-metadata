# This file details all of the variables in each of the datasets that are associated with Trinder S, Askew AP and Whitlock R, Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina .

## Overview
- Documented datasets come from the Buxton Climate Change Impacts Laboratory (BCCIL) and relate to climate-driven evolutionary changes in Festuca ovina.
- Datasets cover germination, pedigree, genetic (microsatellite) data, reproductive output, and flowering time, including field and common garden experiments.
- Data are organized around maternal/paternal parental lines, experimental blocks, soil-depth treatments, and climate treatments, enabling cross-dataset analyses of environmental effects on reproductive and life-history traits.

## Datasets and Key Features

- Dataset: Trinder_Fovina_Germination_data_1.csv
  - Purpose: Germination data for Festuca ovina seeds.
  - Key variables: Full_ID, Mat_Clone, Mat_Block, Mat_Climate, Weight.mg, Germ, Germ_obs_days, Last_obs_days, Last_obs, Planted, Prep, Germ_obs, Cana; date fields use dd/mm/yyyy formats.

- Dataset: Trinder_Fovina_Germination_data_2.csv
  - Purpose: Subset of germinated seeds with paternal parentage information.
  - Key variables: Full_ID, Weight.mg, LHWeight, Germ_obs_days; Mat_Clone, Mat_Climate, Mat_Block; Pat_Clone, Pat_Climate, Pat_Mean_SD, Pat_Block; Combi_Climate (combined parental climate origin).

- Dataset: Trinder_Binary_microsatellite_parentage_analysis.csv
  - Purpose: Microsatellite genotype data for parentage and genetic analyses.
  - Key variables: Full_ID and binary presence/absence data for microsatellite loci (e.g., TNN.NNN); missing data coded as -9.

- Dataset: Trinder_BCCIL_F0_F1_Pedigree.csv
  - Purpose: Pedigree relationships for F0 and F1 individuals as inferred by parentage analysis.
  - Key variables: Full_ID, Mat_Clone (maternal), Pat_Clone (paternal, estimated), Prob (posterior probability of paternal clone identification).

- Dataset: Trinder_Fovina_Reproductive_Data.csv
  - Purpose: Reproductive characteristics (offspring sired and flowering tillers).
  - Key variables: Pat_Clone, Pat_Block, Pat_Climate, Pat_Mean_SD; No_Sire (offspring sired) and Flw_No (flowering tillers).

- Dataset: Trinder_Fovina_Flowering_time.csv
  - Purpose: Summarised flowering time data for parental Festuca ovina from BCCIL; focused on deep soil treatment.
  - Key variables: Parental_Clone, Genotype, Block, Treatment, Mean_SD; Day_mean_2012, Day_min_2012, Day_mean_2013, Day_min_2013 (flowering time metrics in Julian Days).

- Dataset: Trinder_Common_Garden_Flowering_Time_2012.csv
  - Purpose: Flowering time data for parental clones in the common garden (2012).
  - Key variables: tagID, Species, Genotype, Parental_Clone, SD (Deep/Shallow), Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

- Dataset: Trinder_Common_Garden_Flowering_Time_2013.csv
  - Purpose: Flowering time data for parental clones in the common garden (2013).
  - Key variables: tagID, Species, Genotype, Parental_Clone, SD, Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

## Data Structure and Standardization

- Consistent identifiers: Full_ID uses a NNNN_XN format for seeds/plants; parental IDs (Parental_Clone, Mat_Clone, Pat_Clone) follow NNNN formats.
- Date formats: Dates are stored in dd/mm/yyyy for collection, preparation, germination, and last observation dates.
- Flowering time: Expressed as Julian Days in 2012 and 2013 datasets (Day_Min, Day_Max, Day_Median, Day_Range).
- Climate and soil treatments: Variables for maternal/paternal climate origin (Mat_Climate, Pat_Climate), soil depth (Mean_SD, SD), and combined parental climate origin (Combi_Climate).
- Genetic data: Microsatellite data are binary (presence/absence) across loci, with missing data coded as -9.

## Data Quality and Accessibility

- Data quality emphasis: Verification and standardization of data from established sources (BCCIL) with explicit QA-ready formats.
- Accessibility considerations: Datasets are organized to enable cross-dataset integration, including pedigree linkage (Pedigree), parentage probabilities, and standardized trait measurements.
- Missing data handling: Binary microsatellite data use -9 for missing; other fields include non-germination and non-sire indicators (e.g., No_Sire).

## Relevance for Environmental Monitoring

- Enables monitoring of climate-related effects on germination success, reproductive output, and flowering phenology across maternal/paternal lineages and soil/climate treatments.
- Supports evaluation of evolutionary responses to climate and soil depth by integrating germination, flowering time, and genetic lineage data.
- Provides standardized outputs (maps, charts, reports) for assessing environmental health and policy performance over time, in line with standardized environmental monitoring practices.
- The inclusion of paternal/maternal origins, block design, and treatment combinations facilitates robust analyses of environmental drivers and their interaction effects on reproductive traits.