# RECOUP-Moor Microbial data: Methodology

- Field Site
  - Location: Stalybridge estate, blanket bog near Manchester, UK (Saddleworth Moor)
  - Event: Wildfire on Saddleworth Moor began June 24, 2018; lasted six weeks; affected 18 km² and caused large-scale removal of surface vegetation

- Methods
  - Plot design: 10 plots established in October 2018 at the post-fire site; each plot 10 m x 10 m
  - Burn severity: 5 plots shallow burn (S1-5) and 5 plots deep burn (D1-5)
  - Unburned reference: 5 plots on a neighboring unvegetated site within the burn area; likely did not burn
  - Sampling within plots: 3 soil cores per plot (≈1 cm diameter, 5 cm depth); samples aggregated to obtain 0–2 cm (top) and 4–5 cm (bottom) depth layers
  - Reference site sampling: same procedure repeated five times at a nearby unburned site (<2 km from burn site)

- Sample handling and storage
  - Immediate on-site preservation in dry ice
  - Transport to University of Southampton
  - Storage at −20 °C until processing

- Laboratory procedures
  - DNA extraction: DNeasy PowerSoil kit
  - Target region: V4 of the 16S rRNA gene
  - Primers: 515F and 806R
  - Sequencing: Illumina MiSeq

- Data structure and plot coding (Variable key for plot code)
  - Unique_sample_ID: unique ID for microbial sample
  - Unique_plotID: ID distinguishing plot feature and replicate (S1-5 = shallow burn, D1-5 = deep burn, N1-5 = unburned/reference)
  - Burn_severity: description of burn severity
  - Sampling_depth: top (0–2 cm) or bottom (4–5 cm)
  - Months_post-fire: approximate months since the fire began
  - ASV sequence: sequence of Amplicon Sequence Variant (ASV) identified through amplicon sequencing