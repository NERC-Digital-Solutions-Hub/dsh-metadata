# Experimental design/sampling method

## Overview
- Tracks changing chemical profiles of Maculinea rebeli caterpillars across region and ant-host interactions.
- Sampling timeline: uncontaminated pre-adoption final instars → six weeks with ants → isolation from ants for 5 days to allow semio-chemical dissipation and caterpillar secretions.
- Data collected as hexane surface chemical extracts analyzed by GC-MS; results stored as a CSV dataset with detailed metadata.

## Sampling design and cohorts
- Sample types and stages:
  - (i) Unparasitized ants (Myrmica schencki and M. sabuleti) from Spain/Pyrenees and Poland; naïve French ants with no Maculinea rebeli experience. n = 5 workers from 5 nests per locality.
  - (ii) Eight batches per region of pre-adoption final instar M. rebeli larvae sampled after leaving Gentiana cruciata, before contact with ants. n = 5 larvae per batch; total 40 larvae for each larval type.
  - (iii) M. rebeli larvae after six weeks with naïve French ants. n = 5 (Spain+schencki and Poland+sabuleti); n = 3 (Spain+sabuleti and Poland+schencki).
  - (iv) As in (iii), but larvae isolated from ants and kept unfed, singly, for 5 days. n = 5 (Spain+schencki), n = 4 (Poland+schencki), n = 3 (Spain+sabuleti and Poland+sabuleti).
- Chemical material analyzed: hexane extracts of surface chemicals from each sample type and condition.
- Regions and host-ant combinations cover multiple country origins and ant species (sabuleti and schencki) to assess regional and host effects.

## Analytical workflow and quality assurance
- Analytical method: Gas chromatography–mass spectrometry (GC-MS) with a HP 5890II GC and HP 5971A MSD; ultra-high purity helium as carrier gas.
- Mass spectrometry: Full scan mode from 40 to 600 m/z; mass spectral data used for peak identification.
- Peak identification and quantification:
  - Initial hydrocarbon screening via ion m/z 57.
  - Quantification by integrating peak areas; convert to Equivalent Chain Length (ECL) using alkane standards (n-C20 to n-C36).
  - Peaks of interest identified by ECL and full-scan spectra aligned with NIST-97/08 database.
  - Exclude column bleed, siloxanes, and phthalate plasticizers (identified by characteristic m/z 149).
  - For analysis, express each peak area as a proportion of the total peak area in the chromatogram.
- Data quality checks: chromatograms inspected for interferences; ensure peaks are chromatographically distinct and symmetrical.

## Data format and column labeling
- Data format: CSV text file.
- Column labeling conventions:
  - Example sample label: Rebeli_sab_0_ES_1141 (Maculinea rebeli reared with Myrmica sabuleti; Spain; sample number 1141).
  - Other examples cover country origin, ant association, and sample sequence (e.g., Rebeli_sab_5_ES_1155 indicates a sample after 5 days isolation with Spain origin).
  - Extensive list includes samples from different country/ant combinations (Spain, Poland, France) and developmental/experimental stages (pre-adoption, post-6 weeks with ants, post-isolation).
- Explanation column: Each row includes a descriptive field detailing the sample (origin, ant host, developmental stage, sample number, etc.) to enable interpretation and cross-referencing.

## Data processing and potential products
- Processed data elements:
  - Peak areas converted to proportions of total peak area per chromatogram.
  - Equivalent Chain Length (ECL) positions used for tentative identifications.
- Potential data products for end users:
  - Self-serve exploration of chemical profiles by region, ant species, larval stage, and post-treatment condition.
  - Comparisons of hydrocarbon profiles across host ants and geographic origins.
  - Reusable CSV dataset with accompanying metadata to support downstream analyses.

## Practical considerations for Data Support
- Complex, multi-factor design requiring careful merging of metadata (origin, ant species, larval type, treatment stage) with chemical profiles.
- Data dictionary and consistent labeling are essential to enable robust cross-dataset analyses and re-use.
- Ensure documentation includes interpretation guidance for the Explanation field and how to map sample labels to experimental conditions.
- Be mindful of potential formatting inconsistencies in the long sample-label list when integrating with other data sources.