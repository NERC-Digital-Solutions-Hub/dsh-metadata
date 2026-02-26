# RECOUP-Moor Microbial data: Methodology

## Field Site
- Location: Stalybridge estate, Saddleworth Moor, a blanket bog near Manchester, UK.
- Vegetation: Calluna vulgaris and Eriophorum vaginatum.
- Event: June 24, 2018 wildfire; fire lasted six weeks, affecting ~18 km² and removing surface vegetation.

## Sampling Design and Field Procedures
- Plots: 10 plots established in October 2018 at the post-fire site.
  - Burn severity: 5 plots shallow (S1–S5) and 5 plots deep (D1–D5) burns.
  - Adjacent reference: 5 plots on a neighboring unvegetated site within the burn area but likely unburned (N1–N5).
  - Plot size: 10 m × 10 m.
- Within-plot sampling: 3 soil cores per plot (≈1 cm diameter, 5 cm depth).
  - Depths combined per plot: 0–2 cm (top layer) and 4–5 cm (bottom layer).
  - Result: one soil sample per plot per depth.
- Reference sampling: Five samples from a neighboring unburned reference site, using the same procedure and replicated five times.
- Sample handling on site: Immediate freezing in dry ice, transported to the University of Southampton, stored at −20°C.

## Laboratory Methods
- DNA extraction: DNeasy PowerSoil kit.
- Target region: V4 of the 16S rRNA gene.
- Primers: 515F and 806R.
- Sequencing: Illumina MiSeq.

## Data Coding and Metadata
- Variable key for plot coding includes:
  - Unique_sample_ID and Unique_plotID (identifying plots and replicates; e.g., S1–S5 for shallow burn, D1–D5 for deep burn, N1–N5 for unburned/reference).
  - Burn_severity (description of burn intensity).
  - Sampling_depth (Top: 0–2 cm; Bottom: 4–5 cm).
  - Months_post-fire (approximate time since fire).
  - ASV sequence (sequence data for amplicon sequence variants, e.g., TACGAAGGG…).