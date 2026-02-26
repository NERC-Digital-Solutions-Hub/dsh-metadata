# Experimental design / sampling regime

- Objective and scope
  - Document describes an experimental study on herbivory in oil palm within the BEFTA project framework.
  - Location: three oil palm estates in Riau Province, Sumatra, Indonesia (Pt Ivo Mas Tunggal): Ujung Tanjung, Kandista, Libo.
  - Timeframe: sampling from 2013 to August 2017 (18 measurement occasions).
  - Part of a broader vegetation management experiment; plots include mature/over-mature stands and replanted stands.

- Study setting and sampling design
  - Experimental area: 50 x 50 meters per plot, with approximately 50 meters of separation from access tracks on three sides and about 1000 meters from the fourth side.
  - Plots: 18 plots established in 2013 as part of BEFTA; mature stands include plots planted 1987–1992; Libo replanted in 2014.
  - Palm selection and positioning: within each plot, three palms randomly selected from numbered palms; sampling positions fixed at edge of plot at 45°, 165°, and 285° from compass north.
  - Field procedures: herbivory assessed by visual estimation of crown damage; the 18th frond is removed for detailed assessment.

- Measurements and units
  - Observational workflow: after frond removal, 20 leaflets (in 10 pairs) are photographed for damage assessment.
  - Two key data streams:
    - PercentDamagePhoto: percentage leaf area damaged based on digital image analysis of the 20 leaflets.
    - PercentTotalDamageEye / PercentFrondEye: observer-assessed damage to entire palm crown and to the 18th frond, respectively.
  - Additional data: Abunclass (damage abundance class) and Count (number of leaflets in each damage class).
  - Distance metadata: for data from 2016–2017 exclosure experiments with ant poison, distance records proximity to focal palm; data within exclosure or near exclosure may be unreliable.

- Data processing and quality control
  - Pre-processing: photographs converted to binary images; manual adjustments for missing leaflet tips to estimate intact area; consistent photographer, angle, board, and camera used.
  - Quality checks: basic validation for impossible values; 50% data-entry verification against field sheets with error rate <1%; all changes annotated with provenance.
  - Data processing notes: image-derived data and annotated counts stored in a transparent “thin format” csv structure.

- Data structure and storage
  - Files: three separate .csv files (data from mature stands and replanted plots).
  - Thin format: each row represents a single observation; percentage data type repeated across rows for each damage category.
  - Key fields include: Estate_abbrev, Triplet, Plot, Treatment, Period, PalmNumber, Date, PercentTotalDamageEye, PercentFrondEye, PercentDamagePhoto, Abunclass, Count, distance.
  - Descriptions clarify coding (e.g., estate names KNDE for Kandista, UTNE for Ujung Tanjung, LIBE for Libo; triplets identify plot sets; Plot identifiers like C01; Treatment categories: reduced, normal, enhanced).

- Miscellaneous and governance
  - Funding: NE/P00458X/1.
  - Data files: BEFTA core plots (2016–2017) and replanted plots data.
  - Reproducibility notes: standardized measurement protocol, with image-based and observer-based damage assessments; explicit metadata about measurement conditions and data provenance.
  - Access and use considerations: the dataset discusses public sharing of underlying data as a governance consideration; the distance column highlights data points that may be unsuitable due to proximity to ant-poison exclosures.

- Relevance for monitoring and policy evaluation
  - Provides a structured, time-series dataset on herbivory and palm damage across different management treatments and stand types.
  - Demonstrates rigorous data collection, processing, and quality assurance suitable for monitoring environmental health indicators in agricultural ecosystems.
  - Includes detailed metadata and data governance notes, facilitating data reuse, integration with other datasets, and transparent reporting of limitations (e.g., exclosure-related proximity effects).