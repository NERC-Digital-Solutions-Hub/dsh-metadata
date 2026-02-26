# Header Descriptions for Dataset "OH_Soil_Properties"

- Overview
  - Metadata describing the header fields used for the OH_Soil_Properties dataset, enabling consistent interpretation and reuse of soil property measurements across plots and sampling times.

- Key header fields and meanings
  - Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
  - Site: Site name.
  - Sample: Sample number at that site.
  - Age: Site age since last wildfire (years).
  - Depth: Depth of soil organic horizon (cm).
  - BD: Bulk density, soil organic horizon (g cm-3).
  - CN: Ratio of total carbon to total nitrogen, soil organic horizon.
  - pH: pH of soil organic horizon.
  - LOI: Loss on ignition, soil organic horizon (% soil organic matter).
  - P: Total phosphorous, soil organic horizon (mg g -1 soil dry weight).
  - totPlfa: Total phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
  - totFung: Total fungal phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
  - totBact: Total bacterial phospholipid fatty acid content, soil organic horizon (nmol g -1 dry weight).
  - fungBact: Ratio of fungal to bacterial phospholipid fatty acid content.

- Data governance and quality considerations
  - Ensure consistent unit definitions and naming across datasets (e.g., cm, g cm-3, nmol g-1 dry weight, %).
  - Use this metadata to support data discovery, interoperability, and reuse in portals and catalogues.
  - Validate that the actual data align with these header descriptions (e.g., depth values fall within plausible soil horizons, LOI values within expected ranges).
  - Capture data provenance, measurement time, and method details to support traceability and reproducibility.

- Implications for data stewardship
  - Maintain alignment between dataset data and header descriptions; update metadata when fields are added or renamed.
  - Document data quality checks and any transformations applied during sharing (cleaning, normalization, transformation).
  - Ensure appropriate access, licensing, and update pathways so researchers can discover and rely on up-to-date metadata.


# Header Descriptions for Dataset "NH4_NO3_OH_Soil Properties"

- Overview
  - Metadata describing the header fields used for the NH4_NO3_OH_Soil Properties dataset, to support accurate interpretation of nitrogen-related soil chemistry measurements.

- Key header fields and meanings
  - Identifier: Sample Identification for measurement of each plot/gas chamber ring at each sampling time.
  - Site: Site name.
  - Sample: Sample number at that site.
  - Age: Site age since last wildfire (years).
  - NO3.ppm: NO3- concentration, soil organic horizon (parts per million).
  - NH4.ppm: NH4+ concentration, soil organic horizon (parts per million).
  - mgNO3.N: NO3- concentration, soil organic horizon (mg kg -1 soil dry weight).
  - mgNH4.N: NH4+ concentration, soil organic horizon (mg kg -1 soil dry weight).

- Data governance and quality considerations
  - Ensure consistent units (ppm and mg kg-1) and clear documentation of what the units represent.
  - Validate data integrity against the dimensional expectations (e.g., values within plausible soil nitrate/ammonium ranges).
  - Align this dataset’s metadata with the OH_Soil_Properties dataset where applicable to support cross-dataset analyses (e.g., linking depth, age, site).

- Implications for data stewardship
  - Keep header descriptions synchronized with actual data fields; record any unit conversions or methodological notes.
  - Document data quality checks and transformations applied prior to sharing.
  - Facilitate discoverability and reuse by including these descriptions in data portals and catalogues, and by providing lineage and method details for measurements.