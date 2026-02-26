# Records of offspring production for 192 female cockroaches ( Blaptica dubia )

## Overview
- Records the number of nymphs produced by 192 female cockroaches across up to two broods.
- Data collected to assess fitness consequences of social network position under different humidity conditions.
- Collected at the University of Aberdeen Zoology building insectary between 29/12/23 and 23/01/24.
- Stored and managed as a spreadsheet with accompanying methodological metadata.

## Data collection and structure
- Each female housed in an individual box with food, hydration, and shelter; checked twice weekly for offspring counts.
- Females mated with two males over two weeks (28°C, ~50% humidity) and tagged for identification.
- Post-mating, females transferred to an incubator at 28°C with either 50% or 30% humidity for two weeks (experimental period) where social associations were recorded (refer to cockroach_aggregation_records).
- After the experimental period, all females returned to 28°C 50% humidity in individual containers; offspring production counted twice weekly for 10 weeks.
- Dataset fields (metadata) include:
  - unique_ID: unique identifier for each female
  - humidity: 50% or 30% humidity during the experimental period
  - label: back tag identifier
  - group: social group identifier
  - nymphs: number of nymphs produced in brood 1
  - date1: date of brood 1 (NA if none)
  - nymphs2: number of nymphs produced in brood 2
  - date2: date of brood 2 (NA if none)
  - total_off: total offspring across both broods

## Data completeness and handling
- All females have brood data; 40/192 produced non-zero brood 1; 1/192 produced non-zero brood 2.
- If zero offspring for a brood, the date is NA and the corresponding nymphs value is 0 or NA as applicable.
- Data are recorded in a single spreadsheet; related dataset (cockroach_aggregation_records) contains social network details.

## Data quality, standards, and stewardship
- Responsible personnel: Callum McLean (RAs), Georgia Cash (PhD student), and Principal Investigator David Fisher; McLean and Fisher responsible for interpretation.
- Emphasis on clear metadata to enable reuse (detailed variable descriptions and the linkage to the related aggregation records dataset).
- Clear documentation of experimental design, environmental conditions, and timing to support reproducibility and secondary analyses.
- Data storage location noted (University of Aberdeen Zoology building insectary) and plan to upload/share through appropriate data portals as part of governance.

## Experimental design and context (methods)
- Experimental setup:
  - 192 females mated with two males over two weeks at 28°C, ~50% humidity.
  - Two humidity treatments during the experimental period: 50% and 30% humidity, with groups of 24 tracked for social associations.
- Post-experiment monitoring:
  - Return to 28°C, 50% humidity; offspring counts twice weekly for 10 weeks; no offspring observed after 10 days.
- Purpose tied to a project on the evolution and plasticity of social networks traits and how humidity influences fitness outcomes.

## Storage, accessibility, and reuse considerations
- Primary data stored as a spreadsheet with structured metadata and links to related datasets (e.g., social association records).
- Completeness notes and NA handling documented to aid correct interpretation of zero vs. missing data.
- For reuse, ensure alignment between metadata fields and any linked datasets; maintain provenance of data collection and processing steps as described.