# Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina

## Overview
- Catalog of variables across multiple datasets linked to a climate-driven study on Festuca ovina, including germination, pedigrees, microsatellite data, reproductive output, and flowering time.
- Data originate from Buxton Climate Change Impacts Laboratory (BCCIL), Derbyshire, UK.
- Datasets collectively cover maternal and paternal lineages, experimental blocks, climate treatments, soil depth, and phenological measurements (germination and flowering times).

## Datasets and Key Variables

- Trinder_Fovina_Germination_data_1.csv
  - Purpose: Germination data for Festuca ovina seeds.
  - Key variables: Full_ID, Mat_Clone, Mat_Block, Mat_Climate, Mat_Mean_SD (mean soil depth), Well, Coldate, Weight.mg, Prep, Germ (TRUE/FALSE), Last_obs, Germ_obs, Last_obs_days, Germ_obs_days, Planted.

- Trinder_Fovina_Germination_data_2.csv
  - Purpose: Subset of germinated/planted seeds with paternal information.
  - Key variables: Full_ID, Weight.mg, LHWeight (ordinal seed mass), Germ_obs_days, Mat_Clone, Mat_Climate, Mat_Mean_SD, Mat_Block, Pat_Clone, Pat_Climate, Pat_Mean_SD, Pat_Block, Combi_Climate (combined parental climate origin).

- Trinder_BCCIL_F0_F1_Pedigree.csv
  - Purpose: Pedigree of F0 and F1 individuals from parentage analysis.
  - Key variables: Full_ID, Mat_Clone, Pat_Clone, Prob (posterior probability for paternal clone identification).

- Trinder_Binary_microsatellite_parentage_analysis.csv
  - Purpose: Microsatellite genotype data for parentage and genetic analyses.
  - Key variables: Full_ID plus binary presence/absence data for microsatellite loci (headers like TNN.NNN); missing data denoted by -9.

- Trinder_Fovina_Reproductive_Data.csv
  - Purpose: Reproductive characteristics (offspring sired and flowering output).
  - Key variables: Pat_Clone, Pat_Block, Pat_Climate, Pat_Mean_SD, No_Sire, Flw_No.

- Trinder_Fovina_Flowering_time.csv
  - Purpose: Summary flowering time for parental individuals from BCCIL.
  - Key variables: Parental_Clone, Genotype, Block, Treatment, Mean_SD, Day_mean_2012, Day_min_2012, Day_mean_2013, Day_min_2013 (note: 2013 fields described with similar structure).

- Trinder_Common_Garden_Flowering_Time_2012.csv
  - Purpose: Flowering time data in 2012 for parental clones in the common garden.
  - Key variables: tagID, Species, Genotype, Parental_Clone, SD (Deep/Shallow soil depth), Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

- Trinder_Common_Garden_Flowering_Time_2013.csv
  - Purpose: Flowering time data in 2013 for parental clones in the common garden.
  - Key variables: tagID, Species, Genotype, Parental_Clone, SD, Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.

## Data Provenance and Definitions
- General definitions: Full_ID format NNNN_XN; paternal and maternal clone identifiers; Julian Days used for flowering time metrics.
- Institutions and context: Data tied to BCCIL climate treatments, soil depth categories (Deep/Shallow), and experimental blocks.

## Data Governance Considerations for Data Leaders
- Data lineage and integration: Datasets interlink via Mat_Clone, Pat_Clone, Parental_Clone, Full_ID, and experimental factors (Block, Climate, SD). Cross-dataset linking enables comprehensive analyses of germination, reproduction, and phenology under climate treatments.
- Metadata and documentation: Descriptions provide variable definitions, formats, and units (e.g., Julian Days for flowering). Some 2013 field descriptions in the source appear truncated; verify completeness for reproducibility.
- Discoverability and packaging: Data are provided as multiple CSVs with clear names; consider consolidating into a unified data dictionary and establishing consistent cross-dataset identifiers to improve discoverability and reuse.
- Data quality and encoding: Presence/absence data for microsatellites; missing values indicated by -9. Ensure uniform coding and validation across analyses.
- Reuse and collaboration: Data support parentage analyses, genetic analyses, and climate-driven phenotype studies; well-suited for reproducibility efforts and cross-study comparisons if documentation is maintained.

## Practical Considerations for Action
- For data strategy, ensure a centralized data dictionary that maps all identifiers (Full_ID, Mat_Clone, Pat_Clone, Parental_Clone) across datasets.
- Maintain clear provenance notes for each dataset, including experimental conditions (Block, Treatment, SD) and their relationships to phenotypic measurements.
- Establish data quality checks (e.g., consistency of date formats, Julian Day calculations, and missing data handling) to support robust analyses of germination, reproduction, and flowering time under climate treatments.