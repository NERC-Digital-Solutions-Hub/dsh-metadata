# Data collected on Mt Etna during the field transplant in 2017

## Overview of the study design
- Field transplant experiment conducted on Mt Etna in 2017.
- Five genotypes randomly chosen for each of two species.
- For each genotype, four cuttings measured at each transplant elevation.
- Four leaves measured per plant.
- Measurements for all plants repeated on a second day to account for weather and measurement timing.
- After 30 minutes of dark adaptation, light response measurements recorded with an IMAGING-PAM M-series chlorophyll fluorometer.

## Data schema and key variables
- Species: two Senecio species (AE = S. aethnensis; CH = S. chrysanthemifolius).
- Genotype: genotype ID from individuals grown in the glasshouse from which cuttings were taken.
- TGSite: elevation of the transplant sites.
- TGBlock: replicate experimental blocks in the field.
- Grid: grid location of plants within each block (genotype randomized to grid locations).
- Day: day measurements were taken.
- Columns 7-22: fluorometer outputs; PI(total) is the primary metric used in analysis as it represents total photosynthetic capacity; other fluorometer outputs exist but PI(total) was the focus.

## Measurement methodology and timing
- Chlorophyll fluorescence measured with IMAGING-PAM fluorometer.
- Measurements followed 30 minutes of dark adaptation.
- Data collected per plant across multiple leaves and cuttings, with replication on a second day.

## Data processing and usage
- Primary analysis uses PI(total) as the key variable for photosynthetic capacity.
- The dataset includes additional fluorometer outputs (columns 7-22) that could be used for further analyses if needed.

## Data management and governance considerations
- Experimental design includes clear structuring by species, genotype, blocks, grid locations, and day, facilitating traceability and reproducibility.
- Metadata captured includes site elevation, block replication, and randomization schema.
- While PI(total) is the primary analytic focus, retaining full fluorometer outputs enables broader future analyses.

## Implications for data leadership
- Demonstrates end-to-end data handling: from experimental design and specimen replication to structured data capture and primary metric selection.
- Highlights the importance of comprehensive metadata (species, genotype, location, replication, timing) to support data discoverability, quality, and reuse.
- Illustrates how to balance immediate analytic needs (PI(total)) with maintaining access to richer measurement data for potential future analyses.