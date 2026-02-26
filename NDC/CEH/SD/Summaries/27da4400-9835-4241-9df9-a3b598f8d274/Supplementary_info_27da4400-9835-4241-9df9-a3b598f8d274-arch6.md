# Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

- Purpose and scope
  - Provides supplementary data accompanying genotype data for three freshwater macroinvertebrate species from upland Wales, UK (2012–2013).
  - Documents sample collection, DNA extraction, genotyping, data quality control, allele binning, and data file structure to support reuse and reanalysis.

- Sample collection
  - Species: Amphinemura sulcicollis, Isoperla grammatica, Baetis rhodani.
  - Method: Kick sampling; on-site genus-level sorting; stored in absolute ethanol (2012 samples also stored at -80°C).
  - Sampling target: At least 20 individuals per species per site (often more to mitigate misidentification).
  - Laboratory identification: Species-level confirmation using Elliott et al. (1988) and Hynes (1977).

- DNA extraction methods used
  - Four extraction methods employed due to cost and availability:
    1) High Pure PCR Template Preparation Kit (Roche) – used across species with counts: A. sulcicollis 27, I. grammatica 2, B. rhodani 175.
    2) DNeasy 96 Blood & Tissue Kit (Qiagen) – A. sulcicollis 173, I. grammatica 190.
    3) Chelex 100 resin (Bio-Rad) – A. sulcicollis 13, I. grammatica 5.
    4) Gentra Puregene Core Kit A (Qiagen) – A. sulcicollis 65, I. grammatica 40, B. rhodani 11.
  - Quality control across methods: selected samples were re-extracted with different methods to ensure comparability; overall extraction method had limited impact on results (comparable Na, Ho, He across methods).

- Genotyping
  - Loci: A. sulcicollis (10 loci), I. grammatica (10 loci), B. rhodani (13 loci).
  - Paternity: B. rhodani individuals DNA-barcoded to remove cryptic species.
  - Process: Fragment analysis (Dundee Biosciences) with ROX500 internal size standard; data scored with Genemarker v1.91; allele sizes binned by hand.

- Data quality control and consistency checks
  - Loci diversity: A. sulcicollis (11–56 alleles), I. grammatica (38–72), B. rhodani (11–55); high allele counts required rigorous QC.
  - QC steps:
    - Use of many repeats to verify scoring/binning accuracy.
    - Re-sequencing/re-running ambiguous samples.
    - Verification of unique alleles; re-checking binning ranges.
    - Repeated failed samples (minimum three repeats) to reduce missing data.
    - Inclusion of negatives and repeats in every fragment analysis order to detect contamination.
    - Multiple scoring passes per project; discrepancies resolved via re-analysis; unresolved cases excluded.

- Allele binning
  - Challenge: Automated binning (e.g., TANDEM) caused errors (e.g., heterozygotes binned as homozygotes).
  - Approach: Manual binning with allele-specific rules.
  - Basis: For each microsatellite, specimen-specific minimum/maximum bp limits defined; ensured heterozygotes not misclassified as homozygotes.
  - Documentation: Binning rules per microsatellite recorded in dedicated Binning files.

- Data files and structure
  - Data resources consist of six CSV files:
    - Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv (Baetis rhodani at 13 loci)
    - Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv (A. sulcicollis at 10 loci)
    - Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv (I. grammatica at 10 loci)
    - Binning_Baetis_rhodani_Hannah_Macdonald.csv
    - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
    - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
  - Structure of the raw data files:
    - Site; DURESS site description; Year collected (2012/2013); Eastings; Northings; Altitude (m); Land-use; Catchment; Name (sample identifier combining site, genus initial, and sample number); Extraction_method.
    - For each microsatellite: Repeats; Fails; Allele1; Allele2.
    - '-9' denotes missing data.
  - Binning files contain: Microsatellite_code; N (unique alleles); Min(bp); Max(bp); Allele; No.alleles; Within(bp); Between; Between_alleles; plus related counts and ranges.

- Related reading and references
  - Key prior work on data generation and microsatellite development cited for context and methods (development of genomic resources, microsatellite development, and statistical tools such as GenAlEx).

- Notes on data provenance and usage
  - Links to related papers and theses provide methodological context and full details on microsatellite development and population genetics analyses.
  - Data are organized to enable reanalysis, cross-method comparison, and reuse for end-user analyses or integration with broader ecological or conservation studies.