# Daily photographs of paired phenotypic interactions between four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA

- Overview
  - Dataset of daily photographs capturing phenotypes from pairwise interactions among four Streptomyces strains (A, B, C, D) isolated from a Minnesota nature reserve.
  - Photographs correspond to metabolomics and RNA sampling data collected in parallel (LC-MS and RNA sampling; MS submission ongoing).
  - Context: strains previously isolated from Cedar Creek Ecosystem Science Reserve; related to a study on resource use by soilborne Streptomyces.

- Data Collected and Formats
  - Image data: unedited .jpg photographs.
  - Image metadata included: resolution 4000 x 3000 pixels; focal length 5 mm.
  - Temporal notes: images taken daily from days 2 to 6 post inoculation (with day 1 defined as 24 hours post inoculation).

- File Organization and Naming Convention
  - All image files exist in a single folder.
  - Naming scheme: D_L_R_N_I.jpg
    - D = day (2–6)
    - L = left-hand strain (A, B, C, or D)
    - R = right-hand strain (A, B, C, or D)
    - N = biological replicate number
    - I = technical image replicate number

- Experimental Design and Sampling
  - Culture preparation:
    - Spores standardized to 1 x 10^9 CFU/mL in 20% glycerol; diluted to 1 x 10^8 CFU/mL in ISP2 broth.
    - 4 µL inoculated 1 cm apart in pairs on ISP2 agar; each pairing prepared in quadruplicate for each timepoint (n = 20 per pairing).
  - Sampling plan:
    - Quadruplicate plates per pairing/timepoint, enabling destructive daily sampling for metabolomics and RNA in triplicate (plus one spare).
    - One set of quadruplicate plates chosen at random for daily photography; same four plates imaged to capture phenotypes across timepoints.
    - Photos taken daily on days 2–6; sampling for LC-MS/RNA is destructive.

- Imaging Protocol and Equipment
  - Photos captured in a class II biosafety cabinet.
  - Plates aligned to the same position using reference markings to ensure consistency.

- Reproduction, Identity Verification, and Provenance
  - Strain identity verified by PCR and Sanger sequencing of 16S rRNA genes (primers 27F and 1492R).
  - Context and provenance tied to the Cedar Creek Ecosystem Science Reserve isolates and the related Microbial Ecology publication (Schlatter et al., 2013).

- Temporal Coverage and Replicates
  - Biological design: n = 20 replicates for imaging-related dataset (to support destructive daily sampling in metabolomics/RNA studies).
  - Photographic dataset: n = 4 biological replicates; each plate imaged 4–5 times per timepoint (I = technical replicate).

- Quality Control and Data Provenance
  - Dataset considered complete to at least biological triplicate for most timepoints.
  - Day 6 data: some pairings used for LC-MS sampling, reducing photomicrograph replicates to biological triplicate for that day.
  - Naming scheme preserves linkage of each image to its corresponding Day, Strain pair, Biological replicate, and Technical replicate.

- Potential Uses and Data Support Considerations
  - Enables exploration of inter-strain interaction phenotypes and correlation with metabolomics data (LC-MS) and transcriptomics (RNA) across days 2–6.
  - Useful for building self-serve data products (e.g., dashboards or visualization tools) to compare phenotypes across strain pairs and timepoints.
  - Clear, consistent naming and provenance support data integration with other datasets; practitioners should account for day-6 data gaps due to destructive sampling.

- Limitations and Considerations for Data Support
  - Day 6 phenotypic images are incomplete for some pairings due to LC-MS destructive sampling.
  - Data are unedited images; users should consider potential variation in imaging conditions across plates, though alignment efforts mitigate this.
  - The dataset is paired with ongoing mass spectrometry data submission; availability may depend on MS data release status.