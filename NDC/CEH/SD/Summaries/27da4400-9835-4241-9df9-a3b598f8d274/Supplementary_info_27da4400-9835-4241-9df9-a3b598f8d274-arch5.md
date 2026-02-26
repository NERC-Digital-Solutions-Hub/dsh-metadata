# Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

## Overview
- Supplementary information accompanying genotype data for three freshwater macroinvertebrates collected in upland Wales, UK (2012-2013).
- Data deposited in the NERC Environmental Information Data Centre; includes fragment analysis raw data and allele binning information.
- Document provides detailed methods, quality control, and data structure to enable reuse and reproducibility.

## Sample collection and specimen handling
- Larval specimens collected by kick sampling; identified to genus on site and stored in absolute ethanol (2012 samples also stored at -80°C).
- Target: at least 20 individuals per species per site; more collected to account for misidentifications.
- Laboratory identification to species level using established keys; specimens stored accordingly.

## DNA extraction methods
- Four extraction methods used due to cost and availability:
  1) High Pure PCR Template Preparation Kit (Roche) – used for initial extractions.
  2) DNeasy 96 blood and tissue kit (Qiagen) – bulk extraction, enabling 96 samples per run.
  3) Chelex 100 resin (Bio-Rad) – cost-effective for small tests.
  4) Gentra Puregene Core Kit A (Qiagen) – used for later samples when Chelex varied in performance.
- Sample counts per method varied by species.
- Cross-method validation: some samples were extracted twice with different methods; genotypes compared to assess impact. Na, Ho, and He were compared across methods with GenAlEx; results showed narrow ranges, indicating minimal method impact on results.

## Genotyping and data processing
- Genotyping conducted at:
  - Amphinemura sulcicollis: 10 loci
  - Isoperla grammatica: 10 loci
  - Baetis rhodani: 13 loci
- Prior to genotyping, Baetis rhodani individuals were DNA-barcoded to remove cryptic species.
- Fragment analysis performed (Dundee Biosciences, UK) with ROX500 internal size standard.
- Allele sizes scored using Genemarker v1.91; binning performed by hand due to high allele counts.

## Data quality control
- Microsatellite loci exhibited very high allele counts (A. sulcicollis 11–56; I. grammatica 38–72; B. rhodani 11–55), necessitating rigorous QC.
- QC steps included:
  - Repeating ambiguous scores and unique alleles to confirm true alleles and bin ranges.
  - Repeating failed samples at least three times to minimize missing data.
  - Including negatives and repeats in each fragment analysis order to detect contamination and order-specific differences.
  - Multiple scoring rounds with investigations of discrepancies, often resulting in updated scoring rules.
  - Exclusion of samples if consensus could not be achieved after re-analysis.

## Binning of alleles
- Automated binning with TANDEM was attempted but produced errors (e.g., heterozygotes binned as homozygotes).
- Manual binning was used to ensure accuracy:
  - Establishment of per-allele rules with minimum and maximum bin ranges in base pairs.
  - Verification that heterozygotes are not binned as homozygotes.
  - Documentation of allele size ranges, and differences between adjacent alleles.
- Allele binning rules are documented in species-specific Binning files.

## Data files and structure
- Data resource consists of six CSV files:
  - Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv (Baetis rhodani; 13 loci)
  - Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv (Amphinemura sulcicollis; 10 loci)
  - Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv (Isoperla grammatica; 10 loci)
  - Binning_Baetis_rhodani_Hannah_Macdonald.csv
  - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
  - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
- Fragment_analysis_rawdata files structure:
  - Each locus data stored per microsatellite with columns for Repeats, Fails, Allele1, Allele2 (per locus), using suffixes corresponding to species (Iso_, Amp_, Brh_).
  - -9 indicates missing data.
  - Sample identifiers combine site, species, and individual number (e.g., 93A4).
  - Extraction_method indicates which of the four extraction methods was used (1–4).
- Binning files describe per-locus binning rules:
  - Microsatellite_code, N, Min(bp), Max(bp), Allele, No.alleles, Within(bp), Between, Between_alleles, etc.
- Site metadata included in data tables:
  - Site names, DURESS names, collection years (2012, 2013), Eastings, Northings, Altitude, Land-use, Catchment, and unique sample Name codes.

## Provenance and references
- Related methodological references and prior work for microsatellite development and analysis are provided, including:
  - Macdonald et al. (2016, 2016) on genomic resources and microsatellite development
  - Williams et al. (2002) on microsatellite loci for Baetis rhodani
  - Dewoody et al. (2006), GenAlEx (Peakall & Smouse, 2012), TANDEM (Matschiner & Salzburger, 2009)
  - Foundational keys and ecological references used for species identification (Elliott et al. 1988; Hynes 1977)
- Additional reading includes Macdonald (2016) PhD thesis detailing data generation and broader context.