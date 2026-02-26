# PalmFrondHerbivory_2016_2017.csv

- Study context and aims
  - Investigates herbivory damage to oil palm crowns on three estates in Riau Province, Sumatra, Indonesia (Ujung Tanjung, Kandista, Libo) as part of the BEFTA project.
  - Focuses on mature vs replanted stands and how herbivory damage accumulates over time.

- Experimental design and sampling regime
  - 18 plots established in 2013 within a 50 x 50 m area per plot, 50 m from access tracks on three sides and ~1000 m from the fourth side.
  - Each palm numbered; three sampling positions per plot at 45°, 165°, and 285° from north.
  - Three palms per plot randomly selected for herbivory assessment.
  - Herbivory measured every 3–4 months from 2013 to August 2017 (total of 18 sampling events).

- Data collection and processing methods
  - Overall crown herbivory estimated visually; the 18th frond is cut and collected for analysis.
  - From the frond: 20 leaflets are photographed in a fixed protocol; damaged categories assigned (1 = no damage to 4 = heavy damage).
  - Images pre-processed to obtain total leaflet area; a second image is created with all damage filled in to estimate intact area.
  - Percent damage calculated as:
    - PercentTotalDamageEye (observer-assessed crown damage)
    - PercentFrondEye (damage on the 18th frond)
    - PercentDamagePhoto (area damaged on 20 leaflets from image analysis)
  - Abundance class (Abunclass) and Count (number of leaflets in that class) recorded for each observation.
  - A distance variable exists for observations near ant-poison exclosures (2016–2017); data with values in this column may not be suitable for general analysis.

- Data format and structure
  - Three separate CSV files (thin format): each row represents a single observation for a damage category; percentage data is repeated across rows for the same observation.
  - Key columns:
    - Estate_abbrev, Triplet, Plot
    - Treatment (reduced, normal, enhanced)
    - Period (discrete sampling periods)
    - PalmNumber, Date
    - PercentTotalDamageEye, PercentFrondEye, PercentDamagePhoto
    - Abunclass, Count
    - distance (related to exclosure proximity)

- Data quality and provenance
  - Basic validation performed; 50% of data entries checked against original field sheets with error rate <1%.
  - All changes tracked with metadata to ensure traceability.

- Data storage and availability
  - Data from mature stands are stored in BEFTA core plots (2016–2017); replanted-stand data are in a separate file.
  - Funding: NE/P00458X/1.
  - Main dataset referenced within a broader BEFTA project: Biodiversity and Ecosystem Function in Tropical Agriculture.

- Important notes for analysis and interpretation
  - Variation in data collection methods (visual eye estimates vs image-based measurements) provides multiple perspectives on damage but requires harmonization considerations.
  - The “Period” and plot-level treatments enable analyses of temporal trends and management effects on herbivory.
  - Exclosure-related distance data should be treated cautiously in analyses due to potential contamination or confounding factors.
  - Data at local scales (plot/palm level) enable fine-grained analyses but may face limitations in generalizing beyond the three estates.