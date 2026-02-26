# readme for soil populations - IGTE_counts.csv

- The document is a data dictionary and workflow guide for the IGTE_counts.csv file, detailing how soil bacterial population data are collected, annotated, and calculated across treatments, species, and timepoints.
- It defines each field, the experimental design, and how colony counts are converted to CFU per millilitre for standardized analysis and monitoring.

## Data structure and field definitions

- Treatment: describes initial plasmid status and mercury exposure
  - A.Hg compensated plasmid + mercury
  - B wild-type plasmid, no mercury
  - B.Hg wild-type plasmid + mercury
  - C no plasmid, no mercury
- Replicate: biological replicate identifier (1–6) for each treatment
- Transfer: evolution timepoint (0 = start, 30 = end)
- Bacteria: species associated with the count, determined by plating media
  - P. fluorescens (SBW25)
  - P. putida (KT2440)
- Marker: detected version of the target
  - All: total count for the species
  - HgR: mercury resistance detected on plasmid bearers or via chromosomal capture (PCR later)
  - KmR: kanamycin resistance (used only for P. putida to detect transfer of Tn6291 via pQBR57)
- Media: selective additives used to detect specific species/markers; concentrations reduced over time due to adaptation
  - Examples include Gm30, Gm30Hg20, Sm250, Sm250Hg20, Sm250Km50, Gm6, Gm6Hg20, Sm125, Sm125Hg20, Sm125Km25, Sm50, Sm50Hg20, Sm50Km10
- Volume: volume plated (μl)
- Dilution: dilution factor plated (e.g., 10^-x)
- Count: number of colonies observed on the plate
- CFU_ml: colony-forming units per millilitre, calculated from count, dilution, and volume
  - Formula (as provided): CFU_ml = (count × 10^(-dilution)) / (volume × 10^(-3)) 
  - Equivalently, CFU_ml = count × 10^dilution × 1000 / volume

## Experimental design and scope

- Biological design:
  - Each treatment includes 6 independent replicates
  - Two timepoints: start (0) and end (30) of evolution
  - Two target bacterial species measured by selective plating
- Treatments capture:
  - Plasmid status: compensated plasmid (pQBR57_0059 KO) vs wild-type plasmid vs no plasmid
  - Mercury exposure: presence or absence of mercury in soil (16 μg/g)
- Markers and detection:
  - All markers provide total species counts
  - HgR and KmR markers enable detection of mercury resistance and kanamycin resistance, respectively
  - KmR is specific to P. putida to monitor transfer events involving Tn6291 via pQBR57
- Media and selective pressures:
  - Media compositions combine antibiotics and mercury to isolate and identify specific strain-marker combinations
  - Antibiotic/mercury concentrations are gradually reduced over time to reflect adaptation

## Data processing and interpretation

- Counts are converted to CFU/ml using the specified formula to allow direct comparison across samples, treatments, and timepoints.
- Media choices and markers enable tracking of:
  - How plasmid carriage and mercury exposure affect population dynamics
  - The spread of resistance determinants (HgR, KmR) within and between species
- End users can compare changes over time (0 vs 30) and across treatments to assess environmental health and the impact of management or exposure scenarios.

## Relevance to environmental monitoring aims

- Provides a standardized dataset that can be used to assess environmental health and policy performance over time.
- The structured data dictionary supports quality assurance, reproducibility, and integration with other environmental datasets.
- Emphasizes the importance of making underlying data accessible and reusable for broader analyses and external scrutiny.

## Data management and accessibility considerations

- The dataset is organized to facilitate storage and upload to appropriate data portals.
- The emphasis on verify-clean-transform aligns with best practices for environmental data monitoring and reporting.

## Key challenges and considerations for analysts

- Increasing the value of these datasets by integrating them with additional relevant data (e.g., soil properties, environmental conditions) beyond single-use analyses.
- Ensuring easy access to and understanding of underlying data used to generate final outputs, enabling broader reuse and transparency.