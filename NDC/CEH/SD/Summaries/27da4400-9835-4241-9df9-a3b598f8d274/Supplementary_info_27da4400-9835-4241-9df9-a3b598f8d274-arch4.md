# Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

## Overview
- Supplementary information accompanying genotype data for three freshwater macroinvertebrates from upland Wales, UK (2012–2013).

## Sample collection
- Larval specimens collected by kick sampling; identified to genus on site and to species in the lab; stored in absolute ethanol (2012 samples also stored at -80°C).
- Target: at least twenty individuals per species per site; often more to account for field misidentification.

## Extraction methods
- Four extraction methods used due to cost/availability:
  1) High Pure PCR Template Preparation Kit (Roche)
  2) DNeasy 96 blood and tissue kit (Qiagen)
  3) Chelex® 100 resin (Bio-Rad)
  4) Gentra Puregene Core Kit A (Qiagen)
- Sample counts per method vary across species (e.g., A. sulcicollis: 27, 173, 13, 65; I. grammatica: 2, 190, 5, 40; B. rhodani: not all methods used equally).
- Method effects tested by extracting some samples with multiple methods; genotypes compared; statistical checks (Na, Ho, He) showed minimal impact of extraction method.

## Genotyping
- Genotyped at 10 loci (A. sulcicollis), 10 loci (I. grammatica), and 13 loci (B. rhodani).
- B. rhodani individuals DNA-barcoded to remove cryptic species.
- Fragment analysis conducted; ROX500 internal size standard; allele sizes scored and binned manually using Genemarker v1.91.

## Data quality control
- High allelic diversity observed (A. sulcicollis 11–56; I. grammatica 38–72; B. rhodani 11–55), requiring extensive QC.
- QC steps included: repeated scoring for repeats, re-running ambiguous samples, validating unique alleles, re-running failed samples, including negatives/repeats to detect contamination, multiple scoring passes, resolving discrepancies, and excluding samples with unresolved consensus.

## Binning alleles
- Manual binning implemented due to large allele counts; automated binning with TANDEM proved unreliable.
- Established per-locus rules: minimum and maximum bp for each allele; ensure heterozygotes not binned as homozygotes; documented allele size ranges and bin boundaries in dedicated “Binning” files.

## Data files
- Six CSV data files:
  - Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv (Baetis rhodani; 13 loci)
  - Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv (A. sulcicollis; 10 loci)
  - Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv (Isoperla grammatica; 10 loci)
  - Allele binning information:
    - Binning_Baetis_rhodani_Hannah_Macdonald.csv
    - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
    - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
- Each data file contains per-sample columns (Sample, Site, Year, coordinates, altitude, land-use, catchment, name, extraction method) plus per-locus columns (Repeats, Fails, Allele1, Allele2). Missing data denoted by -9.
  
## Binning files
- Provide per-microsatellite binning details:
  - Microsatellite_code, N, Min(bp), Max(bp), Allele, No.alleles, Within(bp), Between, Between_alleles.

## Further reading
- References to related data generation and microsatellite development papers:
  - Macdonald et al. 2016 (bioRxiv 046227)
  - Macdonald et al. 2016 (Aquatic Conservation)
  - Macdonald (2016) PhD thesis
  - Williams et al. 2002; Dewoody et al. 2006; Holland & Parson 2011; Elliott et al. 1988; Hynes 1977

## References
- Citations for methodologies and tools used (GenAlEx, TANDEM, GenMarker, scoring practices, and microsatellite development).