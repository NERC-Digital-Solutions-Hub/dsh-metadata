# Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

## Overview
- Describes supplementary information and data resources for fragment analysis raw data of three freshwater macroinvertebrates from upland Wales, UK (2012–2013).
- Focuses on genotyping data, extraction method comparisons, allele binning, data quality control, and metadata for interpretation and reuse.

## Sampling and collection
- Larval specimens collected by kick sampling and identified to genus on site; stored in absolute ethanol.
- Aim: at least 20 individuals per species per site, often more to mitigate misidentification in the field.

## Extraction methods
- Four DNA extraction methods used due to cost and availability:
  1) High Pure PCR Template Preparation Kit (Roche)
  2) DNeasy 96 Blood and Tissue Kit (Qiagen)
  3) Chelex 100 resin (Bio-Rad)
  4) Gentra Puregene Core Kit A (Qiagen)
- Sample counts per species by method provided (A. sulcicollis, I. grammatica, B. rhodani).
- Validation: some samples were extracted twice with different methods; genotypes compared to check equivalence.
- Post-genotyping, representative samples from various sites were compared across extraction methods using Na, Ho, and He (GenAlEx). All three species showed minimal differences, indicating extraction method had limited impact on results.

## Genotyping
- Loci per species: A. sulcicollis (10 loci), I. grammatica (10 loci), B. rhodani (13 loci).
- B. rhodani individuals DNA-barcoded to remove cryptic species.
- Fragment analysis performed by Dundee Biosciences; ROX500 used as internal size standard.
- Allele sizes binned manually after scoring with Genemarker v1.91.

## Data quality control
- Microsatellite loci exhibited very high allele counts (A. sulcicollis 11–56; I. grammatica 38–72; B. rhodani 11–55), requiring extensive QC.
- QC steps included:
  - Repeated scoring on repeatedly problematic loci
  - Re-reading and confirming unique alleles
  - Repeating failed samples (minimum three repeats)
  - Including negatives and repeats in each fragment analysis order to detect contamination
  - Multiple scoring rounds with discrepancies resolved or samples excluded if consensus could not be reached

## Binning alleles
- Automated binning (TANDEM) attempted but errors occurred (e.g., heterozygotes misclassified as homozygotes).
- Manual binning employed due to dataset size (1,112 alleles) and accuracy needs.
- For each microsatellite, a set of rules established for allele size (min/max bp) to prevent misbinning of heterozygotes.
- Recorded allele size ranges and gaps between adjacent alleles; binning rule tables are provided in the corresponding Binning files.

## Data files
- Six CSV data resources:
  - Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv (Baetis rhodani; 13 loci)
  - Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv (Amphinemura sulcicollis; 10 loci)
  - Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv (Isoperla grammatica; 10 loci)
  - Binning_Baetis_rhodani_Hannah_Macdonald.csv
  - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
  - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
- Fragment_analysis_rawdata files include per-sample fields such as Site, Year collected, Eastings/Northings, Altitude, Land-use, Catchment, Sample Name, Extraction_method, plus per-locus columns: Repeats, Fails, Allele1, Allele2.
- Allele columns use -9 to indicate missing data; locus-specific columns are grouped by species (e.g., Iso_1_Repeats, Amp_1_Allele1, etc.).
- Binning files describe microsatellite code, allele counts, and binning ranges (Min(bp), Max(bp), Within, Between, Between_alleles).

## Further reading / References
- Foundational works and prior development related to this dataset:
  - Macdonald, H. C., Cunha, L., and Bruford, M. W. (2016). Development of genomic resources for four potential environmental bioindicator species.
  - Macdonald, H. C., Ormerod, S. J., and Bruford, M. W. (2016). Enhancing capacity for freshwater conservation at the genetic level.
  - Macdonald, H. C. (2016). Population genetics and demographic resilience in three aquatic invertebrates (PhD thesis).
  - Dewoody et al. (2006); Elliott et al. (1988); Holland & Parson (2011); Hynes (1977); Matschiner & Salzburger (2009); Peakall & Smouse (2012); Williams et al. (2002).