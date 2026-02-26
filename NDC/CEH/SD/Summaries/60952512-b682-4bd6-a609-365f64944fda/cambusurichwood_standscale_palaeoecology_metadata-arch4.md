# Metadata

## Overview
- Metadata for a palaeoecological dataset from Cambusurich Wood, Scotland (OS grid NN 62741 34679) examining long-term dynamics in ancient temperate woodland of high conservation value.
- Based on duplicate peat cores collected in October 2020 using a Russian corer from an 8.5 x 7 m peat-infilled hollow (Camb).
- Two parallel analytical streams: microfossil analyses (pollen, non-pollen palynomorphs, spores, microcharcoal) and macrofossil/macrocharcoal analyses; chronology and loss-on-ignition (LOI) derived from the same core as microfossils.
- Funded by Natural Environment Research Council (Grant NE/S007377/1).

## Data Content

- CambusurichWood_Raw_Microfossil_Data.csv
  - Sample_mid_depth (cm) – sub-sample mid-depth
  - Sample_volume (cm3)
  - Exotic_lycopodium_added – number of exotic lycopodium spores added for pollen concentration calculations
  - Exotic_lycopodium_counted – number counted in analyses
  - Exotic_lycopodium_tablets_added – number of lycopodium tablets added
  - Rows 6-120 – raw counts for pollen, spores, non-pollen palynomorphs, and microcharcoal

- CambusurichWood_Raw_Macrofossil_Data.csv
  - Sample_mid_depth – 2 cm peat sub-sample mid-depth
  - Sample_volume
  - Rows 3-76 – raw counts of macrofossils per sample including seeds, bracts, catkin parts, buds, twigs, cones, leaf parts, megaspores, fruit varves, leaves, etc.
  - Data presented as raw counts or a four-point intensity scale: x (rare), xx (occasional), xxx (frequent), xxxx (abundant)
  - Rows 77-80 – macrocharcoal counts by size classes (0–1 mm, 1–2 mm, 2–3 mm, 3–4 mm)

- CambusurichWood_Chronological_Controls.csv
  - Depth_cm – sample depth for chronological controls (AMS radiocarbon dating or 210Pb)
  - Lab-code – unique sample identifier (AMS dates)
  - Material – description of chronological control or dated material
  - 14C_Age – sample age (years before present)
  - Error – age uncertainty (years)

- CambusurichWood_Loss_On_Ignition.csv
  - Mid_depth_cm – mid-depth of 1 cm peat sample
  - Loss-on-ignition – percentage LOI following Heiri et al. (2001)

- CambusurichWood_Troels_Smith.csv
  - Depth_cm – sediment description boundaries (cm)
  - Components – sediment components described using Troels-Smith (1955) system

## Data Provenance and Methods
- Cores collected October 2020; duplicate cores used for microfossil and macrofossil analyses.
- Chronology and LOI derived from the same core used for microfossil analyses.
- LOI method aligned with Heiri et al. (2001) protocol; sediment descriptions follow Troels-Smith system (1955).
- Supporting literature provided for pollen types, plant macrofossil analyses, and palynological methods.

## Data Quality and Standards
- Data are raw counts and semi-quantitative scales; depth and volume units specified.
- Proxies include microfossils, macrofossils, macrocharcoal, LOI, and sediment descriptions, enabling multi-proxy analyses.
- Depth alignment across datasets relies on mid-depth/sub-sample depth references; careful harmonization needed for integrated analyses.
- Metadata lists sources and methods, supporting reproducibility and comparability with related studies.

## Usage and Best Practices for Data Leaders
- Assess data suitability for cross-proxy synthesis (microfossil vs macrofossil vs charcoal) and align depth scales.
- Verify data quality, unit consistency, and provenance across files; maintain cross-file sample identifiers (depths, lab codes).
- Use supporting literature to interpret pollen types, LOI measurements, and Troels-Smith sediment classifications.
- Plan data governance: ensure versioning, clear licensing, data dictionaries, and discovery metadata to support future reuse.
- Consider data integration with wider data networks to enhance data discoverability and collaborative opportunities (co-ownership of data products).

## Supporting Literature
- Bennett, K., 1995-2007. Catalogue of pollen types.
- Field, Beaulieu, Guiot, Ponel, 2000. Palaeoecology study (macro/microfossils, insect investigations).
- Heiri, Lotter, Lemeke, 2001. LOI methodology.
- Miola, 2012. Tools for Non-Pollen Palynomorphs (NPPs).
- Moore, Webb, Collinson, 1991. Pollen Analysis.
- Nakagawa et al., 1998. Pollen extraction methods.
- Stockmarr, 1971. Tablets with spores for absolute pollen analysis.
- Troels-Smith, 1955. Sediment description system.