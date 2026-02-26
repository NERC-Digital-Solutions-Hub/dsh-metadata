# Derwent X-ray powder diffraction (XRD) Sediment Fingerprinting

- Purpose and scope
  - Sediment fingerprinting in the River Derwent Catchment, Yorkshire, UK
  - Samples collected from soils and instream sediment (river bars/banks), across multiple sites
  - Aims to understand mineralogical composition of sediments via XRD

- Collection, fieldwork, and lab processing
  - Field collection: grab samples from different soil types and instream sediment related to river features
  - Laboratory processing: samples dried, sieved, and powdered
  - Instrumentation: Bruker D8 XRD used for analysis

- Analytical methods and data produced
  - Qualitative mineral phases analysis conducted to identify minerals present
  - Data recorded as raw XRD output: CSV with two values per entry
    - 2 theta value
    - Counts
  - No processing done with phase tables to identify minerals in the presented data (raw output)

- Data structure and contents
  - CSV includes:
    - Sample site name
    - Location data (X and Y coordinates)
  - Large list of sampling sites with corresponding coordinates
    - Examples of site naming themes: Lower Rye u/s Derwent confluence River 1, Derwent U/S Rye River 1/2, Final Derwent River/Bank, Jugger Howe Soil series, Boxa Woods, Spital Beck, The Beck, Harwood Dale, Black Beck, Raisedale Beck, Ledge Beck, River Seph, Harwood Dale Bank, etc.
  - Some transcription entries appear garbled or incomplete in places

- Locations and geographic scope
  - Coverage around the Derwent River and surrounding catchment areas
  - Includes river mouths, bank sites, floodplains, and upland/terrestrial sites (soils and banks)

- Quality control and data provenance
  - Instrument calibration indicated
  - Data presented as raw XRD output (not phase-table processed)
  - Potential metadata issues: some entries are partially garbled or inconsistent in the transcription, which may affect interpretability and data discovery

- Implications for data reuse and governance (Data Leaders angle)
  - Data usability: can support sediment provenance and mineralogical fingerprinting, if matched with appropriate phase-table analyses
  - Metadata needs: ensure comprehensive data dictionary, units, coordinate reference system, and processing steps are documented for discoverability and reuse
  - Data standards and quality: raw data require clear provenance, calibration details, and post-processing steps to enable cross-study comparability
  - Data discoverability and collaboration: the dataset spans many sites and coordinates, offering potential for networked use with partners; requires governance around versioning, licensing, and data sharing
  - Recommendations for data strategy
    - Establish a data product that includes metadata-rich entries (site name, precise coordinates, CRS, sampling date, processing steps, instrument settings)
    - Document processing workflow from raw XRD counts to mineralogical interpretation (including any phase-table applications)
    - Implement a data dictionary and standard naming conventions to reduce garbled/transcribed metadata
    - Ensure clear data licensing and update/maintenance plan to reflect new measurements or corrections
    - Facilitate cross-partner use by providing standardized formats and crosswalks to related datasets (e.g., other catchments or sediment fingerprinting efforts)