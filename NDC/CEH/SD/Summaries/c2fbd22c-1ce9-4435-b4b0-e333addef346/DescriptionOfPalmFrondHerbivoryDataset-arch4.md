# Experimental design / sampling regime

- Location and scope
  - Research conducted on three oil palm estates in Riau Province, Sumatra, Indonesia: Ujung Tanjung (UTNE), Kandista (KNDE), Libo (LIBE) owned by Pt Ivo Mas Tunggal.
  - Part of the Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) project; 18 plots established in 2013 within the BEFTA framework.
  - Growth histories: Ujung Tanjung and Kandista plots are mature/over-mature oil palm (planted 1987–1992); Libo plots replanted in 2014.

- Plot design and sampling
  - Experimental area: 50 x 50 m with 50 m clearance to three sides and ~1000 m to the fourth side.
  - Palm indexing: each palm numbered; three sampling positions per plot at 45°, 165°, and 285° from compass north.

- Herbivory measurement protocol
  - Measurement period: 2013–August 2017, with 18 measurement events at 3–4 month intervals.
  - Palm selection: randomly choose three palms per plot for each observation.
  - Damage assessment process
    - Visually estimate overall crown damage.
    - Cut and collect the 18th frond, photograph 20 leaflets (in 10 pairs, evenly spaced) after arranging on a board; photos taken by the same observer from fixed angle with the same equipment.
    - Leaflet damage categorized from 1 (no damage) to 4 (heavy damage); record counts per category.
    - Digital image analysis: preprocess photos to binary, measure total leaflet area in Fiji; create a second image with damage filled in to estimate intact area; compute percent leaf area damaged.

- Response variables and units
  - PercentTotalDamageEye: observer-estimated damage for the whole crown.
  - PercentFrondEye: damage percentage for the 18th frond.
  - PercentDamagePhoto: damage percentage from digital photograph analysis of 20 leaflets.
  - Abunclass: damage class for each observation line.
  - Count: number of leaflets in the corresponding damage class.
  - Distance: distance to focal palm within ant-excluded exclosures (relevant for the exclosure experiment; not recommended for use if data are outside the specified radii).

- Data quality and governance
  - Basic validity checks performed; 50% of data entries validated against original field sheets with <1% error rate; corrections recorded with data provenance preserved.

- Data format and storage
  - Three separate CSV files in thin (long) format; each line represents a single observation with repeated percentage data across rows as needed.
  - Key columns include: Estate_abbrev, Triplet, Plot, Treatment, Period, PalmNumber, Date, PercentTotalDamageEye, PercentFrondEye, PercentDamagePhoto, Abunclass, Count, distance.
  - Data notes: dataset includes BEFTA core plots (2016–2017) and replanted plots; certain distance data relate to exclosure treatments and may limit use if outside specified conditions.

- Miscellaneous and metadata
  - Funding reference: NE/P00458X/1.
  - Coordinate information and example plot identifiers provided for mature stands and replanted stands (plot naming like C01, D28, G07, etc.).
  - The dataset is designed to support analyses of herbivory impact and data-driven understanding of palm leaf damage across different management treatments and over time.

- Practical considerations for use
  - Be aware of the exclosure-related distance field, which may indicate data points not suitable for certain analyses.
  - Two data files exist: one for BEFTA core plots (2016–2017) and one for replanted plots; ensure correct file usage in analyses.