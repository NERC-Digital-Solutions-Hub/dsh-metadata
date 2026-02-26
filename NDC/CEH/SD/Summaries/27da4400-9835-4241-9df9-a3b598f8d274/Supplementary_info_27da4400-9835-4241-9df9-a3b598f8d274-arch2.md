# Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

- Purpose and scope
  - Provides genotype data for three freshwater macroinvertebrate species (Amphinemura sulcicollis, Isoperla grammatica, Baetis rhodani) collected in upland Wales, UK during 2012–2013.
  - Data accompanying the study on population genetics and demographic resilience; stored in the NERC Environmental Information Data Centre.

- Sample collection and on-site processing
  - Larval specimens collected by kick sampling and sorted to genus on site; stored in absolute ethanol.
  - Target: at least 20 individuals per species per site, with more collected to mitigate misidentification.
  - Laboratory identification to species level using established keys; samples stored: 2012 samples in ethanol, 2012–2013 samples also in ethanol or -80°C.

- DNA extraction methods (four methods used)
  - Method 1: High Pure PCR Template Preparation Kit (Roche) for blood and tissue.
  - Method 2: DNeasy 96 Blood and Tissue Kit (Qiagen) for higher throughput.
  - Method 3: Chelex 100 resin (Bio-Rad) for cost efficiency (tested on smaller subsets).
  - Method 4: Gentra Puregene Core Kit A (Qiagen) for later samples with varying success from Chelex.
  - Across species, counts of samples per method varied (e.g., A. sulcicollis: 27, 2, 173, 65 samples respectively for methods 1–4).

- Method validation and quality assurance
  - Some samples re-extracted with different methods to test for extraction method impact.
  - Genotypes compared to assess DNA quality; Na, Ho, He values reported to show limited impact of extraction method on results.

- Genotyping design
  - Loci: Amphinemura sulcicollis (10 loci), Isoperla grammatica (10 loci), Baetis rhodani (13 loci).
  - Baetis rhodani individuals were DNA-barcoded to remove cryptic species prior to genotyping.
  - Fragment analysis performed with ROX500 internal size standard; scoring done with Genemarker v1.91; allele sizes binned by hand.

- Data quality control and accuracy
  - Microsatellite loci exhibited high allelic diversity (A. sulcicollis 11–56 alleles; I. grammatica 38–72; B. rhodani 11–55).
  - Extensive QC steps due to many new loci and potential scoring errors:
    - Repeats to test scoring/binning accuracy; repeat scoring for ambiguous calls.
    - Validation of unique alleles; multiple repeats to minimize missing data.
    - Contamination checks via negatives and repeats; re-analysis until consensus; exclusion if unresolved.
    - Cross-order replication to ensure consistency across fragment analyses.

- Allele binning strategy
  - Automated binning (e.g., TANDEM) attempted but rejected due to errors (e.g., misclassifying heterozygotes as homozygotes).
  - Manual binning employed with:
    - Defined minimum and maximum allele lengths for each allele.
    - Checks to ensure heterozygotes are not binned as homozygotes.
    - Documentation of size ranges and inter-allele distances.
  - Binning rules and allele tables provided in dedicated Binning files.

- Data files and structure
  - Six CSV data files:
    - Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv (Baetis rhodani at 13 loci: B_1–B_5, B_7, Brh-1–Brh-7)
    - Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv (Amphinemura sulcicollis at 10 loci: Amp_2–Amp_6, Amp_8–Amp_11, Amp_13)
    - Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv (Isoperla grammatica at 10 loci: Iso_1–Iso_10)
  - Allele binning information files:
    - Binning_Baetis_rhodani_Hannah_Macdonald.csv
    - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
    - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
  - Data structure details:
    - Site, DURESS name, Year collected (2012 and 2013), Eastings, Northings, Altitude, Land-use, Catchment, Sample name (site + species initial + sample number), Extraction_method.
    - Per-locus columns include Repeats, Fails, Allele1, Allele2; missing data indicated by -9.
  - Extraction methods documented (1–4) per sample and included in the data tables.

- Related literature and references
  - Notes and references included for microsatellite development, data generation prior to microsatellite development, and methodological standards (e.g., GenAlEx), with links to relevant papers and theses for full detail.

- Accessibility and interoperability
  - Data organized to enable reuse and cross-study comparisons; aligned with standardised data formats and metadata (site names, coordinates in British National Grid, year, extraction method, and allele binning rules) to support environmental monitoring and population genetics analyses.