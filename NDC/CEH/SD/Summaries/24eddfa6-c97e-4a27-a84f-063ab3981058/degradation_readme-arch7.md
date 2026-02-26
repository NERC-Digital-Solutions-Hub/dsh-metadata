# Degradation characteristics of bio-based teabags buried in soil, UK, November 2021 - June 2022

## Overview
- A multi-file dataset documenting chemical deterioration, material changes, and composition of three anonymised bio-based PLA: cellulose teabags after 7 months buried at 10 cm depth in UK soil (Nov 2021–Jun 2022).
- Funded by NERC BIO-PLASTIC-RISK project; associated with Courtene-Jones et al. (2024).
- Intended to support analysis of degradation processes and potential environmental implications, with data designed for subsequent integration into data products and map-based visualizations.

## Data files and contents
- Degradation_Mass.csv
  - Measures teabag mass loss during 7-month burial.
  - Columns: teabag ID (A/B/C), Time (months), initial_teabag_mass (g), final_mass (g), mass_loss (g), Mass_loss_percent (%).
- Degradation_PLA.csv
  - Proportion of PLA in teabags and changes after burial.
  - Columns: teabag ID (A/B), Time (months), PLA_content (%).
  - Note: data for Tbag-C not included.
- Degradation_crystallinity.csv
  - Crystallinity changes after burial.
  - Columns: Tbag (A/B), Time (months), crystallinity (%).
  - Note: no data for Tbag-C.
- Degradation_prGCMS_TbagA.csv
- Degradation_prGCMS_TbagB.csv
- Degradation_prGCMS_TbagC.csv
  - Pyrolysis-GCxGC-TOF MS chemical composition data for each teabag type.
  - Columns include: 1tR (retention time 1st column, minutes), 2tR (retention time 2nd column, seconds), Compound (chemical name), ions (main ions).
  - Data presented separately per teabag type (A, B, C).

## Methods and calculations
- Mass loss
  - mass_loss_percent = 100 - (final_mass / initial_teabag_mass) × 100
- PLA composition
  - Proportion of cellulose:PLA determined by dissolving PLA in chloroform, filtering, drying, and calculating cellulose:PLA as cellulose_mass / (cellulose_mass + PLA_mass) and PLA_mass / (cellulose_mass + PLA_mass).
- Crystallinity
  - Calculated from DSC data as: Crystallinity (%) = [(∆Hm − ∆Hcc) / ∆H100%] × 100
  - ∆Hm: enthalpy of melting; ∆Hcc: enthalpy of cold crystallisation; ∆H100% = 93 J/g for 100% crystalline PLA.
  - Enthalpy precision: 0.1%.
- Chemical characterization
  - Py-GCxGC-TOF MS performed on 80–100 µg samples; pyrolysis at 600 °C for 30 s, with detailed GC/MS configuration provided.
  - Data processed with ChromSpace; compounds identified against NIST MS library.

## Spatial and GIS-related context
- Data describe degradation metrics over time for specific teabag samples but do not include explicit geospatial coordinates.
- Potential GIS use:
  - Join degradation metrics to sampling location data if georeferenced (e.g., burial plots, soil properties, land-use layers).
  - Create time-series maps showing changes in mass loss, PLA content, and crystallinity across sites/plots.
  - Overlay chemical fingerprints (from prGCMS data) with environmental covariates to explore spatial patterns.
- Important note: anonymised teabag brands (A, B, C) and lack of explicit spatial coordinates in the dataset mean spatial analyses require supplementary site-location metadata.

## Data structure and attributes (highlights)
- Degradation_Mass.csv
  - Time: months; initial_teabag_mass, final_mass, mass_loss (g); Mass_loss_percent (%).
- Degradation_PLA.csv
  - Time: months; PLA_content (%); Note: data gaps for Tbag-C.
- Degradation_crystallinity.csv
  - Time: months; crystallinity (%); Note: data only for Tbag-A and Tbag-B.
- Degradation_prGCMS_TbagA.csv / B.csv / C.csv
  - 1tR: first-column retention time (min); 2tR: second-column retention time (s); Compound; ions.
- Data provenance and QA
  - Sampling from at least five boxes across multiple stores (Plymouth, UK) 2021–2021.
  - Sample handling: washed, dried, vacuum-stored; 4 °C storage; calibration checks.
  - DSC measurements on 1–3 mg teabag samples; Py-GCxGC-TOF MS analyses conducted in triplicate per teabag type.
- Data notes
  - NAN indicates missing data.
  - Each teabag is anonymised (A, B, C) and not all measurements exist for every teabag type.

## Provenance and access
- Source: BIO-PLASTIC-RISK project; supported by NERC grants NE/V007556/1 and NE/V007246/1.
- Published associated work: Courtene-Jones et al. 2024, Science of the Total Environment (Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms). DOI: https://doi.org/10.1016/j.scitotenv.2024.172806

## Considerations for data users and GIS workflows
- Data integration
  - Combine with site-level soil properties, moisture, temperature, and land-use data to explore drivers of degradation.
  - If georeferenced sampling locations are available separately, create spatial layers for each metric (mass loss, PLA content, crystallinity, key compounds).
- Data quality and gaps
  - Tbag-C data missing in several files; consider imputing cautiously or limiting analyses to A/B where complete data exist.
  - Anonymised brands reduce ability to map to real-world products but preserve cross-site comparability.
- Temporal analysis
  - Focus on 0–7 month trajectory; crystallinity and PLA content provide insight into material changes over burial duration.
- Output ideas for GIS products
  - Time-series maps of degradation metrics by sampling location.
  - Spatial correlation maps linking degradation metrics with soil variables.
  - Chemical fingerprints mapped to spatial grids if location data are available.

## Related publication
- Courtene-Jones et al. (2024). Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment.