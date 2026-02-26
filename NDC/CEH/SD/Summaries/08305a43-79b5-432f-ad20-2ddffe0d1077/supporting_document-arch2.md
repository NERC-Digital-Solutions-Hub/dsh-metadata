# Information can explain the dynamics of group order in animal collective behaviour

## Overview
- Describes a high-resolution, group-level behavioural dataset from 3-spined sticklebacks (Gasterosteus aculeatus) tested in a controlled arena to study collective motion and group order.
- Aims to demonstrate how information flow and social interactions shape collective outcomes, contributing to the understanding of animal collective behaviour.

## Experimental design and collection/generation method
- Subjects: 96 fish from three holding tanks, forming 12 groups of eight for testing.
- Housing and conditions: Kept in three glass tanks (~50 fish per tank) for 10 months; temperature 16°C; 11:13 h light:dark; fed daily.
- Randomization and habituation: Groups formed via complete random block design with mixed tank representation to reduce bias; six-day habituation in smaller holding tanks with enrichment.
- Testing arena and stimuli: Oval arena (133.5 cm L × 72 cm W; 62 cm walls) with four holes (3.5 mm diameter) for presenting a bloodworm stimulus through a pipette wrapped in red tape.
- Protocol: Tests conducted Mon–Fri over four weeks (31 July–25 August 2017). Each trial: acclimation for 2 minutes, then stimulus presentations (up to six, at least 3 minutes apart) while groups are on opposite side of arena. Two sets of six groups tested on alternate days; one presentation opportunity per stimulus.

## Data collection and processing
- Video capture: Overhead 4K video (3840 × 2178) at 25 fps, camera ~161 cm above arena; lighting diffusion to reduce reflections.
- Trajectory data: Automated 2D tracking produced Cartesian coordinates (x_i, y_i) for each fish (i = 1–8) across time steps; fish identities maintained across trials using software fingerprints.
- File handling: Data stored per group per trial; group files labeled with fish coordinates (x.1, y.1 for fish 1; x.2, y.2 for fish 2; etc. up to x.8, y.8). Frame metadata included.
- Data format and conversion: Video converted to MPEG-4 HD; 1 mm ≈ 2.7 pixels to relate coordinates to physical scale.
- Quality control: Raw data; occasional untracked frames indicated as NA.

## Data structure and content
- Structure: 12 groups, each with multiple trial files; e.g., Group 1 files: 10, 23, 32, 45, 53; Group 2 files: 02, 15, 29, 39, 51, 62, 69, 80, 87, 97, 111; etc.
- Variables: For each group-trial file, eight fish are tracked with separate x and y coordinates (x.1, y.1 … x.8, y.8) and a frame index; frame-level data also included.
- Data scope: Raw trajectories for eight fish per trial, enabling analyses of movement, spacing, alignment, and response to stimuli.

## Quality, limitations, and notes
- Some frames contain NA where one or more fish could not be tracked.
- A replacement procedure occurred during the first trial week (one fish per affected group replaced with naive individuals) with 24-hour habituation before testing.

## Related outputs and context
- Primary related publication: MacGregor, H.E.A., Herbert-Read, J.E., & Ioannou, C.C. Information can explain the dynamics of group order in animal collective behaviour. Nature Communications 11, 2737 (2020).
- Additional work: MacGregor & Ioannou (in press) Collective motion diminishes, but variation between groups emerges, through time in fish shoals (Royal Society Open Science).

## Relevance for environmental monitoring analysts
- Demonstrates standardized, transparent data collection and processing workflows suitable for long-term environmental monitoring of animal groups.
- Emphasizes the importance of data quality control, reproducible processing (raw data, coordinate tracking, and frame-by-frame outputs), and clear data structures for integration with other datasets.
- Highlights two key challenges relevant to monitoring practice:
  - Increasing the value of datasets by enabling cross-study and cross-species data integration (beyond single-use analyses).
  - Providing open access to underlying data and metadata to support reuse in policy evaluation and environmental health assessments.