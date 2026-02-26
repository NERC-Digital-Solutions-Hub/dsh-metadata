# readme for soil populations - IGTE_counts.csv

- Purpose: Documentation for the IGTE_counts.csv readout describing bacterial counts from soil evolution experiments, including plasmid status, mercury exposure, replicates, species, detection markers, and how CFU per mL are calculated. Tailored for mapping and visualizing these data across treatments, timepoints, and replicates.

## Data structure and key fields

- Treatment
  - Describes plasmid carriage status at the start (pQBR57), whether the plasmid is wild-type or compensated (KO of pQBR57_0059), and whether mercury was added to the soil (at 16 μg/g).
  - Example categories include: compensated plasmid with mercury (A.Hg), wild-type plasmid without mercury (B), and no plasmid without mercury (C).
- Replicate
  - Biological replicate identifier; each treatment includes 6 independent replicates (1–6).
- Transfer
  - Evolution timepoint: 0 (start) or 30 (end).
- Bacteria
  - Species counted, determined by plating media: P. fluorescens (SBW25) or P. putida (KT2440).
- Marker
  - What the count detects:
    - All: total count for the species
    - HgR: mercury resistance detected on plasmid bearers or chromosomal mercury resistance (confirmed by PCR later)
    - KmR: kanamycin resistance (only for P. putida) to detect transfer of transposon Tn6291 via pQBR57
- Media
  - Specific detection/selection media used (and their antibiotics/mercury combinations). Examples include:
    - Gm30, Gm30Hg20
    - Sm250, Sm250Hg20
    - Sm250Km50
    - Gm6, Gm6Hg20
    - Sm125, Sm125Hg20
    - Sm125Km25
    - Sm50, Sm50Hg20
    - Sm50Km10
  - Note: concentrations may decrease over time as bacteria adapt to soil.
- Volume
  - Volume plated, in microliters (μL).
- Dilution
  - Plating dilution factor (e.g., 10^-x).
- Count
  - Number of colonies visible on the agar plate.
- CFU_ml
  - Colony forming units per mL, calculated as:
    - CFU_ml = (count × 10^dilution) / (volume × 10^-3)
  - This standardizes counts to per-mL units from plated volumes and dilutions.

## Experimental design and data interpretation notes

- The dataset combines plasmid status, mercury exposure, bacterial species, and resistance markers across multiple biological replicates.
- Timepoints (0 and 30) enable assessment of population changes over the evolution experiment.
- Media and marker combinations enable discrimination between total counts, mercury resistance, and kanamycin resistance (the latter specific to P. putida).
- Data may require harmonization across different media and timepoints before GIS-based visualization, due to varying concentrations and detection conditions.

## GIS relevance and visualization opportunities

- Map-ready aggregation: visualize CFU_ml or counts byTreatment, Bacteria species, and Marker across timepoints.
- Time-series mapping: show changes from Transfer 0 to Transfer 30 by replicate and treatment to identify spatial-like trends in soil microcosm experiments.
- Multivariate visualization: use media/marker combinations as facets or color-coding to compare total counts vs. HgR vs. KmR distributions.
- Data quality considerations: ensure consistent units (CFU_ml), handle differing media conditions, and align replicates and timepoints for accurate spatial-temporal mapping.
- Metadata integration: attach this field-level metadata to GIS features to facilitate interpretation of map-based data products and to support end-user understanding of experiment design.