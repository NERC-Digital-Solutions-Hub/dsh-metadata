# RECOUP-Moor Microbial data: Methodology

## Overview
- Post-fire microbial study on blanket bog at Stalybridge/Saddleworth Moor (near Manchester, UK).
- 10 plots established in October 2018 at a post-fire site, with 5 shallow (less severe) burns and 5 deep (more severe) burns.
- A nearby unvegetated site within the fire boundary sampled, plus five unburned reference plots nearby for comparison.
- Objective includes generating microbial data (16S rRNA gene sequences) tied to spatially defined plots and soil depths for GIS-based analysis.

## Field Site
- Location: Stalybridge estate on Saddleworth Moor, blanket bog ecosystem.
- Dominant vegetation: Calluna vulgaris and Eriophorum vaginatum.
- Fire event: June 24, 2018; wildfire affected 18 km² and removed surface vegetation.

## Sampling Design and Field Methods
- Plot layout: 10 plots at post-fire site, each 10 m x 10 m.
  - Burn severity: S1–S5 (shallow), D1–D5 (deep).
- Additional samples: 5 plots on a neighboring unvegetated site (within fire boundary but likely unburned before the fire) and 5 unburned reference plots nearby.
- Within each plot:
  - 3 soil cores collected per depth.
  - Depths: 0–2 cm (top layer) and 4–5 cm (bottom layer).
  - Across-plot aggregation: three cores per depth aggregated to one sample per plot per depth.
- Reference site sampling: same procedure, five times, to provide an unburned baseline.

## Sample Handling and Processing
- On-site handling: samples placed in dry ice immediately after collection.
- Transport and storage: transported to the University of Southampton and stored at −20 °C.
- DNA extraction: performed using the DNeasy PowerSoil kit.

## Molecular Methods
- Target region: V4 region of the 16S rRNA gene.
- Primers: 515F and 806R.
- Sequencing platform: Illumina MiSeq.

## Data Structure and Variable Key
- Variable key for plot codes:
  - Unique_sample_ID: unique ID for each microbial sample.
  - Unique_plotID: ID distinguishing plot and replicate (S1–S5 for shallow burns, D1–D5 for deep burns, N1–N5 for unburned/reference).
  - Burn_severity: description of burn severity (observational).
  - Sampling_depth: top (0–2 cm) or bottom (4–5 cm) soil layer.
  - Months_post-fire: approximate months since the fire began.
  - ASV sequence: sequence of amplicon sequence variants identified by sequencing.

## GIS-related Data Considerations
- Spatial integration opportunities:
  - Map plot boundaries and centroids (10 m x 10 m plots) and assign burn severity and sample depth attributes.
  - Link microbial data (ASV profiles) to each spatial unit for visualization of community composition by burn severity and soil depth.
  - Create layers for post-fire vs. unburned/reference comparisons, including distance to unburned areas if relevant.
  - Time-since-fire dimension (Months_post-fire) can be used to analyze temporal changes in microbial communities if multiple timepoints are added.

## Data Management and Access
- Sample handling and storage procedures emphasize chain-of-custody and temperature control (dry ice on-site; −20 °C storage).
- DNA data are generated via Illumina MiSeq, with detailed sample and plot coding to enable cross-referencing with GIS attributes and metadata.