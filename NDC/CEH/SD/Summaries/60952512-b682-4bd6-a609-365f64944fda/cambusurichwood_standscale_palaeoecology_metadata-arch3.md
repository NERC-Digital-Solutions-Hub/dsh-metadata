# Metadata

- Overview
  - A dataset of palaeoecological proxies from Cambusurich Wood, Scotland, derived from stand-scale analyses to study long-term dynamics in ancient temperate woodland of high conservation value.
  - Location: Ordnance Survey grid NN 62741 34679; Cambusurich Wood Site of Special Scientific Interest.
  - Sampling: October 2020, duplicate peat cores collected with a large Russian corer from an 8.5 × 7 m peat-infilled forest hollow named Camb.
  - Analyses: microfossils (pollen, non-pollen palynomorphs, spores, microcharcoal), plant macrofossils, macrocharcoal; chronology and LOI (loss-on-ignition) based on the same core as microfossil analyses.
  - Funding: Natural Environment Research Council (Grant NE/S007377/1).

- Data files and key contents
  - CambusurichWood_Raw_Microfossil_Data.csv
    - Sample_mid_depth (1 cm peat subsample mid-depth in cm)
    - Sample_volume (sample volume in cm3)
    - Exotic_lycopodium_added (number of exotic lycopodium tablets added for pollen concentration calculations)
    - Exotic_lycopodium_counted (number of exotic lycopodium spores counted)
    - Exotic_lycopodium_tablets_added (number of exotic lycopodium tablets added)
    - Rows 6–120: raw counts for pollen, spores, non-pollen palynomorphs, and microcharcoal
  - CambusurichWood_Raw_Macrofossil_Data.csv
    - Sample_mid_depth (2 cm peat subsample mid-depth in cm)
    - Sample_volume (sample volume)
    - Rows 3–76: raw macrofossil data per sample (depth) across categories such as seeds, bracts, catkin scales, buds, twigs, cones, etc.; values are raw counts or a four-tier scale (rare to abundant)
    - Rows 77–80: macrocharcoal counts by fragment size classes (0–1 mm, 1–2 mm, 2–3 mm, 3–4 mm)
  - CambusurichWood_Chronological_Controls.csv
    - Depth_cm (sample depth for chronological controls)
    - Lab-code (unique sample identifier for AMS radiocarbon dates)
    - Material (description of chronological control material)
    - 14C_Age (radiocarbon age in years before present)
    - Error (uncertainty in age)
  - CambusurichWood_Loss_On_Ignition.csv
    - Mid_depth_cm (mid-depth of 1 cm peat sample)
    - Loss-on-ignition (percentage LOI using Heiri et al. 2001 protocol)
  - CambusurichWood_Troels_Smith.csv
    - Depth_cm (sediment depth boundaries in cm)
    - Components (sediment components described using Troels-Smith 1955 system)

- Methods and standards
  - Chronology: AMS radiocarbon dating and 210Pb dating used for age controls
  - Analyses: pollen, spores, non-pollen palynomorphs, microcharcoal (microfossil), macrofossils (macrofossil counts and semi-quantitative scales), macrocharcoal by size
  - LOI: Loss-on-ignition following the protocol of Heiri et al. (2001) for organic and carbonate content estimation
  - Taxonomic and reference framework: Supporting literature includes Bennett (pollen types), Field et al. (palaeoecology), Heiri et al. (LOI methodology), Miola (NPPs), Moore et al. (Pollen Analysis), Nakagawa et al. (pollen extraction methods), Stockmarr (exotic spores tablets), Troels-Smith (sediment characterization)

- Supporting literature (selected references)
  - Bennett, K. (Catalogue of pollen types)
  - Field, M., Beaulieu, J., Guiot, J. & Ponel, P. (2000)
  - Heiri, O., Lotter, A., Lemeke, G. (2001)
  - Miola, A. (2012)
  - Moore, P.D., Webb, J.A. & Collinson, M.E. (1991)
  - Nakagawa, T. et al. (1998)
  - Stockmarr, J. (1971)
  - Troels-Smith, J. (1955)

- Data governance, accessibility, and use considerations
  - Data are organized into clearly defined CSV files with explicit column descriptions, enabling transparent replication and secondary use.
  - Some fields are raw counts or semi-quantitative scales; users may need standard transformation for cross-study comparability.
  - Metadata supports traceability to sample depth, volumes, dating controls, and sediment descriptions, aiding data quality assessment and governance.
  - The dataset exemplifies data provenance from field collection through laboratory analyses to chronological controls, aligning with open data and data-sharing best practices, while acknowledging potential barriers noted in monitoring frameworks (e.g., data gaps, metadata sufficiency, and governance needs).