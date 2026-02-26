# Loch Leven long-term monitoring data

## Overview
- Data come from Loch Leven’s long-term monitoring programme (started 1968) and describe the nature of the data, sampling/analysis methods, data processing, and output format.
- Part of the UK-SCAPE WP7 LEVEN project; collected and processed by NERC/CEH and partner institutions.

## Sampling regime and sites
- Fortnightly sampling at two main sites: Reed Bower (RB) and Sluices/Outflow (L).
- Reed Bower is boat-access only; Sluices can be sampled by boat or from shore.
- If sampling is impeded (weather, ice, resources), one or both sites may be skipped.
- Site codes: Harbour (H), Reed Bower (RB/RB5), Sluices (L/Sl8) with corresponding UK National Grid coordinates provided.

## Measurements and analyses
- In situ measurements: conductivity, pH, temperature ( Secchi depth measured at Reed Bower).
- Water samples: collected as duplicates (2 L each) and analyzed in the lab for SRP, TP, TSP, soluble silicate, total diatom silica, and chlorophyll a.
- Methods:
  - SRP: Murphy & Riley (1962) with phospho-molybdenum blue; absorbance at 882 nm.
  - TP: digestion with sulphuric acid and potassium persulphate; measured similarly to SRP.
  - TSP: analogous to TP but from filtered samples.
  - Chlorophyll a: filtered from 400 ml samples.
- Weather data: cloud cover, wind direction/strength (Beaufort scale) recorded at Reed Bower when possible; wind force linked to a detailed scale table.

## Crustacean & Zooplankton data
- Densities (ind/L) of crustacean zooplankton taxa at RB and L (Reed Bower includes more taxa; L includes others).
- Sampling methods:
  - RB: 4 m net haul (120 µm mesh).
  - L: 30 L of surface water passed through a 120 µm net.
- Preservation and analysis:
  - Samples preserved in 4% formaldehyde.
  - Sub-sampling and counting under a binocular microscope; species-level identification where possible.
  - Counts converted to density per litre; samples reconstituted and archived.

## Data processing and quality assurance
- Processing done with an R import script that:
  - Handles wind values (uses first value in a range like 4-5).
  - Applies replicate checks using Median Absolute Deviation (MAD) to screen conductance, pH, and dissolved oxygen data; converts pH for processing (10^pH then back) and rounds results (pH/DO to 2 decimals; others to 1 decimal).
- QA: automated and manual checks for entry errors and out-of-range values; unusual values investigated and corrected as needed.

## Data format and column structure
- Data stored in a single CSV file with columns describing the determinand, site conditions, lake chemistry, and zooplankton counts.
- Missing values marked as NA.
- Columns cover:
  - Date, Week of Year, weather and site conditions (e.g., water level, cloud cover, wind direction, wind force).
  - Physical/chemical measurements: Depth, Secchi depth, Conductivity, Temperature, DO (mg/L and %), pH.
  - Nutrients and pigments: TP, SRP, TSP, chlorophyll a.
  - Zooplankton densities: multiple taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopodidae, Cyclops abyssorum, Cyclops vicinus, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus) at RB and L.
- Column naming includes site suffixes (e.g., RB, L) and units; detailed column descriptions are provided in accompanying documentation (Table 3).

## Practical notes for data use (Data Support perspective)
- The dataset is long-term and multi-parameter, suitable for building dashboards and self-serve analyses of lake chemistry, physics, and zooplankton dynamics.
- Users should account for potential data gaps due to sampling constraints and weather.
- Standardized site IDs and consistent measurement methods facilitate cross-site comparisons and temporal trend analyses.
- Output is primarily a well-structured CSV ready for integration into data products, with clear provenance and methodological references.