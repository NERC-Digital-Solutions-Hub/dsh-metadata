# Derwent X-ray powder diffraction (XRD) Sediment Fingerprinting

- Purpose and scope
  - Qualitative mineralogical fingerprinting of sediment from the Derwent catchment, Yorkshire, UK using X-ray diffraction (XRD).
  - Field collection from diverse soil types and in-stream sediment along the river channels.

- Methods
  - Sample collection: grab samples from multiple sites around the catchment, including river banks and bars.
  - Field processing: samples dried, sieved, and powdered.
  - Instrumentation: Bruker D8 XRD used for analysis.
  - Analytical approach: qualitative phase analysis to identify minerals present in sediment.

- Data content and format
  - Primary data file format: CSV.
  - Data included:
    - Sample/site identifiers (e.g., Derwent_XRD_SedimentFingerprinting_(n)).
    - Site name and location data (X and Y coordinates) for each sample.
    - XRD outputs: 2 theta values (degrees) and corresponding counts (raw counts).
  - Data units:
    - 2 theta: degrees.
    - Counts: raw intensity counts.
  - Data status: raw XRD output; no phase-table processing applied yet.

- Data structure and coverage
  - Structure: each row corresponds to a data point from a specific sample, with associated site name and coordinates.
  - Site naming examples: Lower Rye u/s Derwent confluence River 1, Final Derwent River, Jugger Howe Soil 1–3, Boxa Woods, Spital Beck River 1–2, etc.
  - Geographic scope: sampling across the Derwent River system; coordinates provided for site localization.
  - Note: data listing contains many entries with X and Y coordinates; some portions of the text appear garbled or inconsistent, indicating possible formatting or transcription issues in the dataset metadata.

- Quality control and data quality
  - Instrument calibration indicated.
  - Data are raw outputs, not processed against phase reference tables; users will need to apply phase identification (e.g., using standard phase tables) to interpret mineral content.

- How to use and potential data products
  - Use case: combine raw 2 theta and counts with site metadata to explore mineralogical fingerprints across sites.
  - Next steps for users: apply phase identification to translate 2 theta/count data into mineral components; align with site coordinates for mapping.
  - Potential outputs for end users:
    - Self-serve exploration dashboards or pivot-table style views of mineral signals by site.
    - Maps showing spatial distribution of XRD features.
    - Comparative reports across sites to identify patterns in sediment mineralogy.

- Practical considerations for data work
  - Metadata completeness: verify and standardize site names and coordinates; resolve any garbled entries in the dataset.
  - Coordinate reference: clarify the spatial reference system for X/Y coordinates to enable accurate mapping.
  - Data integration: consider linking with additional site data (e.g., soil type, catchment location) to enhance interpretation and downstream dashboards.