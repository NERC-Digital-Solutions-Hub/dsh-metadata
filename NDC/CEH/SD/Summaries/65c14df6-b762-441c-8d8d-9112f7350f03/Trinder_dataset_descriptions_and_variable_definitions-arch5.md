# This file details all of the variables in each of the datasets that are associated with Trinder S, Askew AP and Whitlock R, Climate-driven evolutionary change in reproductive and earlyacting life-history traits in the perennial grass Festuca ovina .

## Overview
- Documents the variables across multiple Festuca ovina datasets used in a climate-driven evolutionary study at Buxton Climate Change Impacts Laboratory (BCCIL), Derbyshire, UK.
- Datasets cover germination, pedigree and parentage, reproductive output, and flowering time, enabling analysis of maternal/paternal effects, genetics, and phenology under different climate treatments.

## Datasets (and brief purpose)
- Trinder_Fovina_Germination_data_1.csv: Germination data for F1 seeds.
- Trinder_Fovina_Germination_data_2.csv: Subset of germination data with added paternal parentage information.
- Trinder_Binary_microsatellite_parentage_analysis.csv: Microsatellite genotype data in binary presence/absence form for parentage analyses.
- Trinder_BCCIL_F0_F1_Pedigree.csv: Pedigree of F0 and F1 individuals, including posterior probabilities for paternal clone assignments.
- Trinder_Fovina_Reproductive_Data.csv: Reproductive characteristics (offspring sired, flowering tillers).
- Trinder_Fovina_Flowering_time.csv: Summarised flowering time data for parental individuals (deep soil treatment focus).
- Trinder_Common_Garden_Flowering_Time_2012.csv: Flowering time data for parental clones in the 2012 common garden.
- Trinder_Common_Garden_Flowering_Time_2013.csv: Flowering time data for parental clones in the 2013 common garden.

## Data model and key relationships
- Core identifiers used to link datasets:
  - Full_ID: Unique ID for F1 seeds/plants and parents.
  - Mat_Clone / Pat_Clone: Maternal and paternal P0 clone identifiers.
  - Mat_Block / Pat_Block: Experimental blocks for maternal/paternal origins.
  - Mat_Climate / Pat_Climate: Climate treatment origins for maternal/paternal parents.
  - Combi_Climate: Combined parental climate origin (e.g., C_C, C_D, D_C, D_D) in the germination dataset 2.
- Trait and measurement data across datasets:
  - Germination: Germination status (Germ), timing (Germ_obs_days, Last_obs_days), seed weight (Weight.mg), preparation and planting dates.
  - Reproduction: No_Sire (number of offspring inferred sired by paternal plant), Flw_No (number of flowering tillers), paternal/block/climate metadata.
  - Flowering time: Day_Min, Day_Max, Day_Median, Day_Range (Julian days or days since setup), with separate 2012 and 2013 entries in common garden datasets and summarized 2012/2013 values in the 2012/2013 Flowering_time files.
  - Genotype/parentage: Microsatellite loci data (binary PRESENCE/ABSENCE per locus/bin), used for parentage analyses and genetic analyses.
  - Pedigree: Mat_Clone and Pat_Clone with Prob (posterior probability) for paternal clone identification.
- Cross-dataset linkage:
  - Full_ID serves as the primary key to align F1 individuals with parental data, germination outcomes, and flowering time records.
  - Pedigree and microsatellite data enable integration of genetic analyses with phenotypic traits across treatments and blocks.

## Provenance, metadata and formats
- Data originate from the Buxton Climate Change Impacts Laboratory (BCCIL) experiments, with explicit fields for collection dates, preparation dates, and treatment designations.
- Formats: CSV files with clearly defined variable names and definitions; date fields use dd/mm/yyyy formats; some flowering time data are reported as Julian days.
- Metadata coverage includes: specimen identity, parental origins, experimental block and climate, measurement units (e.g., mg for seed weight, Julian days for flowering times), and data quality indicators (e.g., -9 for missing microsatellite data).

## Data quality, standards and governance considerations
- Standardization needs:
  - Ensure consistent date formats and units across all datasets.
  - Harmonize flowering time fields across 2012 and 2013 datasets and the common garden datasets (Julian days vs. calendar days as applicable).
  - Validate that Combi_Climate coding is consistently applied (C_C, C_D, D_C, D_D) across relevant datasets.
- Data quality notes:
  - Some metadata descriptions contain garbled text (notably in the 2012/2013 Day definitions), requiring verification against source records.
  - Microsatellite data use -9 to denote missing values; ensure consistent handling in analyses.
- Provenance and lineage:
  - Pedigree information relies on both known (Mat_Clone) and inferred (Pat_Clone with Prob) paternal assignments; maintain traceability to source datasets.
- Documentation needs:
  - Comprehensive metadata to accompany each dataset for discoverability, including data creator, collection context, and data use restrictions.

## Access, sharing and data governance considerations
- Data are structured for sharing within genetic, phenotypic, and ecological analyses; ensure proper data licensing and any embargo policies are respected.
- Data integration across multiple datasets requires disciplined versioning and linkage keys (Full_ID, Mat_Clone, Pat_Clone, Combi_Climate).
- Data stewardship tasks:
  - Maintain data provenance and cohort definitions (e.g., which seeds are F1 from which P0 parents).
  - Enforce metadata completeness and consistency checks.
  - Prepare data products for repository submission or portal upload with clear data use notes.

## Practical uses for data stewards
- Support discovery and reuse by ensuring datasets are discoverable via consistent naming, clear variable definitions, and linkages between pedigree, germination, reproductive, and flowering time data.
- Facilitate interoperability across analyses by standardizing core identifiers and climate treatment codes.
- Enable robust data quality assurance and version control to keep datasets up to date and correctly attributed.
- Assist researchers in performing integrated analyses of genetic, phenotypic, and climate-treatment effects on reproductive and flowering traits in Festuca ovina.