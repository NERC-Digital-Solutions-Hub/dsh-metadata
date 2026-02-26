# Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

## Overview
- Describes genotype data generation for three freshwater macroinvertebrates from upland Wales, UK (2012–2013).
- Data comprise final genotyping across multiple microsatellite loci for Amphinemura sulcicollis, Isoperla grammatica, and Baetis rhodani.
- Data are organized into six CSV files, including raw fragment analysis data and allele binning information; includes site metadata and extraction details.

## Sample collection
- Target: at least 20 individuals per species per site; more collected to account for misidentification.
- Collection method: kick sampling; specimens identified to genus on site and stored in absolute ethanol.
- Laboratory identification: species-level via established keys; 2012 samples also stored at -80°C.

## Extraction methods
- Four DNA extraction methods used (cost/availability considerations):
  - High Pure PCR Template Preparation Kit (Roche)
  - DNeasy 96 Blood & Tissue Kit (Qiagen)
  - Chelex 100 resin (Bio-Rad)
  - Gentra Puregene Core Kit A (Qiagen)
- Some samples were extracted twice with different methods to test method effects; comparisons showed only minor differences across methods.
- A subset of samples was re-extracted and genotyped to assess consistency (Na, Ho, He values indicated minimal method impact).

## Genotyping
- Genotyped at:
  - Amphinemura sulcicollis: 10 loci
  - Isoperla grammatica: 10 loci
  - Baetis rhodani: 13 loci
- Baetis rhodani individuals DNA-barcoded to remove cryptic species prior to genotyping.
- Fragment analysis performed (ROX500 internal size standard); scoring with Genemarker v1.91; allele sizes binned by hand.

## Data quality control
- Microsatellite loci exhibited high allelic diversity (A. sulcicollis 11–56; I. grammatica 38–72; B. rhodani 11–55), necessitating stringent QA.
- QA steps included:
  - Repeating samples that were ambiguous to score/bin.
  - Rechecking unique alleles to confirm true alleles and bin ranges.
  - Repeating failed samples to minimize missing data (minimum three repeats).
  - Including negatives and repeats in each fragment analysis order to detect contamination.
  - Re-scoring multiple times; resolving discrepancies; excluding unresolved samples.

## Binning alleles
- Allele binning required due to large allele counts (1,112 alleles total).
- Automated binning (TANDEM) attempted but failed in places (e.g., heterozygotes binned as homozygotes).
- Manual binning implemented with strict rules:
  - Set minimum/maximum allele lengths for each allele.
  - Ensure heterozygotes are not binned as homozygotes.
  - Validate bin limits with repeat checks; document size ranges and gaps between successive alleles.
- Binning rules and parameters are documented in dedicated Binning files.

## Data files (structure and contents)
- Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv
  - Final genotyping data for Baetis rhodani at 13 loci (B_1–B_5, B_7, Brh-1–Brh-7)
- Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv
  - Final genotyping data for Amphinemura sulcicollis at 10 loci (Amp_2–Amp_6, Amp_8–Amp_11, Amp_13)
- Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv
  - Final genotyping data for Isoperla grammatica at 10 loci (Iso_1–Iso_10)
- Allele binning information for each species:
  - Binning_Baetis_rhodani_Hannah_Macdonald.csv
  - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
  - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
- Data file structure notes:
  - Site descriptions reference Hannah Macdonald’s thesis and DURESS project entries.
  - Columns include Site, Description, Year collected, Eastings, Northings, Altitude, Land-use, Catchment, Name (sample identifier), Extraction_method.
  - For each species, per-locus columns include Repeats, Fails, Allele1, Allele2; missing data indicated by -9.
  - Allele binning tables map Microsatellite_code to allele sizes, with counts of unique alleles and ranges (Min(bp), Max(bp), Within, Between, Between_alleles).

## Data governance and reproducibility
- Quality control and replication procedures documented to ensure reliability and traceability.
- Multiple extraction methods and cross-method comparisons documented to assess methodological impact.
- Detailed allele binning rules and per-locus binning information provided to support transparent re-analysis.
- References to foundational literature and prior publications for microsatellite development and data interpretation are provided.

## Relevance for monitoring frameworks
- Demonstrates handling of complex, high-allelic-mityped genetic data within an environmental monitoring context.
- Illustrates comprehensive metadata capture (site, extraction method, coordinates, habitat context) and data provenance.
- Provides a model for QA/QC workflows, replication strategies, and rigorous binning to ensure data integrity in environmental health monitoring.
- Highlights practical challenges in data sharing and metadata completeness, relevant to governance considerations in monitoring frameworks.