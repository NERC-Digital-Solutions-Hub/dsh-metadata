# Land Cover Map of Great Britain (1990) Dataset Information

- Overview
  - Digital land cover dataset produced from Landsat Thematic Mapper data, 25m resolution, 25 classes.
  - First complete land cover map of Great Britain since the 1960s and first nationwide satellite-derived digital land cover map.
  - Used across government, business, and research for agriculture, ecology, conservation, forestry, environmental assessment, water, urban planning, transport, telecommunications, recreation, and mineral extraction.
  - Examples of applications: detecting changing land cover, mapping bracken for health studies (ticks), motorway environmental assessments, planning telecom networks.

- Data structure and classification
  - Two product levels:
    - 25m data with 25 target classes (A–Q plus UNCLASSIFIED).
    - 1km summary data aggregating into 17 key classes (proportions per 1km cell, as integer percentages).
  - 25m data stores a single value (0–25) per grid cell; 1km data stores per-class percentage coverage within each 1km cell.
  - Classification approach: Landsat TM, supervised maximum likelihood; combines summer and winter imagery to improve accuracy.
  - Class descriptions cover a comprehensive set of land covers, including sea/estuary, inland water, coastal bare ground, saltmarsh, various grassland types, pastures, moorlands, bracken, shrubs/woodlands, bogs, tilled land, suburban/rural development, urban development, inland bare ground, and unclassified areas.
  - Note: Subclasses exist (e.g., many grassland types) but are aggregated to ecologically meaningful target classes; mapping is constrained by minimum mappable size and spectral separability.

- Spatial resolution, registration, and accuracy
  - Spatial resolution: 25m grid (coarser summary available at 1km).
  - Minimum map-able area: around 0.125 ha (2 pixels) in practice, with typical effective minimum closer to 1 ha.
  - Registration: Landsat-derived maps aligned with field maps; average positional displacement about 0.8 pixels (≈20 m); most areas require no shift or only small adjustments.
  - Accuracy: based on ground-truth comparisons; overall accuracy realistically around 80–85%, though reported correlations vary by comparison method and class definitions.
  - Main sources of error: misclassification of mixed boundary (edge) pixels, temporal changes between dates, and differences in class definitions between ground surveys and satellite classification.

- Data access, licensing, and usage
  - Stand-alone data available for specific areas at 25m or 1km resolution (percentage or dominant value dataset for 1km).
  - Licensing: license agreements required, with options from single-user to corporate multi-user; data access tailored to end use.
  - Data charges: three bands (commercial, non-commercial, research); UK academics may receive further reductions.
  - Contact and delivery: CEH Wallingford, tel +44 (0)1491 692315; email spatialdata@ceh.ac.uk; areas provided under licence with options to customize licensing.
  - Data can be requested for any area; 1km data includes 17 key classes; 25m data includes 25 target classes (A–Q) plus UNCLASSIFIED.

- Practical notes for analysts
  - Be mindful of the distinction between land cover (what is on the ground) and land use (how land is used); imagery timing affects classification (summer vs winter).
  - Accuracy reflects average error rates; local accuracy may vary by region, class, and scale.
  - When combining 25m and 1km data, ensure interpretability of class definitions and consider potential time differences between imagery dates.
  - Appendices provide practical mapping details, including colour schemes for visualization (Appendix 2) and guidance for using the dataset (Appendix notes).

- Appendices and updates
  - Appendix 2: Colour recipe for LCM1990 mapping is provided.
  - Land Cover Map 2000 is now available; information, sample data, and download options are available via the Countryside 2000 portal.
  - References and notes include guidance on accuracy assessment and methodological considerations; feedback via a Data Assessment Report (DAR) form is encouraged.

- Additional considerations
  - Unclassified area remains around 2% in 25m data; unclassified proportion in 1km data is inferred as 100 minus sum of the 17 key-class bands.
  - Data supplied with metadata and licensing to enable discoverability and reuse; ongoing developments and improvements reflected in subsequent versions (e.g., LCM2000).