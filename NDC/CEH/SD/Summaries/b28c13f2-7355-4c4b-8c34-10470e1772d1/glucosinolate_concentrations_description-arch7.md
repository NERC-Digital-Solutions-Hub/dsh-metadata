# Description, Experimental Design and Collection

- Study objective: Data represent glucosinolate concentrations in Brassica napus plants within FreeAir Diesel and Ozone Enrichment (FADOE) rings.
- Data provenance: Full FADOE configuration and quality control described in reference [1]; LC-MS analysis protocol described in reference [2].

## Spatial context and sampling locations

- Field locations and movement:
  - 2018: FADOE rings in a field of wheat at latitude 51.482853, longitude -0.897749.
  - 2019: Rings moved to an adjacent field at latitude 51.482374, longitude -0.895855.
- Ring and field structure:
  - Each FADOE ring has a numeric identifier ('Ring', Column B).
  - Two rings were assigned to each of four pollution treatments.

## Experimental design and data collection

- Treatments:
  - Pollutants: diesel exhaust (D), ozone (O3), diesel exhaust + ozone (D+O3), and a control (CON; natural air) (Column C).
- Aphid inoculation:
  - Inoculation levels: 50 aphids, 10 aphids, or no aphids; leaves collected from three plants per ring.
  - Aphids_present indicates whether aphids were present (Yes/No) (Column E).
- Plant sampling:
  - Plant_ID identifies plants from which leaves were sampled.
  - Sampling occurred when plants were five weeks old.
- Sample processing:
  - Leaves were freeze-dried and ground to a fine powder; up to three replicate samples analysed per ground sample (Replicate column F).
- Glucosinolate measurement:
  - Seven glucosinolates measured by LC-MS following protocol [2]:
    - Progoitrin, Glucoalyssin, Gluconapin, Glucobrassicanapin, Glucobrassicin, 4-methoxyglucobrassicin, Neoglucobrassicin (Columns G–M).
  - Totals computed:
    - Indole_GLS (Column N), Aliphatic_GLS (Column O), Total_GLS (Column P).

## Data structure and key variables (for GIS use)

- Sample identifier: Sample_ug_g-1_dw (Column A) – code based on FADOE ring, aphid treatment, plant, and replicate.
- Spatial identifiers:
  - Ring (Column B) – ring number within the field layout.
  - Field location context via recorded coordinates for 2018 and 2019 locations.
- Experimental context:
  - Pollutant (Column C) – D, O3, D+O3, CON.
  - Plant_ID (Column D) and Aphids_present (Column E) – presence/absence of aphids.
  - Replicate (Column F) – replicate number for each ground sample.
- Measured variables:
  - Individual glucosinolate concentrations (Columns G–M).
  - Aggregates: Indole_GLS (N), Aliphatic_GLS (O), Total_GLS (P).

## Data quality notes and references

- Quality control and experimental configuration details are described in reference [1].
- Glucosinolate measurement protocol via LC-MS described in reference [2].
- The dataset supports geospatial analysis of glucosinolate variation across rings, treatments, and aphid inoculation, with explicit spatial coordinates and ring-level mapping.