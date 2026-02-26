# RECOUP-Moor Microbial data: Methodology

## Scope and Objective
- Microbial DNA dataset collected from post-fire and reference conditions on Saddleworth Moor, UK.
- Includes plant community context, burn severity (shallow vs deep) and unburned/reference areas.
- DNA sequencing target: 16S rRNA V4 region using Illumina MiSeq.

## Field Site and Experimental Design
- Location: Stalybridge estate blanket bog near Manchester; vegetation: Calluna vulgaris and Eriophorum vaginatum.
- Event: June 24, 2018 wildfire; affected ~18 km2 and removed surface vegetation.
- Plot layout (Oct 2018): 10 plots, each 10 m x 10 m.
  - 5 plots: shallower burn (S1–S5).
  - 5 plots: deeper burn (D1–D5).
  - Bare peat exposed across post-fire plots.
- Additional reference: 5 plots on a neighboring unvegetated site within burn area, likely unburned prior to fire.

## Sampling and Sample Processing
- Within each plot:
  - Collect 3 soil cores (approx. 1 cm diameter, 5 cm depth).
  - Pool to form one sample per plot per depth (top 0–2 cm; bottom 4–5 cm).
- Reference site sampling: same procedure, five replicates.
- Sample handling: on-site dry ice, transport to University of Southampton, store at -20°C.
- Laboratory processing:
  - DNA extraction with DNeasy PowerSoil kit.
  - Target region: V4 of 16S rRNA using primers 515F and 806R.
  - Sequencing: Illumina MiSeq.

## Metadata and Coding Scheme
- Key variables encoded in the plot code:
  - Unique_sample_ID, Unique_plotID, Burn_severity, Sampling_depth, Months_post-fire, ASV sequence.
- Burn severity coding:
  - S1–S5: shallow burn (per plot).
  - D1–D5: deep burn (per plot).
  - N1–N5: unburned/reference.
- Depth coding:
  - Top (0–2 cm) or Bottom (4–5 cm) soil layer.
- Months_post-fire: approximate months since fire.
- ASV sequence: sequence identifiers for amplicon sequence variants.

## Data Governance and Quality Considerations for Data Stewards
- Provenance and traceability:
  - Clear linking of field plots to burn severity and depth, with unique IDs.
  - Documentation of collection date, handling, and processing steps (on-site freezing, lab extraction, primers, sequencing platform).
- Data structure and interoperability:
  - Use of consistent, descriptive codes with explicit mappings (S/D/N, S1–S5, D1–D5, N1–N5).
  - Depth and sampling depth clearly defined to enable aggregation or stratified analyses.
- Data quality and limitations:
  - Burn severity is observational; potential misclassification risk.
  - Small number of plots per category; spatial proximity (<2 km to reference) may influence comparisons.
- Standards and reuse:
  - Metadata fields align with standard sample-based microbial studies (sampling depth, burn treatment, time since fire, ASV data).
  - Recommend including standardized metadata conventions (e.g., MIxS) for broader reuse and discovery.
- Data management notes:
  - Data are organized by plot and depth with ASV sequences; ensure proper versioning and sufficiency of documentation to reproduce analyses or re-use in meta-analyses.