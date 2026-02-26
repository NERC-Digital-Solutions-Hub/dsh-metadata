# Tc and Se Uptake By Higher Plants - Meta Data

## Overview
- Metadata for a dataset examining uptake of technetium-99 (Tc-99) and selenium-75 (Se-75) by higher plants.
- 61 species, each with 5 replicates, grown in randomised blocks.
- Focused on three major clades of APGIII angiosperm phylogeny (labelled a, b, c in accompanying materials).

## Experimental design and data collection
- Growing conditions:
  - 12 cm pots with saucers; Levington's F2S compost (sphagnum peat-based) with added lime (dolomite) and ammonium sulfate (~3%).
  - pH ~6.2; P ~50 mg/L; K ~50 mg/L; nitrate ~10 mg/L.
- Experimental setup:
  - Plants grown in randomised blocks, in batches, until exponential growth phase.
- Radiolabelling:
  - 25 mL solution surface-applied containing 107 kBq/L 99Tc and 95 kBq/L 75Se.
  - Mean activity in substrate: ~17.8 kBq 99Tc/kg; ~15.8 kBq 75Se/kg.
- Harvest and preparation:
  - After 48 hours, above-ground shoot material harvested, dried, and digested (0.1 g in 5 mL HNO3 + 5 mL H2O2) until reaction ceased.
  - Digested samples cooled and counted for emissions.

## Measurement and data processing details
- Counting methods:
  - 75Se gamma-emissions counted; 99Tc beta-emissions counted after digestion using scintillant.
  - Counts for Se-75 decay-corrected to the labeling date.
- Data recording:
  - Counts reported as CPM (counts per minute) for both beta (Tc-99) and gamma (Se-75) emissions.
  - Decay-corrected values adjusted to time of labeling for Se-75.

## Data file schema and key fields
- Data file name: TcAndSeUptakeByPlantsData.
- Key columns:
  - Block: indicates species grown together in a random block design.
  - CPM1 beta: counts per minute beta emissions from Tc-99.
  - CPM1 gamma: counts per minute gamma emissions from Se-75.
  - Decay corrected: Se-75 counts per minute decay-corrected to time of labeling.

## Metadata, provenance, and quality
- Detailed substrate composition, pH, and nutrient levels enable reproducibility and cross-study comparisons.
- Random block design supports control of variability and robust interpretation.
- Explicit decay-correction information ensures temporal comparability of Se data.
- Clear documentation of measurement methods (gamma vs beta counting) aids data integration.

## Implications for data strategy and reuse
- Serves as a strong example of comprehensive experimental metadata for complex radiolabeled uptake studies.
- Highlights importance of:
  - Precise provenance (substrate, growth conditions, labeling specifics).
  - Clear data schema with explicit units and decay corrections.
  - Documented data processing steps for reproducibility.
- Useful for cross-study uptake analyses across many species and clades, provided standardized metadata is maintained.

## Limitations and access considerations
- Data involves radiolabeled materials; ensure appropriate governance, safety, and access controls.
- User interpretation requires understanding of units (kBq/kg compost) and decay corrections.
- Potential gaps in metadata beyond what is described (e.g., additional growth conditions or timepoints) should be considered when integrating with other datasets.