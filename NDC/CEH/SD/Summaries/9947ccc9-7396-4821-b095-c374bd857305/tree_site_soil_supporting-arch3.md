# Soil, site and tree characteristics for acute oak decline (AOD) symptomatic and non-symptomatic oak in three UK woodlands, southern England, 2016

## Purpose and scope
- Dataset supporting investigation of how local-scale environmental factors relate to Acute Oak Decline (AOD) symptoms.
- Cross-site, cross-site comparison across three UK oak woodlands to understand interactions between tree traits, soil properties, and site context.
- Includes measurements for 60 sampled oaks (10 symptomatic and 10 asymptomatic per site).

## Data structure and contents
- Three CSV files:
  - Tree_characteristics.csv
  - Site_characteristics.csv
  - Soil_characteristics.csv
- Documented variables cover:
  - Tree-level: location, species classification (morphometric leaves and genetic SNP confirmation), dimensions (height, DBH, crown), crown condition, rooting depth, AOD symptom status.
  - Site-level: location context around each tree (depth to gleying, basal area within 0-20 m and 20-40 m, compound topographic index, tree social status).
  - Soil-level: depth-specific physico-chemical properties (texture fractions, bulk density, organic matter, pH, total C and N, mineral N, Olsen P, cation exchange capacity, exchangeable cations).
- Units and documentation are specified per variable; missing values marked as "nd".

## Study sites and sampling design
- Spatial coverage: Monks Wood (Cambridgeshire), Writtle Forest (Essex), Stratfield Brake (Oxfordshire), England.
- Temporal coverage: fieldwork conducted July–November 2016; single time point.
- Experimental design: 3 sites × 20 trees per site (10 symptomatic, 10 asymptomatic) → 60 trees total.
  - Symptomatic trees selected by presence of bleeding canker lesions on the lower stem.
  - Asymptomatic trees selected by random direction from symptomatic trees and choosing the first asymptomatic tree encountered after walking >20 m.

## Field and laboratory methods
- Tree measurements and identification:
  - Morphometric leaf analysis to classify as Quercus robur, Quercus petraea, or hybrids.
  - Genetic confirmation via SNP analysis (Sequenom) at INRA.
  - Measurements: tree height, DBH (1.35 m), crown width (EW and NS), crown density reduction, rooting depth.
  - Geospatial coordinates recorded (WGS84).
- Surrounding site context:
  - Depth to gleying (soil signs of drainage/gleying).
  - Basal area within 0–20 m and 20–40 m around tree.
  - Compound topographic index (topographic wetness index).
  - Tree social status (dominant to dying on a 1–5 scale).
- Soil sampling and analysis:
  - For each tree: eight soil samples per depth (5–15 cm and 40–50 cm), taken 1.5–2.0 m from the stem, pooled by depth to one composite per depth per tree.
  - Depths analyzed: 5–15 cm and 40–50 cm.
  - Analyses include: organic matter by loss on ignition (LOI), pH (water), texture (clay/silt/sand fractions), total carbon and nitrogen, mineral N (nitrate and ammonium after 1 h 20 °C extraction with 1 M KCl), Olsen P, cation exchange capacity (CEC), and extractable cations (Al, Ca, Fe, K, Mg, Mn, Na) using BaCl2 extracts and ICP-OES.
  - Data normalization: concentrations expressed as mg kg−1 dry soil where applicable; LOI, pH, and other properties recorded as specified.
  - Replication and QA: multiple technical replicates for key analyses; calibration standards and reference materials used; some measurements repeated or re-analyzed if needed.
- Quality control and governance:
  - Data quality checks include blanks, calibration, and reference materials described in instrument-specific QA notes.
  - Handling of below-detection-limit values (LoD/2) for certain nutrients per USEPA guidance.

## Data quality, governance and metadata
- Missing values indicated as 'nd' for several variables.
- Below-detection-limit values adjusted to half the detection limit in mineral N and related analyses where applicable.
- Metadata includes detailed instrument methods, replication schemes, and calibration procedures to support traceability and auditability.
- The dataset accompanies a pre-print exploring the cause–effect relationship between local site/soil factors and AOD.

## Temporal, spatial and data provenance notes
- Temporal snapshot: one-time sampling within July–November 2016.
- Spatially explicit: precise tree coordinates provided; three woodlands across southern England.
- Provenance documented: standard forest measurement procedures; topographic and soil analyses aligned with cited methodologies and references.

## Related outputs and potential monitoring utility
- The dataset forms the basis of a pre-print titled “The cause-effect conundrum of local-scale site and soil factors in acute oak decline (AOD).”
- For monitoring frameworks, the data provide a rich set of environmental health indicators at multiple scales:
  - Tree health indicators (AOD status, crown condition, rooting depth, social status).
  - Local site context indicators (depth to gleying, basal area, topographic index).
  - Soil health indicators (texture, organic matter, pH, C and N, mineral N, Olsen P, CEC, exchangeable cations).
- Emphasizes the need for data governance, metadata completeness, data sharing, and cross-site comparability to overcome common monitoring challenges (data access, interoperability, up-to-date metadata, and data transformation requirements).