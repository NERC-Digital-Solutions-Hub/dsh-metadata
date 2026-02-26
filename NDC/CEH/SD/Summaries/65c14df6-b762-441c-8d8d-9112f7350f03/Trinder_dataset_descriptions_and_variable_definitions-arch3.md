# This file details all of the variables in each of the datasets that are associated with Trinder S, Askew AP and Whitlock R, Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina .

## Overview
- Compiles variable definitions for eight datasets used in a study of climate-driven evolutionary changes in Festuca ovina.
- Datasets span germination, flowering time, reproductive output, pedigree/parentage, microsatellite data, and common garden experiments conducted at Buxton Climate Change Impacts Laboratory (BCCIL) in the UK.
- Focus on maternal/paternal lineage, climate treatments, soil depth treatments, and experimental blocks to assess environmental effects on early life-history traits and reproduction.

## Datasets and Purpose

- Trinder_Fovina_Germination_data_1.csv
  - Purpose: Germination data for Festuca ovina seeds.
  - Key variables: Full_ID, Mat_Clone, Mat_Block, Mat_Climate, Mat_Mean_SD, Well, Coldate, Weight.mg, Germ (TRUE/FALSE), Last_obs, Germ_obs, Planted.

- Trinder_Fovina_Germination_data_2.csv
  - Purpose: Subset of germinated seeds with planted status and additional parental information.
  - Key variables: Full_ID, Weight.mg, LHWeight, Germ_obs_days, Mat_Clone, Mat_Climate, Mat_Mean_SD, Mat_Block, Pat_Clone, Pat_Climate, Pat_Mean_SD, Pat_Block, Combi_Climate.

- Trinder_Binary_microsatellite_parentage_analysis.csv
  - Purpose: Microsatellite genotype data (binary presence/absence) used for parentage analysis.
  - Key variables: Full_ID; microsatellite loci in the form TNN.NNN with presence/absence data; missing data coded as -9.

- Trinder_BCCIL_F0_F1_Pedigree.csv
  - Purpose: Pedigree reconstruction of F0 and F1 individuals via parentage analysis.
  - Key variables: Full_ID, Mat_Clone (maternal parent, known), Pat_Clone (paternal parent, estimated), Prob (posterior probability for paternal identity).

- Trinder_Fovina_Reproductive_Data.csv
  - Purpose: Reproductive output data (offspring sired, number of flowering tillers).
  - Key variables: Pat_Clone, Pat_Block, Pat_Climate, Pat_Mean_SD, No_Sire, Flw_No.

- Trinder_Fovina_Flowering_time.csv
  - Purpose: Summary flowering time data for parental individuals; focused on deep-soil treatments.
  - Key variables: Parental_Clone, Genotype, Block, Treatment, Mean_SD, Day_mean_2012, Day_min_2012, Day_mean_2013, Day_min_2013.

- Trinder_Common_Garden_Flowering_Time_2012.csv
  - Purpose: Flowering time data in 2012 for parental clones in the common garden.
  - Key variables: tagID, Species (Festuca ovina), Genotype, Parental_Clone, SD (soil depth), Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

- Trinder_Common_Garden_Flowering_Time_2013.csv
  - Purpose: Flowering time data in 2013 for parental clones in the common garden.
  - Key variables: tagID, Species (Festuca ovina), Genotype, Parental_Clone, SD, Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

## Key Experimental Design Elements

- Location and management
  - Buxton Climate Change Impacts Laboratory (BCCIL), Derbyshire, UK (abbrev. BCCIL).
  - Treatments include climate origins and soil depth treatments (e.g., Deep vs. Shallow soil depth) across multiple blocks.

- Parental and progeny structure
  - Maternal (Mat_Clone) and paternal (Pat_Clone) parents collected at BCCIL.
  - Combined parental climate origin (Combi_Climate) capturing interaction effects between maternal and paternal treatments.

- Data types and measures
  - Germination timing and success (Germ_obs_days, Germ_obs, Last_obs_days).
  - Seed and seedling metrics (Weight.mg, LHWeight).
  - Reproductive output (No_Sire, Flw_No).
  - Flowering time metrics across years and microcosms (Day_Min, Day_Max, Day_Median, Day_Range).

- Pedigree and genetics
  - Microsatellite data in binary form for parentage analysis (Trinder_Binary_microsatellite_parentage_analysis.csv).
  - Pedigree reconstruction with probabilistic paternal assignments (Trinder_BCCIL_F0_F1_Pedigree.csv).

## Data Quality and Metadata Considerations

- Metadata completeness and standardization
  - Explicit variable definitions, formats, and date representations (dd/mm/yyyy; Julian Days).
  - Multiple datasets reference consistent experimental structures (clone IDs, blocks, climate treatments, soil depth).
- Data gaps and handling
  - Some datasets include missing values (e.g., -9 in microsatellite data).
  - Complex composite variables (e.g., Combi_Climate) require careful interpretation to disentangle parental climate effects.
- Shared data and governance
  - Data are organized with detailed definitions to facilitate reuse and integration into monitoring or policy-relevant analyses.
  - The collection spans several years and experimental conditions, enabling temporal monitoring of climate-related reproductive traits.

## Relevance for Monitoring Frameworks

- Enables environmental health monitoring by linking climate/manipulated soil depth conditions to germination, flowering time, and reproductive success.
- Supports evaluation of policy-relevant questions on climate change impacts on plant reproductive traits and potential adaptive responses.
- Provides a rigorous framework for data governance: provenance, metadata clarity, and explicit data sharing through well-documented datasets.
- Offers a multi-level view (seed/seedling stage, flowering phenology, reproductive output, and genetic lineage) for comprehensive environmental health indicators.
- The structured pedigree and microsatellite data allow genomic-informed monitoring of hereditary responses to environmental changes.