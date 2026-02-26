# Survey Overview

- Purpose: Document the InSAR ToPS project fieldwork at two Flow Country sites to monitor climate impacts (Sept 2017–Nov 2018) via peat cores, peat depth, and teabag decomposition metrics.

## Survey Area

- Locations: 
  - Knockfin Heights, an upland blanket peatland (>300 m above sea level), part of the RSPB Forsinard estate, Caithness/Sutherland.
  - Munsary, a lowland blanket peatland area within the Flow Country, Caithness, owned by Plantlife.
- Site characteristics: complex erosion features at Knockfin Heights; Munsary features numerous pool systems, high water tables, near-natural condition with historical grazing and peat extraction; recent drainage blocking restoration nearby.
- Study setup included a map layout with markers for permanent, floating monitoring devices and sample locations.

## Field Sampling and Cores

- Cores were collected at multiple sub-sites (e.g., Munsary A–G, Knockfin A–F) with OSGB36 coordinates provided for each point.
- Method: Russian corer (max length 4 m); cores sectioned into 50 cm intervals (first 50 cm sampled every 5 cm, remainder every 10 cm).
- On-site subsampling and description of intervals for Von Post classification and texture/air-bubble features.
- Knockfin Heights peat volume measured in situ by foil wrap and measuring cylinder due to accessibility issues.
- Core processing followed the protocol of Chambers et al. (2011).

## Peat Depth Protocol

- Depth measurements conducted November 2018 on a predefined 1 km^2 grid across Knockfin Heights.
- Depths recorded relative to peat surface; methodology aligned with NatureScot Peat Depth and Condition Survey Guidance (2021).

## Teabag Index

- 100 teabag pairs installed at all benchmarks at ~5 cm depth in June 2018; removed Sept 2018 during European drought peak.
- Weights recorded and litter decomposition metrics (S: degree of litter breakdown, K: decomposition rate) calculated with standard protocols.
- Note: deer damage caused loss/damage of many teabags.

## Von Post Humification and Bulk Density

- Humification: Von Post methodology (FAO 2011; based on Von Post and Granlund 1926) conducted in the field at Knockfin Heights.
- Bulk density: measured by water displacement method (Chambers et al. 2011). Sample protocol involved approximately 2 cm^3 peat, moisture/wet-dry weight measurements, and subsequent calculation of bulk density.

## Soil Moisture, Ash, and Loss on Ignition (LOI)

- Moisture and LOI determined from ~10 g peat samples using 105°C drying for moisture and a 550°C/105°C sequence for LOI.
- Calculations:
  - Moisture: H2O% = (md / mw) × 100
  - LOI% = ((md − ma) / md) × 100
  - Organic Carbon (OC%) ≈ LOI% / 2
  - Ash% = 100 − LOI%

## Data and File Documentation

- File naming conventions for site-level datasets:
  - KH = Knockfin Heights; MUN = Munsary
  - ENV = Environmental Monitoring Data; SITE = SUB SITE A–F; WT = Water Level (collected separately)
- Data fields by dataset:
  - Peat Depth: waypoint/site name, OSGB36 coordinates, peat surface height, Peat_Depth (cm), comments.
  - Bulk Density: Site/subsite, Interval, Midpoint, Density (wet/dry, g/cm^3), Von Post, Ash%, LOI%, Moisture%, comments.
  - Teabag Index (TPI): measurement number, site location, coordinates (BNG), location, S, K; references to underlying methodologies.
- Data organization and metadata are aligned with the cited references and protocols (Chambers et al. 2011; FAO 2011; NatureScot 2021; von Post/L.). 

## Data Quality, Limitations, and Challenges

- Data availability and resolution gaps: data held in multiple places; some measurements limited by site accessibility and environmental conditions.
- Deer damage caused significant loss/damage to teabag deployments, affecting sample completeness.
- Large/complex datasets and variable resolutions require cleaning, transformation, and potential sub-division into manageable GIS-ready layers.
- Consistency in data standards across measurements emphasized (e.g., units, coordinate reference system OSGB36).

## GIS Relevance and Potential Data Products

- ready-to-map datasets for GIS visualization:
  - Peat depth (cm) across Knockfin Heights and Munsary on an OSGB36 grid.
  - Bulk density (wet/dry in g/cm^3) and LOI/OC percentages by core interval.
  - Soil moisture (%) and ash content per sample interval.
  - Teabag Index results (S and K) by benchmark/site with spatial context.
  - Von Post humification classes by core interval.
- Integration opportunities with InSAR-derived land-surface data to correlate peatland surface changes with soil properties.
- Use for policy/land-management visualization and engagement for stakeholders (policy colleagues, clients, public), consistent with GIS-focused data products.

## References

- Chambers, F.M., Beilman, D.W. & Yu, Z. (2011): Methods for determining peat humification and quantifying peat bulk density, organic matter and carbon content.
- FAO (2011) Classification of Organic Soils.
- NatureScot (2021) Peatland Action Peat Depth and Condition Survey Guidance.
- Von Post L., Granlund L.E. (1926); Södra Sveriges Torvtillgångar.