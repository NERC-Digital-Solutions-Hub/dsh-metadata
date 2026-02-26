# Loch Leven long-term monitoring dataset

- Description: Dataset from the Loch Leven long-term monitoring programme in Scotland, collected as part of UK-SCAPE WP7 LEVEN. Covers lake water chemistry, crustacean zooplankton, and associated sampling/analysis methods; output is a single CSV with detailed column metadata.

## Spatial extent and sampling design

- Sampling regime: Fortnightly visits to two main sites per occasion.
- Sites:
  - Harbour (Site H)
  - Reed Bower (Site RB / RB5)
  - Sluices / Outflow (Site L / Sl8)
- Location coordinates (EPSG:27700, UK National Grid):
  - Harbour: Easting 312251, Northing 701670
  - Reed Bower: Easting 313568, Northing 701141
  - Sluices / Outflow: Easting 317004, Northing 699380
- Accessibility constraints: Weather, ice, and resource limitations may prevent sampling; Reed Bower is boat-access only, Sluices can be sampled from shore or boat.
- Data structure: Determinands recorded per site with site-specific columns; “Outlet” values are referenced as “Sluices” for dataset consistency.

## Measurements and data types

- In situ measurements (at or near sampling): Conductivity (µS/cm), pH, temperature, and Secchi depth (Secchi depth at Reed Bower only).
- Water samples (duplicates) collected from each site for laboratory analyses:
  - Soluble Reactive Phosphorus (SRP, µg P/L)
  - Total Soluble Phosphorus (TSP, µg P/L)
  - Total Phosphorus (TP, µg P/L)
  - Chlorophyll a (chla, µg/L)
  - Soluble reactive silicate, total diatom silica (sample handling detailed in methods)
- Bottle methods and filtration details provided; samples processed within hours to days as specified.
- Weather observations: Cloud cover, wind direction/force (when possible); wind force mapped to Beaufort scale with a lookup table.

## Crustacean & Zooplankton data

- Taxa counted per litre (ind/L) at Reed Bower and Sluices:
  - Daphnia hyalina, Eudiaptomus gracilis (adults + copepodites I-V), Eudiaptomus nauplii
  - Cyclopodidae (total, incl. Cyclops abyssorum and C. vicinus)
  - Cyclops abyssorum, Cyclops vicinus (adults + copepodites I-V)
  - Cyclopodidae nauplii, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus
- Sampling methods:
  - Reed Bower: 4 m net hauls, 120 µm mesh
  - Sluices: 30 L surface water filtered through 120 µm net
- Laboratory processing: Subsampling (4 sub-samples counted per sample), taxonomic identification to practical resolution, counting via binocular microscope, counts converted to ind/L and archived.

## Sampling, measurement and analysis methods (chemistry)

- Duplicate 2 L water samples per site; integrated sampling at Reed Bower using a weighted PVC sampler; Sluices sampled near surface.
- Analyses:
  - SRP via Murphy & Riley (1962) method; absorbance at 882 nm
  - TP via digestion (sulphuric acid and persulphate) to SRP; Wetzel & Likens (2000)
  - TSP similar to TP but filtered
- Filtration, storage, and handling details provided; chlorophyll a via 400 mL filtered through GF/C filter.

## Data processing and quality assurance

- Data processing: Import script in R; decisions to standardize values (e.g., wind force from first value in ranges).
- Replicate handling: Values from Hach probes (conductivity, pH, DO) are screened using Median Absolute Deviation (MAD). pH values are converted to 10^pH for MAD calculations, then back-transformed; means computed and values rounded (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
- QA: Automated and manual checks for data entry errors and out-of-range values; unusual values investigated and corrected as needed.

## Data format and column descriptions (CSV schema)

- Storage: All data in a single CSV; missing readings marked as NA.
- Column naming: Descriptive names with determinand, site, and units; columns cover:
  - Date, Week of Year
  - Weather: Cloud cover, Wind direction, Wind force
  - Lake/site metrics: Water depth (Depth_m), Secchi depth (Secchi_m), water level, etc.
  - Water chemistry: Conductivity (µS/cm), Temperature (°C) for conductivity measurement, DO (mg/L and %), pH, pH temperature
  - Phosphorus: TP, SRP, TSP (multiple replicates where applicable)
  - Chlorophyll a: chla (µg/L) replicates
  - Zooplankton: Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Cyclopod nauplii, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus (all as ind/L; replicates per site)
- Site-specific prefixes: RB and L denote Reed Bower and Sluices respectively; H denotes Harbour-related measurements where applicable.
- Column 3: Detailed definitions and units provided in Table 3 (core reference for column semantics).

## References and further reading

- Methods and datasets cited for chemical analyses, zooplankton identification, and long-term Loch Leven studies.
- Supporting literature and project reports listed for context and replication.