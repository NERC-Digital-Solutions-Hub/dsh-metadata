# Daily photographs of paired phenotypic interactions between four strains of Streptomyces bacteria isolated from a nature reserve in Minnesota, USA

## Overview
- Dataset comprises photographs of four interacting Streptomyces strains in pairwise cultures, captured days 2 through 6 post inoculation.
- Images correspond to a larger study with mass spectrometry data being submitted concurrently.
- Strains were previously isolated from Cedar Creek Ecosystem Science Reserve, Minnesota; related to a 2013 Microbial Ecology study.
- File format: unedited .jpg images; resolution 4000 x 3000; focal length 5 mm.
- Images are stored in a single folder and named using the convention D_L_R_N_I.jpg, where D = day, L/R = left/right strains (A, B, C, D), N = biological replicate, I = technical image replicate.

## Dataset structure and sampling design
- Experimental setup: pairs of four Streptomyces strains cultured on ISP2 agar with standardized inocula; four plates per pairing per timepoint (quadruplicate) for MS and RNA sampling in triplicate; one set of quadruplicate plates photographed daily.
- Temporal scope: daily imaging from day 2 to day 6 after inoculation (day 1 is the baseline).
- Technical replication: each plate imaged 4–5 times per timepoint (I in the naming scheme).
- Biological replication for the included photo dataset: n = 4; overall planned sampling for related analyses includes n = 20 per pairing (for MS).
- Note: on day 6, some plates were used for LC-MS sampling, reducing phenotypic imaging to biological triplicate for those cases.

## Quality control and data provenance
- Strain identity verified by PCR and Sanger sequencing of 16S rRNA gene (primers 27F and 1492R).
- Imaging conducted in a class II biosafety cabinet with consistent positioning based on reference markings.
- Phenotypic photos aligned with the same four plates across early timepoints; sampling is destructive for some timepoints, hence the need for prioritized plate selection.
- Documentation captures the complete experimental design for the included dataset; day 6 observations may differ due to destructive sampling.

## Data governance and stewardship considerations
- Metadata and standards
  - Ensure metadata fields capture: D, L, R, N, I, date of imaging, plate identifiers, and linking to the corresponding MS/RNA sampling data.
  - Record experimental conditions: ISP2 composition, inoculation method, plate format, and replication scheme.
- Data availability and access
  - Mass spectrometry data submission is ongoing; coordinate release of image data with MS data to maintain data integrity and provenance.
  - Images are high-resolution; consider storage and transfer capabilities when sharing (folder structure and naming consistency are essential).
- Data quality and interoperability
  - Maintain consistent naming convention (D_L_R_N_I.jpg) and folder organization to enable programmatic linking to MS/RNA datasets.
  - Include a data access note describing any temporary embargoes or publication plans related to the accompanying MS data.
- Documentation and provenance
  - Provide a dataset-level readme detailing experimental workflow, QC steps, and how images relate to other datasets (e.g., MS, RNA).
  - Maintain traceability between days, biological replicates, and corresponding image captures to support reproducibility.

## Relevance to Data Stewardship aims
- Demonstrates strong data governance through clear naming conventions, comprehensive metadata capture potential, and linkage to complementary datasets.
- Shows attention to data quality, provenance, and the need to coordinate updates as related data (MS) are finalized and shared.
- Highlights practical challenges such as completing metadata for complex multi-replicate experiments and ensuring timely data availability across coupled data streams.