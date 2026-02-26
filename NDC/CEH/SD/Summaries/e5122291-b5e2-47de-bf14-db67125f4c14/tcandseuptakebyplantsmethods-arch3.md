# Tc and Se Uptake By Higher Plants - Meta Data

## Overview
- Investigates uptake of technetium-99 (99Tc) and selenium-75 (75Se) by higher plants.
- 61 species, each with 5 replicates in 12 cm pots with saucers.
- Growth medium: Levington's F2S compost; supplementary lighting and heating; watered to field capacity.
- Plants grown in randomised blocks until exponential growth phase.

## Experimental design
- Species sampled across three major clades of the APGIII angiosperm phylogeny (labelled a, b, c in accompanying file).
- Randomised block design with batches to manage variability.

## Radiolabeling and measurements
- Radiolabeling: 25 mL solution containing 107 kBq/L 99Tc and 95 kBq/L 75Se distributed on the compost surface.
- Mean activity: 99Tc ~17.8 kBq/kg compost; 75Se ~15.8 kBq/kg compost.
- Harvest: 48 hours post-labeling; above-ground shoots dried and 0.1 g digested in 5 mL HNO3 plus 5 mL H2O2.
- Measurement: gamma-emissions counted for 75Se; beta-emissions counted for 99Tc after appropriate sample preparation.
- Data are decay-corrected to the labeling date for 75Se.

## Data file structure and column explanations
- Data file: TcAndSeUptakeByPlantsData
- Key columns:
  - Block: indicates the random block in which the species were grown together.
  - CPM1 beta: counts per minute of beta emissions from Tc-99.
  - CPM1 gamma: counts per minute of gamma emissions from Se-75.
  - Decay corrected: counts per minute of Se-75 decay-corrected to the time of labeling.

## Data processing and provenance
- Detailed protocol for sample digestion, counting, and decay correction to ensure traceability and repeatability.
- Explicit metadata supports interpretation of uptake measurements across species and experimental blocks.

## Relevance for monitoring frameworks
- Provides a controlled dataset linking plant uptake of contaminants (Tc and Se) to species and experimental conditions, useful for evaluating environmental uptake pathways.
- Demonstrates rigorous data capture, processing steps, and decay-correction requirements that align with metadata and data quality standards.
- Highlights the importance of clear data documentation (blocks, counts, decay corrections) for policy-relevant environmental health monitoring and future decision-making.