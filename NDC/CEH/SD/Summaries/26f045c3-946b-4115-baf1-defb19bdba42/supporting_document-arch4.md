# Shoaling and foraging trial data in fish

## Overview
- Behavioral data from six-fish groups tested for shoaling and group foraging across 2 consecutive days, with 31 groups in total.
- Experiments conducted under controlled lab conditions (temperature, light cycle) using standardized arena and recording setup.
- Data captured as high-resolution 2D trajectories (x, y coordinates) for each fish, with identities maintained across trials.

## Experimental setup and timeline
- Subjects: fish collected from the River Cary, Somerset, UK; mean body length 43 ± 3.2 mm at testing.
- Housing and conditions: held in two large glass aquaria for 8 months before testing; water at 14°C; 11:13 hour day/night photoperiod.
- Testing window: 23 September 2019 to 11 March 2020.
- Grouping: groups of six tested over two consecutive days; up to two groups tested per week.
- Arena and recording: white opaque circular arena (97 cm diameter, water depth 10 cm) within a white Perspex tank; filmed from above with a 4K camera and a GoPro, with external monitors to observe trials.

## Procedures

- Day 1 (individuals in group): six fish from the same holding tank allocated to a group by stratified random sampling; each fish filmed individually while in the group.
- Day 2 (group foraging): fish filmed in their group during foraging; groups housed overnight and not reused after testing.

- Individual behavioral assays: each fish placed in an 8 cm diameter × 25 cm high acetate cylinder for 1 minute to view the arena, then released to swim freely for 10 minutes; following this, all six fish in the group are placed in a central chamber for 2 minutes before reseating in the arena for observation.

- Shoaling trials: shoaling behavior recorded for 20 minutes after the rearrangement.

- Group foraging trials: after a 5-minute habituation, a green pipette-tip stimulus is presented from one of four holes; two bloodworms provided as rewards when approached within 10 cm; stimulus held for 15 seconds; presented at least every 3 minutes; trial ends when bloodworms are not consumed within 5 minutes (satiation).

## Data collection and processing

- Video and tracking:
  - Videos converted to MPEG-4 HD; automated 2D tracking used to extract x, y coordinates for each fish at each time step.
  - Individual identities maintained across shoaling and foraging trials using idTracker, with re-tracking adjustments for individual assays to improve accuracy.
- Metadata and provenance:
  - Central chamber used during individual assays to stabilize identities; data re-tracked excluding the central chamber for improved individual tracking.
  - Raw data are preserved with notes on any NA entries where tracking failed; some trials had instances of no movement or corrupted video files.

## Data structure and file formats

- n_n2.txt
  - Columns: x coordinate (X1, X2, …) and y coordinate (Y1, Y2, …) descriptions provided.
- n_shoal.txt
  - Trajectories for six fish: trajectories.1–trajectories.6 (x coordinates), trajectories.7–trajectories.12 (y coordinates), plus frame.
- n_forage.txt
  - Trajectories for six fish: trajectories.1–trajectories.12 similarly structured as in n_shoal, plus frame.

## Quality control and limitations

- Data are provided in raw form; some frames have NA due to tracking gaps.
- A few trials had no movement by one or more fish, and a small number of video files were corrupted.
- Not all groupings or trials are perfectly complete; data reflect these imperfections as noted in the files.

## Relevance for data leadership and governance

- End-to-end data lineage: clearly documents collection conditions, equipment, timing, and trial structure, enabling reproducibility and auditability.
- Rich trajectory data: enables analyses of individual and group motion, social dynamics, and foraging decisions, useful for cross-group and cross-lab comparisons.
- Metadata and identifiers: use of idTracker for consistent identity across trials improves data integrity and traceability.
- Data accessibility and reuse: raw data are organized in clearly named files with descriptive structures, though formal metadata standards and documentation would improve discoverability and reusability (e.g., standardized metadata schemas, data dictionaries, and data licensing).
- Data quality management: visibility of NA entries and occasional corrupted files highlights the need for ongoing quality checks, versioning, and potentially automated validation pipelines.
- Opportunities for data governance improvements:
  - Establish standardized metadata (experimenter, date/time, group composition, trial type, arena settings, tracking parameters).
  - Provide data processing scripts and a reproducible workflow to transform raw trajectories into ready-to-analyze formats.
  - Implement data versioning, provenance records, and a data catalog to support discovery and reuse across research networks.
  - Consider open data practices with accompanying documentation to facilitate cross-lab collaboration and benchmarking.

## Key takeaways

- The dataset captures detailed 2D movement data for six-fish groups across shoaling and group foraging tasks under controlled laboratory conditions.
- Comprehensive documentation of experimental design, video capture, tracking methodology, and data structure supports reproducibility, with noted data quality considerations.
- From a data-leadership perspective, the dataset illustrates the importance of end-to-end data governance, robust metadata, and mechanisms to improve discoverability, standardization, and reuse across networks.