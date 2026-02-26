# Metadata

## Overview
- Dataset contains information about multiple palaeoecological proxies from stand-scale analyses of Cambusurich Wood, Scotland (Ordnance Survey grid reference: NN 62741 34679).
- Generated as part of a study of long-term dynamics in ancient temperate woodland of high conservation value.
- Duplicate peat cores were collected in Oct 2020 from an 8.5 x 7 m peat-infilled forest hollow named Camb in Cambusurich Wood SSSI.
- Microfossil analyses (pollen, non-pollen palynomorphs, spores, microcharcoal) were performed on one core set; plant macrofossil and macrocharcoal analyses on a second set.
- Site chronology and loss-on-ignition (LOI) analyses were based on the same core as the microfossil analyses.
- Supported by Natural Environment Research Council (Grant NE/S007377/1).

## Datasets
- CambusurichWood_Raw_Microfossil_Data.csv
  - Key fields: Sample_mid_depth (1 cm, peat subsample mid-depth), Sample_volume (cm3), Exotic_lycopodium_added, Exotic_lycopodium_counted, Exotic_lycopodium_tablets_added.
  - Data range: Rows 6-120 contain raw counts data for pollen, spores, non-pollen palynomorphs and microcharcoal analyses.
  - Notes: Exotic lycopodium used for calculations on pollen concentrations following Stockmarr (1971).

- CambusurichWood_Raw_Macrofossil_Data.csv
  - Key fields: Sample_mid_depth (2 cm thick peat subsample mid-depth), Sample_volume.
  - Data: Rows 3-76 provide macrofossil counts per sample (depth) across taxa including seeds (s), bracts (br), male catkin scales (m.cat), buds (bd), twigs (tw), cones (c), bud scales (bs), nutlets (n), florets (f), utricles (utr), megaspores (ms), fruit varves (fv), leaves (lf), leaf branches (lb) and undifferentiated remains.
  - Data presentation: Raw counts or four-point scale (x = rare, xx = occasional, xxx = frequent, xxxx = abundant).
  - Rows 77-80: macrocharcoal counts in size classes (0-1 mm, 1-2 mm, 2-3 mm, 3-4 mm).

- CambusurichWood_Chronological_Controls.csv
  - Key fields: Depth_cm (sample depth), Lab-code (AMS radiocarbon dates only), Material (description of chronological control), 14C_Age, Error (age uncertainty).

- CambusurichWood_Loss_On_Ignition.csv
  - Key fields: Mid_depth_cm, Loss-on-ignition (LOI) percentage.

- CambusurichWood_Troels_Smith.csv
  - Key fields: Depth_cm (depth boundaries), Components (sediment description using the Troels-Smith system).

- Supporting literature (listed references) providing methodological context for pollen types, NPPs, LOI, and related paleoecological analyses.

## Spatial and Temporal Context
- Sampling depth expressed as mid-depth measurements in centimeters for peat samples.
- Depth-based proxies enable construction of depth profiles of vegetation and sediment characteristics.
- Chronological controls (14C ages and depths) enable anchoring of proxies to an age framework, supporting potential age-depth modeling.

## Data Quality and Provenance
- Data originate from duplicate cores with parallel analyses (microfossil vs macrofossil) on separate subsamples from the same core.
- Mixed data types: raw counts and categorical four-point scales, with explicit depth references.
- LOI methodology follows Heiri et al. (2001) and provides a measure of organic/carbon content consistency.
- Data are tied to an OS grid reference for spatial localization, enabling GIS integration.

## GIS Applications
- Map-based visualization of paleoecological proxies across Cambusus Wood at stand scale.
- Layer ideas:
  - Sampling points with attributes: mid-depth, Sample_volume, LOI, macrofossil counts/scales, microfossil counts, and macrocharcoal counts by size class.
  - Age-depth surfaces using chronological controls to enable time-resolved maps.
  - Troels-Smith sediment components as categorical spatial layers.
- Integrate with supporting literature to justify classifications and proxy interpretations.
- Use depth-to-age relationships to create temporal maps of vegetation dynamics and sediment characteristics.

## References
- Bennett, K. (1995-2007). Catalogue of pollen types.
- Field, M., Beaulieu, J., Guiot, J., & Ponel, P. (2000). Palaeoecology study.
- Heiri, O., Lotter, A., Lemeke, G. (2001). LOI method reproducibility.
- Miola, A. (2012). Tools for Non-Pollen Palynomorphs analysis.
- Moore, P.D., Webb, J.A., Collinson, M.E. (1991). Pollen Analysis.
- Nakagawa, T., et al. (1998). Pollen extraction methods.
- Stockmarr, J. (1971). Tablets with spores in pollen analysis.
- Troels-Smith, J. (1955). Sediment characterization system.