# Abstract

- Long-term Loch Leven monitoring dataset (Scotland, UK) collected as part of a programme that began in 1968 and is ongoing; historically managed by NERC and, most recently, the NERC / UK Centre for Ecology & Hydrology; under project UK-SCAPE WP7 LEVEN.

- Scope of data:
  - Water chemistry and physical measurements from fortnightly sampling at two main sites (Reed Bower and Sluices/Outlet).
  - Crustacean zooplankton densities from Reed Bower and Sluices.

- Data collection and processing:
  - Field measurements include conductivity, pH, temperature (in situ) and Secchi depth (Reed Bower only); water samples collected at each site for laboratory analyses.
  - Laboratory analyses cover soluble reactive phosphorus (SRP), total phosphorus (TP), total soluble phosphorus (TSP), soluble reactive silicate, total diatom silica, chlorophyll a; detailed methods referenced (Murphy & Riley 1962; Wetzel & Likens 2000; etc.).
  - Weather data (cloud cover, wind direction, wind force) recorded at Reed Bower when possible.

- Crustacean & Zooplankton:
  - Counts of multiple zooplankton taxa per litre across the two sites; preserved samples processed and counted in the lab; counts converted to ind/L.

- Data processing and quality control:
  - An import script (R) processes data prior to database entry; decisions documented (e.g., wind force handling, probe replicate filtering with median absolute deviation, pH transformations for calculations).
  - Automated and manual quality assurance checks performed; unusual values investigated and corrected when appropriate.

- Data format and documentation:
  - All data stored in a single CSV file with columns detailing determinands, site conditions, lake chemistry, and zooplankton counts; missing values marked as NA.
  - Column descriptions and structure documented in Table 3; comprehensive references provided for methods and related literature.

- Key methodological details:
  - Reed Bower sampling uses integrated water column collection; Sluices sampling typically 10 cm below the surface or from a boat/shore depending on conditions.
  - Duplicate field samples collected for most determinations; specific filtration and storage procedures outlined for each chemical parameter.

- Additional context:
  - The document provides site IDs, coordinates, and a map reference for Harbour, Reed Bower, and Sluices; a consistent data coding scheme is used across the Loch Leven monitoring programme.