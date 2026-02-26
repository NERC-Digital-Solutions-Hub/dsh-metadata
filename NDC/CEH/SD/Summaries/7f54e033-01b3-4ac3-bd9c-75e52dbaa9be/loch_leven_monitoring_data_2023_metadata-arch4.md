# Abstract

- Overview: Description of the Loch Leven long-term monitoring dataset, collected as part of a continuing programme since 1968, with recent work by NERC / UK Centre for Ecology & Hydrology. Document covers data nature, sampling and analysis methods, data processing, and output format. Project context: UK-SCAPE WP7 LEVEN.

- Sampling regime and sites:
  - Sampling typically fortnightly.
  - Two main sampling sites visited each occasion: Reed Bower (RB) and Sluices/Outflow (L). Harbour (H) is referenced in site codes but not a primary sampling site for routine collection.
  - Opportunistic constraints may prevent sampling (resource limits, bad weather, ice). When boats are unsafe, only Sluices may be sampled; in extreme cases neither site is visited.

- Measurements and analyses:
  - In situ measurements: conductivity, pH, temperature, and Secchi depth (Secchi depth measured at Reed Bower; others measured in the field as applicable).
  - Water samples collected in duplicates for laboratory analyses: soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), soluble reactive silicate, total diatom silica, total phosphorus (TP), and chlorophyll a (via filtration).
  - SRP and TP/ TSP measurements described with specific chemical methods (Murphy & Riley 1962 for SRP; Wetzel & Likens 2000 for TP with digestion steps; TSP via filtered sample).
  - Weather data (cloud cover, wind) recorded at Reed Bower when possible; wind force described using a custom Beaufort-like scale.

- Crustacean and zooplankton data:
  - Densities of crustacean zooplankton recorded as individuals per litre for multiple taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopidae, Bosmina longirostris, Leptodora kindtii, Bythotrephes longimanus, Chydoridae, Ceriodaphnia sp., Polyphemus pediculus, etc.).
  - Sampling at Reed Bower (4 m net haul, 120 µm) and Sluices (large-volume surface water net), preserved in formaldehyde, counted under a microscope, and converted to ind/L.
  - Data include zeros (recorded when not observed) and NAs (missing values). As of 2022–2023, column names were updated for consistency, and two new taxa were added.

- Data processing and quality control:
  - An R-based import script was used to preprocess data before database ingestion, including handling wind value ranges and probe replicates.
  - Probe replicates (conductivity, pH, dissolved oxygen) are checked: values outside Median Absolute Deviation (MAD) are handled; pH values are converted to 10^pH for MAD calculations, then transformed back for final reporting. Rounding applied (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
  - Inter-calibration: HQ30d replaced by HQ4300; calibration ensures consistency across instrument models.
  - Automated and manual QA checks performed on all data; out-of-range values investigated and corrected as needed.

- Output format and metadata:
  - Data stored in a single CSV file with detailed column descriptions, units, and site information; missing values marked as NA.
  - Column naming conveys determinand, site, and units; 2023 updates standardized encodings ( litres → L, µ → u, ° → deg) and added Ceriodaphnia_sp. columns.
  - Table 3 provides comprehensive descriptions for all columns (date, site, wind/weather variables, depth, Secchi, conductivity, temperature, dissolved oxygen, pH, phosphorus forms, chlorophyll a, and zooplankton densities).

- References and further reading:
  - Method and analysis references for chemical measurements (Golterman et al. 1978; Murphy & Riley 1962; Wetzel & Likens 2000).
  - Zooplankton taxonomy references (Dussart & Defaye 1995; Einsle 1996; Flößner & Kraus 1986; Harding & Smith 1974; Scourfield & Harding 1966).
  - Related reporting and compilations (Dudley et al. 2012; Spears & May 2012).

- Data format specifics:
  - Columns cover: sampling date, week of year, water level, cloud cover, wind direction/force, depth, Secchi depth, conductivity, temperature, dissolved oxygen (mg/L and percentage), pH, total and soluble phosphorus measurements (TP, SRP, TSP), chlorophyll a, and a broad suite of crustacean zooplankton taxa with densities (ind/L). 
  - Site identifiers used: H (Harbour), RB (Reed Bower), L or Sl8 (Sluices/Outflow); units and descriptive labels provided for each column.
  - As of 2023: internal encoding improvements and additional taxa (Ceriodaphnia_sp.) included. Column order preserved; changes focused on naming consistency and readability.