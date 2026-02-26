# Rationale Contamination of waterbodies with FIOs from diffuse and point sources is of significant concern to human health, as well as waterbody quality and ecology, due to the potential for exposure to a large audience of formal and informal recreational users, and for overlap with a range of other stressors.

- Purpose of the dataset: examine the spatial distribution of faecal indicator organisms (FIOs) and their drivers in standing waters across UK Hydroscapes, to inform environmental health monitoring, policy decisions, and future actions.
- Hydroscapes and study sites: three contrasting landscapes were selected—Greater Glasgow (urban), Cumbria (upland/pastoral), and Norfolk (agricultural). Within each Hydroscape, 18 water bodies were chosen to represent gradients in size, productivity, hydrological connectivity, and ecological quality.
- Sampling timeframe: data collected across three seasons (spring, summer, autumn) in 2016 or 2017.
- Target metrics: E. coli concentrations (CFU per 100 ml) and total heterotrophs (CFU per 100 ml) in standing waters.

## Study areas and contextual information

- Hydroscape descriptions:
  - Greater Glasgow: urban landscape
  - Cumbria: upland/pastoral landscape
  - Norfolk: agricultural landscape
- Water bodies: 18 per Hydroscape, selected to capture gradients in size, productivity, connectivity, and ecological quality.
- Seasonal sampling: spring, summer, autumn across 2016–2017.

## FIO sampling and analysis

- Sampling timing: all samples collected 3 hours after sunrise to maintain consistency with UAV exposure timing referenced in the study.
- Spatial sampling design: per water body, samples collected from three discrete locations (~100 m apart). At each location, three subsamples collected about 5 m apart, yielding nine unique samples per water body per visit.
- Total samples: 1,278 unique samples across all water bodies and visits.
- Water collection protocol: samples taken approximately 30 cm below the surface using sterile 180 ml bottles; kept at 4°C and processed within 6 hours.
- Laboratory analysis:
  - Filtration volumes: 100 ml, 10 ml, and 1 ml filtered separately through 0.45 μm membranes.
  - Growth medium: MLGA agar.
  - Incubation: 37°C for 24 hours.
  - Output: bacterial counts reported as colony-forming units (CFU) per 100 ml.
  
## Appendix and data structure

- Dataset focus: Disease_distribution_data_UK_standing_waters.csv
- Field names and descriptions:
  - Hydroscape: landscape type (Greater Glasgow, Cumbria, Norfolk)
  - season: season of data collection (spring, summer, autumn)
  - site: focal water body name
  - sample: code for spatially discrete sample per water body (1–3)
  - rep: sub-sample (a–c) within each sampling point
  - Ecoli: Escherichia coli concentration (CFU per 100 ml)
  - Hetero: total heterotrophs concentration (CFU per 100 ml)
- Metadata purpose: facilitates data verification, reuse, and cross-study comparability; highlights the importance of clear field names and definitions for data sharing.

## Relevance for monitoring frameworks

- Demonstrates a structured, multi-site, multi-season sampling framework to monitor FIOs in waterbodies with varied land use.
- Emphasizes standardized field timing, spatial replication, and sub-sampling to capture within-waterbody variability.
- Includes explicit data descriptors and metadata to support transparency, data governance, and reuse in policy-making and dashboards.
- Highlights practical data management steps (e.g., cold chain, timely processing) essential for data quality and comparability across monitoring programs.
- Illustrates considerations for overcoming data gaps and ensuring openness and accessibility of underlying data in environmental health monitoring.