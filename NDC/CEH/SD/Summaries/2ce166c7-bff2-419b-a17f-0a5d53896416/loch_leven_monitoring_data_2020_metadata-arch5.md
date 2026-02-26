# Loch Leven long-term monitoring dataset

- Comprehensive description of data from Loch Leven, a lowland lake in Scotland, collected as part of a long-term monitoring programme initiated in 1968 and continuing under NERC/UK Centre for Ecology & Hydrology (UKCEH). Document covers data nature, sampling/analysis methods, data processing, and output format under project UK-SCAPE WP7 LEVEN.

## Overview of data and scope
- Long-term, multi-institution dataset focusing on lake water chemistry, physical properties, and crustacean zooplankton.
- Two primary data streams:
  - Water chemistry and physical measurements (conductivity, pH, temperature, Secchi depth, etc.).
  - Crustacean zooplankton densities (ind/L) for multiple taxa.
- Data stored as a single CSV file with extensive metadata in column names; missing values represented as NA.

## Sampling regime and sites
- Fortnightly sampling with two sites per occasion:
  - Reed Bower (RB) — boat access; includes integrated depth sampling method.
  - Sluices / Outflow (L or Sl8) — sampled from surface or shore; boat use variable.
- Sampling occasionally missed due to weather, resources, or ice; when boat usage is restricted, only the Sluices site may be sampled.
- Site identifiers and locations:
  - Harbour (H)
  - Reed Bower (RB / RB5)
  - Sluices / Outflow (L / Sl8)
- Geographic coordinates provided for site locations.

## Measurements, sampling, and analysis
- In situ measurements: conductivity, pH, temperature (with hand-held probes); Secchi depth measured at Reed Bower.
- Water sampling:
  - Duplicate 2 L samples per site; RB uses integrated sampling with a weighted PVC tube; Sl8 uses a surface bottle.
  - Laboratory analyses performed on collected samples for:
    - Soluble Reactive Phosphorus (SRP)
    - Total Phosphorus (TP)
    - Total Soluble Phosphorus (TSP)
    - Soluble reactive silicate
    - Total diatom silica
    - Chlorophyll a
- Analytical methods and storage:
  - SRP via Murphy & Riley (1962) method.
  - TP/TSP following Wetzel & Likens (2000) approach with persulfate digestion for TP.
  - Chlorophyll a analysis via filtration and freezing storage; SRP/TP/TSP sub-samples preserved appropriately.
- Weather data (where possible): cloud cover, wind direction, wind force; wind force mapped to Beaufort scale with a defined lookup.

## Crustacean & Zooplankton data
- Densities (ind/L) for a suite of crustacean zooplankton taxa at Reed Bower and Sluices:
  - Daphnia hyalina; Eudiaptomus gracilis (adults + copepodites I–V); Eudiaptomus nauplii; Cyclopodidae; Cyclops abyssorum; Cyclops vicinus; Cyclopod nauplii; Bosmina longirostris; Leptodora kindti; Bythotrephes longimanus; Chydoridae; Polyphemus pediculus (RB only for some taxa).
- Data collection and processing:
  - RB: 4 m net haul (120 µm mesh).
  - SlU: 30 L surface water passed through 120 µm net.
  - Preservation in 4% formaldehyde; counting under low-power microscope; four sub-samples counted per sample.
  - Counts converted to densities (ind/L) and preserved samples archived.
- Taxa are identified to species level when practical; zeros indicate non-detection within resolution, not necessarily true absence.

## Data processing, quality assurance, and reproducibility
- Data processing: R-based import script with specific handling rules:
  - Wind force: if a range is provided (e.g., 4-5), the first value is used.
  - Probe replicate values (conductivity, pH, DO, and related temperatures) screened using Median Absolute Deviation (MAD):
    - Median ± MAD used to accept or reject replicates.
    - pH values transformed to 10^pH for MAD calculations, then back-transformed for final value.
    - Final values rounded: pH/DO concentration to 2 decimals; conductivity, DO%, and temperatures to 1 decimal.
- Quality assurance: automated and manual checks for data entry errors and out-of-range values; anomalies investigated and corrected where appropriate.

## Data format and column structure
- Data stored in a single CSV file with descriptive columns for:
  - Sampling date and week of year.
  - Site conditions (water level, cloud cover, wind direction, wind force).
  - Weather, depth, Secchi depth.
  - Water chemistry: conductivity, temperature, dissolved oxygen (mg/L and %), pH.
  - Phosphorus metrics: TP, SRP, TSP (with replicates where applicable).
  - Chlorophyll a concentrations.
  - Zooplankton/Crustacean densities for each taxa (per site and replicate).
- Column names include determinand, site, and units; missing data denoted as NA.
- Table 3 provides detailed descriptions for all columns (core reference for dataset interpretation).

## References and methods
- Physical and chemical analysis methods:
  - Murphy J. & Riley J. (1962) for SRP determination.
  - Wetzel R.G. & Likens G.E. (2000) for nutrient analyses.
  - Golterman H.L. et al. (1978) for general freshwater analysis methods.
- Zooplankton identification keys and taxonomic references for accurate sub-sampling and counting.

## Data governance and stewardship notes
- Provenance: long-term, multi-institutional data with clear sampling histories and lab analyses; suitable for time-series analyses and cross-site comparisons.
- Metadata completeness: site IDs, coordinates, measurement units, replication structure, and processing steps documented; processing rules are explicit to enable reproducibility.
- Limitations:
  - Possible sampling gaps due to weather or logistics.
  - Some taxa identifications may be limited by preservation and specimen condition.
- Accessibility and reuse readiness:
  - Data provided in a machine-readable CSV with comprehensive column descriptions.
  - Clear QA steps and processing rules support traceability and data quality assessment.