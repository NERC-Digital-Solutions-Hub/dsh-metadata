# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component Carbon and nitrogen content in soils and vegetation from calcareous grassland, heathland and woodland sites in Dorset, 2017-2018

- Purpose and scope
  - Documents a dataset on carbon and nitrogen content in soils and vegetation across calcareous grassland, heathland, and woodland sites in Dorset, 2017–2018.
  - Built from a historic baseline (Good, 1931–1939) to examine how ecosystem services vary with habitat condition.
  - Includes both soil chemistry data and vegetation chemistry data collected in field surveys.

- Experimental design and site selection
  - Good (1930s) survey used to identify target habitats; archive available via Dorset Environmental Records Centre.
  - Thirteen calcareous grassland, thirteen heathland, and twelve woodland sites were surveyed.
  - Subsampling integrated multiple data sources to identify current habitat types: UK Land Cover Map 2007, Natural England Priority Habitat Inventory, SSSIs, Horsfall (1981), Dorset Heathland survey (Rose et al., 2000), and Higher Level Stewardship data.
  - Habitat gradients defined per habitat type (calcareous, heathland, woodland) across conditions from degradation to restoration or SSSI-quality status.
  - Gradient categories include: calcareous grassland (SSSI-quality; resting; restored; improved grassland), heathland (conifer plantation; high gorse; heathland in SSSI-quality), and woodland (coniferous plantation; broadleaf; ancient woodland in SSSI-quality).

- Data collection methods
  - Sampling units: 50m x 50m plots with random placement within the original Good survey area (via ArcGIS).
  - Soil sampling: four 15 cm depth cores per plot; two air-dried and sieved to 2 mm; analyzed by Lancaster Laboratories (UKCEH) using oxidative combustion and thermal conductivity detection.
  - Analytical procedure: calibration with Acetanilide; standards and blanks included; CRM standards run periodically; limits of detection: C 2.0%, N 0.12%.
  - Bulk density: measured from two additional soil samples; cores oven-dried and weighed; bulk density calculated with a specified formula.
  - Vegetation sampling: five 50 cm quadrats per plot; all vegetation layers collected, dried, and weighed; shrub species identified; analysis performed by UKCEH following soil methods.
  - Data collection quality: field ecologists with extensive experience; data checked for anomalies; consistent recording into structured spreadsheets.

- Data structure and column headings
  - DVNP_Soil_Chemistry_data
    - Site_No (1-39; CEH site number)
    - C_total (carbon concentration in percent)
    - N_total (nitrogen concentration in percent)
    - Bulk_Density (soil bulk density in g cm^-3)
  - DVNP_VegetationChemistry_data
    - Site_No (CEH site number)
    - Quad_No (1-4; with Combined_all option)
    - Vegetation_type (e.g., fresh vegetation, litter)
    - Vegetation_layer (Herb, Scrub, etc.)
    - C_total (carbon concentration in percent)
    - N_total (nitrogen concentration in percent)
    - Dry_Weight (weight of dried vegetation sample in grams)

- Habitat gradient lookup
  - A comprehensive mapping table linking 1940 habitat classifications to 2017 habitat classifications to define the proposed gradient categories.
  - Examples include:
    - Calcareous → Calcareous grassland (SSSI quality)
    - Calcareous → Improved grassland
    - Heathland → Coniferous plantation on heathland
    - Heathland → Gorse high heathland
    - Woodland → Broadleaf woodland
    - Woodland → Ancient woodland (SSSI quality)
  - Note: care taken to exclude ancient woodland plantations from selection.

- Data provenance and quality
  - Data collected by experienced field ecologists; consistent team across surveys.
  - Data quality assured via anomaly checks and standardized recording procedures.
  - Clear documentation of data sources for site selection and habitat classification to support reproducibility and cross-study comparisons.

- References
  - Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
  - Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
  - Natural England (2014) Sites of Special Scientific Interest and historical monuments
  - Natural England (2015) Priority Habitats' Inventory version 2.1
  - Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125

- Potential data use and outputs
  - The dataset enables baseline comparisons of carbon and nitrogen across habitat types and degradation/restoration gradients.
  - Structured data allow for cross-walking historical Good survey data with contemporary habitat classifications.
  - Facilitates creation of data products (tables and summaries) to explore habitat condition effects on soil and vegetation chemistry.