Supplementary information for Fragment analysis raw data for three freshwater macroinvertebrates, Amphinemura sulcicollis , Isoperla grammatica and Baetis rhodani

## Overview
- Supplement providing raw fragment analysis data for three freshwater macroinvertebrates: Amphinemura sulcicollis, Isoperla grammatica, and Baetis rhodani.
- Data originate from upland Wales, UK (2012–2013) and are archived in the NERC Environmental Information Data Centre.
- Includes genotyping data at multiple microsatellite loci, extraction methods, and data quality control procedures.
- Aims to support spatially informed analyses by linking genetic data to sampling sites and environmental context.

## Spatial and sampling metadata
- Sampling sites include Eastings and Northings in the British National Grid (EPSG: 27700).
- Each sample is associated with site-level metadata: site name, year collected, altitude, land-use, catchment.
- Unique sample naming combines site identifier and species/genus, enabling clear spatial linkage for GIS workflows.

## Sampling and specimen processing
- Kick sampling used to collect larval specimens.
- Field identification to genus level (e.g., Baetis for Baetis rhodani) with laboratory confirmation to species level.
- Specimens stored in absolute ethanol; 20 individuals per species per site targeted (often more to buffer misidentifications).

## DNA extraction methods
- Four extraction methods used due to cost and availability:
  1) High Pure PCR Template Preparation Kit
  2) DNeasy 96 Blood & Tissue Kit
  3) Chelex 100 resin (cost-effective)
  4) Gentra Puregene Core Kit A
- Species-specific counts: A. sulcicollis, I. grammatica, B. rhodani (method usage detailed per species).
- Method comparisons showed minimal impact on results; some samples re-extracted to verify consistency.

## Genotyping and data processing
- Genotyping at: A. sulcicollis (10 loci), I. grammatica (10 loci), B. rhodani (13 loci).
- DNA barcoding used on B. rhodani to exclude cryptic species.
- Fragment analysis performed with ROX500 internal size standard; scoring with Genemarker; allele sizes binned by hand.

## Data quality control (QC)
- Loci exhibited high numbers of alleles, increasing scoring difficulty.
- QC steps to ensure accuracy:
  - Frequent repeats to validate scoring/binning.
  - Re-testing ambiguous samples.
  - Repetition of unique alleles to confirm true alleles.
  - Re-scoring failed samples (minimum three repeats to reduce missing data).
  - Inclusion of negatives and repeats within each fragment analysis order to detect contamination.
  - Multiple scoring passes; discrepancies resolved via consensus; unusable samples excluded if no consensus.

## Allele binning (manual)
- Automated binning (e.g., TANDEM) found to be unreliable for this dataset; manual binning used for accuracy.
- For each microsatellite, established rules with minimum/maximum allele lengths to define unique alleles.
- Ensured heterozygotes were not misclassified as homozygotes.
- Allele binning rules are documented in dedicated Binning files per locus.

## Data files and structure
- Six CSV data files in total:
  - Fragment_analysis_rawdata_Baetis_rhodani_Hannah_Macdonald.csv
  - Fragment_analysis_rawdata_Amphinemura_sulcicollis_Hannah_Macdonald.csv
  - Fragment_analysis_rawdata_Isoperla_ grammatica_Hannah_Macdonald.csv
  - Binning_Baetis_rhodani_Hannah_Macdonald.csv
  - Binning_Amphinemura_sulcicollis_Hannah_Macdonald.csv
  - Binning_Isoperla_ grammatica_Hannah_Macdonald.csv
- FragmentAnalysis CSV structure:
  - Core site metadata: Site, DURESS name, Year collected, Eastings, Northings, Altitude(m), Land-use, Catchment, Name, Extraction_method.
  - For each microsatellite: Repeats, Fails, Allele1, Allele2 (with -9 indicating missing data).
- Binning CSV structure:
  - Microsatellite_code, N (number of unique alleles), Min(bp), Max(bp), Allele, No.alleles, Within(bp), Between, Between_alleles.
  - Provides per-locus binning rules and allele definitions.

## How this data supports GIS workflows
- Enables mapping of genetic diversity and structure across sampled catchments and landscapes.
- Facilitates integration with environmental layers (land-use, altitude, river networks) for spatial analyses.
- Coordinate and site metadata enable spatial joins, hotspot detection, and visualization of genetic variation on maps.
- Clear documentation of sampling design, extraction methods, and QC supports reproducibility in GIS-driven analyses.

## Additional information and references
- Context and methods linked to per-species microsatellite development and population genetics work (Macdonald et al. 2016; Macdonald 2016; related papers on microsatellite loci and binning tools like TANDEM).
- Data intended for reuse with appropriate acknowledgment of original authors and data centre hosting (NERC EIDC).