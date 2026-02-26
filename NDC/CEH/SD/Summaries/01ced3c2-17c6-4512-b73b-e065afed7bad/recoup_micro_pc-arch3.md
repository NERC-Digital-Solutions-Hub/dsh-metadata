# RECOUP-Moor Microbial data: Methodology

## Field Site
- Stalybridge estate on Saddleworth Moor (blanket bog near Manchester, UK).
- Wildfire on June 24, 2018, lasting six weeks; affected 18 km² and removed surface vegetation.

## Experimental Design and Sampling
- Ten plots established in October 2018 at the post-fire site.
- Burn severity: five plots with shallow (less severe) burn; five plots with deep (more severe) burn.
- Adjacent unvegetated site within the burn area sampled as an unburned/low-burn comparison; satellite data indicate it was unvegetated before the fire and likely did not burn.
- All plots had surface vegetation removed, exposing bare peat.
- Within each plot, three soil cores (≈1 cm diameter, 5 cm depth) were collected and divided into top (0–2 cm) and bottom (4–5 cm) layers; samples within a plot-depth were pooled into a single sample.
- Five additional samples collected from a neighboring unburned reference site using the same protocol.

## Sampling and Processing
- Sampling conducted in October 2018; samples preserved on dry ice and transported to the University of Southampton.
- Samples stored at −20 °C until processing.
- For DNA extraction, samples were defrosted and processed using the DNeasy PowerSoil kit.

## Laboratory Methods
- Target region: V4 of the 16S rRNA gene.
- Primers: 515F and 806R.
- Sequencing platform: Illumina MiSeq.

## Data Coding and Metadata
- Variable key for plot coding includes:
  - Unique_sample_ID: unique ID for each microbial sample.
  - Unique_plotID: distinguishes plot features and replicates (S1–S5 = shallow burn, D1–D5 = deep burn, N1–N5 = unburned/reference).
  - Burn_severity: observational description of burn severity.
  - Sampling_depth: top (0–2 cm) or bottom (4–5 cm) soil layer.
  - Months_post-fire: approximate months since fire began.
  - ASV sequence: sequence of each observed amplicon sequence variant (e.g., TACGAAGGG…).

## Data Handling and Governance
- Data are collected with explicit metadata to ensure traceability and reuse.
- The approach includes standardized sampling, DNA extraction, sequencing, and clear labeling to support data quality, comparability across plots, and potential sharing within monitoring and policy contexts.