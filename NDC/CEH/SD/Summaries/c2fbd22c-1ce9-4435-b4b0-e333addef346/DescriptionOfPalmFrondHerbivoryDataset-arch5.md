# Experimental design / sampling regime

## Study location and plots
- Location: three oil palm estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal): Ujung Tanjung, Kandista, Libo.
- Planting timeline: estates established 1987–1995 on mineral soils; Libo replanted in 2014.
- Experimental setup: 18 plots established in 2013 as part of the Biodiversity and Ecosystem Function in Tropical Agriculture project.
- Plot geometry: each plot 50 x 50 m with ~50 m separation from access tracks on three sides and ~1000 m from the fourth side.
- Palm and sampling: each palm numbered; three sampling positions per plot at 45°, 165°, and 285° from north.

## Data collection protocol (herbivory measurements)
- Sampling schedule: measurements every 3–4 months from 2013 to August 2017 (18 occasions).
- Palm selection: in each plot, three palms randomly chosen from numbered palms.
- Damage assessment: overall crown herbivory visually estimated; 18th frond cut, captured, and assessed.
- Leaflet sampling: 20 leaflets (in 10 pairs) taken from the frond, placed on a board, photographed consistently by the same person, under consistent conditions.
- Damage categorization: leaflets categorized 1 (no damage) to 4 (heavy damage); counts per category recorded.
- Image processing and analysis: photographs pre-processed to remove noise, converted to binary; leaflet area measured with Fiji; damaged areas filled in for an alternative intact estimate; missing leaflet tips conservatively estimated.
- Response variables: 
  - PercentTotalDamageEye (observer-assessed crown damage)
  - PercentFrondEye (damage on the 18th frond)
  - PercentDamagePhoto (percent surface area lost from digital photograph analysis)
  - Abunclass (damage class for leaflets)
  - Count (number of leaflets in each damage class)
- Distance note: distance column records proximity (within 20 m of ant-poison exclosures); data within this proximity may be unreliable.

## Data fields, structure, and units
- Data storage: three separate CSV files in thin format (one observation per line; percentage data repeated across rows).
- Key headers and descriptions:
  - Estate_abbrev, Estate Description (e.g., KNDE for Kandista, UTNE for Ujung Tanjung, LIBE for Libo)
  - Triplet, Triplet Description (plot triplets)
  - Plot, Plot Description (C01 format)
  - Treatment, Treatment Description (reduced, normal, enhanced)
  - Period, Period Description (discrete sampling periods)
  - PalmNumber, PalmNumber Description (unique BEFTA palm identifier)
  - Date, Date Description (observation date)
  - PercentTotalDamageEye, PercentFrondEye (numeric; observer-assessed damage)
  - PercentDamagePhoto, Abunclass (numeric and categorical damage from photo analysis)
  - Count (integer; number of leaflets in that damage class)
  - distance (numeric; proximity to exclosures; to be used with caution)

## Data quality control, provenance, and notes
- Quality checks: basic validation for impossible values; 50% of data entry cross-checked against field sheets; error rate <1%; corrections recorded with the dataset.
- Provenance: changes and rationale tracked; existence of accompanying notes documenting data processing steps (including image processing and conservative leaflet tip estimation).
- Format decisions: data stored in CSV with thin format; explicit documentation of field meanings and units to support interoperability and reuse.

## Data governance and access considerations
- Data scope: covers mature stands (Kandista, Ujung Tanjung) and replanted stands (Libo); separate datasets for core mature plots and replanted plots.
- Data caveats: the distance column indicates potential non-use of certain records (exclosure proximity); users should consider excluding or carefully filtering these observations.
- Miscellaneous information: funding reference NE/P00458X/1; BEFTA project context; coordinates and miscellaneous plotting details provided for context.

## Practical implications for Data Stewards
- Ensure metadata completeness includes field definitions, units, and data generation workflow (visual scoring, frond harvesting, photography, image analysis).
- Maintain data lineage: document pre-processing steps (MS Paint, Fiji thresholds, conservative leaflet-tip estimation) to enable reproducibility.
- Manage data sensitivity and provenance: track updates, corrections, and any exclusions due to exclosure proximity.
- Support interoperability: note the thin format and repeat structure for percentage data to aid downstream analyses and integration with other BEFTA datasets.