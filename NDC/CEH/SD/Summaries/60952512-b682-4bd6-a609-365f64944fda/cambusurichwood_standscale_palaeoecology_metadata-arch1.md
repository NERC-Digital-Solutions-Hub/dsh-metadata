# Metadata

## Overview
- Metadata for a multi-proxy palaeoecological study of Cambusurich Wood, Scotland (OS grid NN 62741 34679).
- Stand-scale analysis focusing on long-term dynamics in an ancient temperate woodland of high conservation value.
- Duplicate peat cores collected in October 2020 from a small peat-filled hollow within Cambusurich Wood SSSI.
- Two core sets: one for microfossil analyses (pollen, non-pollen palynomorphs, spores, microcharcoal) and one for macrofossil and macrocharcoal analyses.
- Chronology and loss-on-ignition (LOI) are derived from the same core used for microfossils.
- Funded by Natural Environment Research Council (Grant NE/S007377/1).

## Datasets and key fields

- CambusurichWood_Raw_Microfossil_Data.csv
  - Sample_mid_depth: subsample mid-depth (cm); 1 cm resolution.
  - Sample_volume: sample volume (cm3).
  - Exotic_lycopodium_added: number of exotic lycopodium spores added for pollen concentration calculations (Stockmarr 1971).
  - Exotic_lycopodium_counted: number of exotic lycopodium spores counted.
  - Exotic_lycopodium_tablets_added: number of exotic lycopodium tablets added.
  - Rows 6-120: raw counts for pollen, spores, non-pollen palynomorphs, and microcharcoal.

- CambusurichWood_Raw_Macrofossil_Data.csv
  - Sample_mid_depth: subsample mid-depth (cm); 2 cm resolution.
  - Sample_volume: sample volume.
  - Rows 3-76: macrofossil data per sample (depth) including seeds (s), bracts (br), male catkin scales (m.cat), buds (bd), twigs (tw), cones (c), bud scales (bs), nutlets (n), florets (f), utricles (utr), megaspores (ms), fruit varves (fv), leaves (lf), leaf branches (lb), and undifferentiated remains.
  - Data types: raw counts or four-point semi-quantitative scale (x rare 1–10, xx occasional 10–50, xxx frequent 10–100, xxxx abundant >100).
  - Rows 77-80: macrocharcoal counts by fragment size classes (0–1 mm, 1–2 mm, 2–3 mm, 3–4 mm).

- CambusurichWood_Chronological_Controls.csv
  - Depth_cm: sample depth for chronological controls (AMS 14C or 210Pb).
  - Lab-code: unique sample identifier (AMS radiocarbon dates only).
  - Material: description of chronological control or radiocarbon-dated material.
  - 14C_Age: age in years before present.
  - Error: age uncertainty in years.

- CambusurichWood_Loss_On_Ignition.csv
  - Mid_depth_cm: mid-depth of 1 cm peat sample.
  - Loss-on-ignition: LOI percentage following Heiri et al. (2001) protocol.

- CambusurichWood_Troels_Smith.csv
  - Depth_cm: sediment description boundaries (cm).
  - Components: sediment components described using the Troels-Smith (1955) system.

- Supporting literature
  - References underpinning methodologies and pollen/macro remains interpretation (e.g., Bennett 1995–2007; Field et al. 2000; Heiri et al. 2001; Stockmarr 1971; Troels-Smith 1955; plus tools for NPPs and pollen analyses).

## Study context and location details
- Location: Cambusurich Wood, Scotland (OS grid NN 62741 34679).
- Site characteristics: a small peat-infilled forest hollow within a larger woodland; targeted for long-term dynamics of ancient temperate woodland.
- Chronology approach: relies on AMS radiocarbon dating and 210Pb where applicable, integrated with LOI measurements and sediment descriptions.

## Analytical approach and aims for data users
- Purpose: enable data-driven identification of correlations, trend reconstruction, and predictive insight regarding actions affecting woodland dynamics.
- Data integration: multiple proxies (microfossils and macrofossils) with depth-based resolution allow cross-validation of vegetation signals and disturbance indicators (e.g., macrocharcoal, microcharcoal).
- Quality considerations: data include raw counts and semi-quantitative scales; provenance is clearly documented, with a shared core used for chronology and LOI.
- Potential analyses for analysts:
  - Correlate pollen/spore signals with macrofossil assemblages to infer vegetation composition changes over depth/time.
  - Link LOI variations to organic content and preservation, and align with climatic or disturbance events inferred from proxies.
  - Use chronology controls to construct age-depth models and assess timing of ecological shifts.
  - Compare sediment descriptions (Troels-Smith) with biological proxies to interpret depositional environments and disturbances.

## Proximity to data challenges and considerations (analyst-centric)
- Single-site study: limited generalizability beyond Cambusurich Wood, though valuable for site-specific long-term dynamics.
- Depth resolution: microfossil data at 1 cm increments; macrofossil data at 2 cm increments, which may constrain fine-scale temporal interpretation.
- Data standardization: macrofossil tallies include semi-quantitative scales, requiring careful interpretation when combining with raw counts from microfossils.
- Data accessibility: tables and descriptions are embedded in CSVs; linkage to the broader literature is provided via the listed references.

## Access and provenance
- Data generated as part of a funded project (NERC NE/S007377/1) with explicit documentation of core sampling, analytical methods, and supporting references.
- Core set and analyses are associated with Cambusurich Wood SSSI, providing a well-documented natural archive for paleoenvironments and woodland dynamics.