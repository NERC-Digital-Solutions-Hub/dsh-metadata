# Experimental design / sampling regime

- Study location and context
  - Research conducted on three oil palm estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal): Ujung Tanjung (UTNE), Kandista (KNDE), and Libo (LIBE).
  - Part of the Biodiversity and Ecosystem Function in Tropical Agriculture project; plots planted 1987–1995 on mineral soils.
  - 18 plots established in 2013 within a 50 × 50 m experimental area; mature vs replanted stands represented (Ujung Tanjung and Kandista are mature; Libo replanted in 2014).

- Experimental design
  - Each palm within the 50 × 50 m area is numbered; three sampling positions per plot defined at 45°, 165°, and 285° from north.
  - Overall herbivory measured from 2013 to August 2017 (18 sampling events).

- Sampling protocol
  - In each plot, randomly select three palms from the numbered set.
  - Assess herbivory on the crown visually; then cut the 18th frond and capture a standardized photograph of 20 leaflets (in 10 pairs, evenly spaced along the frond).
  - Leaflets categorized damage levels 1–4; count leaflets per category.
  - Image processing sequence:
    - Pre-process photos to remove noise; convert to binary; measure total leaflet area in Fiji.
    - Create a second image with herbivory “filled in” to estimate the intact leaf area; compensate for missing leaflet tips conservatively.
  - Ensure all photos are taken by the same person, from the same angle, using the same equipment for consistency.

- Variables and measurements
  - Eye observations:
    - PercentTotalDamageEye: percentage damage to the whole crown as estimated by the observer (A. D. Advento).
    - PercentFrondEye: percentage damage observed on the 18th frond.
  - Image-based measurements:
    - PercentDamagePhoto: percentage of surface area damaged as determined from digital photographs.
  - Abundance data:
    - Abunclass: damage class category for the line.
    - Count: number of leaflets in that damage class (out of 20).
  - Distance (for exclosure-related data):
    - distance: recorded only for palms within 20 m of focal palms inside exclosures where ant poison was applied (July 2016–August 2017; note: data with a value in this column should probably not be used).

- Data quality and provenance
  - Basic data validity checks performed; 50% of data entries cross-checked against field sheets with <1% error rate.
  - All changes tracked and documented with the dataset.

- Data format and structure
  - Three separate CSV files (thin format): two for mature stands; one for replanted plots.
  - Structure details:
    - Estate_abbrev, Triplet, Plot, Treatment, Period, PalmNumber, Date
    - PercentTotalDamageEye, PercentFrondEye, PercentDamagePhoto
    - Abunclass, Count
    - distance
  - Thin format means each line is a single observation; percentage data may be repeated across multiple rows to represent categories.

- Plot and dataset specifics
  - Mature stands data include plots labeled C01, C10–C19, D28–D30, F04–F06, G07–G16, etc. with coordinates provided in the Miscellaneous section.
  - Replanted stands data include plots labeled with estate E and associated coordinates.
  - Two BEFTA data files: core plots (2016–2017) and replanted plots.

- Miscellaneous context
  - Funding reference: NE/P00458X/1.
  - Data provision includes exact coordinates for plots (section Miscellaneous lists coordinates and plot identifiers).

- GIS-focused implications
  - Suitable for map-based visualization of herbivory across estates, plots, and time.
  - Can be linked to treatment, period, and palm-level identifiers for spatial analyses.
  - Data normalization may be needed to reconcile thin format with GIS attribute tables; careful handling of the distance variable for exclosure-related data.