# This file details all of the variables in each of the datasets that are associated with Trinder S, Askew AP and Whitlock R, Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina .

## Overview
- Presents a collection of datasets linked to a climate-driven evolutionary study on Festuca ovina, focusing on germination, flowering, reproductive output, and genetic pedigree.
- Data originate from Buxton Climate Change Impacts Laboratory (BCCIL) and include maternal/paternal lineage, experimental treatments, spatial context, and temporal measurements.
- Intended for GIS-informed analysis: mapping spatial blocks, soil depth treatments, and treatment origins, as well as linking genetic and phenotypic data.

## Datasets and GIS-relevant details

- Trinder_Fovina_Germination_data_1.csv
  - What it contains: Germination data for Festuca ovina seeds.
  - Key variables: Full_ID, Mat_Clone, Mat_Block, Mat_Climate, Mat_Mean_SD, Well, Coldate, Weight.mg, Prep, Germ, Last_obs, Germ_obs, Last_obs_days, Germ_obs_days, Planted.
  - GIS relevance: Spatial context at seed/plate level (Well) and maternal treatment context (Mat_Block, Mat_Climate).

- Trinder_Fovina_Germination_data_2.csv
  - What it contains: Subset of germination data for seeds that germinated and were planted, with paternal lineage information.
  - Key variables: Full_ID, Weight.mg, LHWeight, Germ_obs_days, Mat_Clone, Mat_Climate, Mat_Mean_SD, Mat_Block, Pat_Clone, Pat_Climate, Pat_Mean_SD, Pat_Block, Combi_Climate.
  - GIS relevance: Enables analysis of paternal effects and combined parental climate (Combi_Climate) alongside maternal context.

- Trinder_Binary_microsatellite_parentage_analysis.csv
  - What it contains: Microsatellite genotype data in binary form used for parentage analyses.
  - Key variables: Full_ID + multiple locus columns (TNN.NNN) with presence/absence (missing = -9).
  - GIS relevance: Genetic provenance layer to contextualize spatially distributed individuals; supports integration with phenotypic/spatial datasets via Full_ID.

- Trinder_BCCIL_F0_F1_Pedigree.csv
  - What it contains: Reconstructed pedigree of F0 and F1 individuals from parentage analyses.
  - Key variables: Full_ID, Mat_Clone, Pat_Clone, Prob (posterior probability for paternal clone identification).
  - GIS relevance: Links individuals to maternal/paternal origins for spatial-genetic analyses.

- Trinder_Fovina_Reproductive_Data.csv
  - What it contains: Reproductive outcomes (offspring sired and flowering tillers).
  - Key variables: Pat_Clone, Pat_Block, Pat_Climate, Pat_Mean_SD, No_Sire, Flw_No.
  - GIS relevance: Spatial and climatic context of paternal contributions; supports mapping reproductive output against treatments and blocks.

- Trinder_Fovina_Flowering_time.csv
  - What it contains: Summary flowering time data for parental Festuca ovina individuals.
  - Key variables: Parental_Clone, Genotype, Block, Treatment, Mean_SD, Day_mean_2012, Day_min_2012, Day_mean_2013, Day_min_2013.
  - GIS relevance: Temporal phenology summarized by spatial blocks and treatments; can be mapped across years.

- Trinder_Common_Garden_Flowering_Time_2012.csv
  - What it contains: Flowering time data for parental clones in the 2012 common garden.
  - Key variables: tagID, Species, Genotype, Parental_Clone, SD, Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.
  - GIS relevance: Fine-grained spatial metadata (Bay, Location, Block) for geospatial analysis of flowering phenology.

- Trinder_Common_Garden_Flowering_Time_2013.csv
  - What it contains: Flowering time data for parental clones in the 2013 common garden.
  - Key variables: tagID, Species, Genotype, Parental_Clone, SD, Bay, Location, Block, Treatment, Mean_SD, Day_Min, Day_Max, Day_Median, Day_Range.
  - GIS relevance: Complementary 2013 spatial-phenology data for trend assessment across years.

## GIS-focused interpretation and workflows
- Join keys and linkages
  - Use Full_ID to connect germination, pedigree, and reproductive data.
  - Use Parental_Clone, Mat_Clone, and Pat_Clone to relate maternal/paternal origins across datasets.
  - Combine Block/Location/Bay fields with SD (soil depth) to map spatial and microhabitat contexts.

- Spatial and temporal mapping opportunities
  - Map germination events by Well and preparation/collection dates to study spatial patterns within plates and temporal trends.
  - Visualize flowering times and flowering time ranges across blocks, bays, and soil depths (SD) for 2012 and 2013 common gardens.
  - Analyze reproductive output (No_Sire, Flw_No) in relation to paternal lineage, block, climate treatments, and soil depth.

- Data integration considerations
  - Data are distributed across many files with overlapping but non-identical metadata; plan for careful schema alignment.
  - Some fields have multiple derived or summarized forms (e.g., Day_min, Day_mean, Day_Median); decide on a consistent set of metrics.
  - Missing data are indicated by -9 in microsatellite data; handle accordingly in analyses.

## Data quality, standards, and challenges for GIS
- Data are spread across numerous datasets with varying definitions and resolutions.
- Inconsistent or incomplete data standards across datasets may require harmonization before integration.
- Large or complex datasets may need packaging into manageable chunks for processing and visualization.
- Cleaning and transforming data (e.g., date formats, categorical encodings) is often necessary prior to GIS analysis.
- Teams conducting analyses may need adequate domain expertise to interpret climate-treatment, soil-depth, and parental-clone designations correctly.

## Provenance and usage context
- Source: Buxton Climate Change Impacts Laboratory (BCCIL), with datasets tied to the study on climate-driven evolutionary changes in reproductive and early-life traits of Festuca ovina.
- Datasets collectively enable analyses of genetic pedigree, phenotypic traits (germination, flowering, reproduction), and environmental treatments within a spatial experimental framework.