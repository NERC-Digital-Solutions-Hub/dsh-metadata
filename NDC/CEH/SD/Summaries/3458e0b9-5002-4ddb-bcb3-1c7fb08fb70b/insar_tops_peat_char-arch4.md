# Survey Overview

- Part of the NERC InSAR ToPS project to monitor climate impact from September 2017 to November 2018.
- Study sites: Knockfin Heights (Upland blanket peatland) and Munsary (Lowland blanket peatland) in the Flow Country, Caithness and Sutherland, Scotland.
- Sites are associated with landowners/partners (RSPB Forsinard estate; Plantlife Munsary Nature Reserve) and include a mix of natural and restored peatland features.

## Survey Area

- Knockfin Heights: >300 m a.s.l. upland peatland with erosive features, drained/undrained pools, lochans, and varied vegetation; part of the RSPB Forsinard estate.
- Munsary: Lowland peatland with numerous pool systems (Dubh Lochans), high water tables, rare plants, and a history of grazing, peat extraction, and burning; near-natural condition with recent restoration (drain blocking).

## Coring Locations and Protocol

- Cores collected at multiple sub-sites (Munsary A–G, Knockfin A–F) using a Russian corer (up to 4 m).
- Sampling: cores sectioned into 50 cm intervals; first 50 cm sampled every 5 cm, remaining core at 10 cm intervals.
- On-site sampling included Von Post humification features and peat texture indicators.
- For Knockfin Heights, peat volume measured on-site by difference using foil wrap and measuring cylinder due to access constraints.
- In-situ coring and laboratory processing followed established protocols (Chambers et al., 2011).

## Peat Depth Protocol

- Peat depth measurements collected November 2018 using a predefined 1 km^2 grid covering Knockfin Heights.
- Depths measured relative to the peat surface following the Peatland Action Peat Depth and Condition Survey Guidance (NatureScot, 2021).

## Teabag Index

- Installed: 100 pairs of teabags at bench marks to ~5 cm depth in early June 2018 (peak of the 2018 drought), removed in early September 2018.
- Outcome measures: S (degree of litter breakdown) and K (decomposition rate) calculated from post-burial wet/dry weights.
- Issues: extensive deer damage led to losses/damage of many teabags.

## Von Post Humification

- Humification assessed in the field following the Von Post and Granlund approach (1930s–1926) as outlined by FAO 2011.

## Bulk Density Measurements

- Bulk density determined by water displacement method.
- Procedure: sample ~2 cm^3 peat; weigh wet/dry masses; calculate density (wet and dry) via displacement in a measuring cylinder and subsequent oven drying.

## Soil Moisture, Ash and Loss on Ignition

- Soil moisture determined from paired dry/wet weights after oven drying (105°C) for 12 hours.
- Loss on Ignition (LOI) computed from dry and ash weights; organic carbon (OC) derived as OC% = LOI% / 2; ash content derived from 100 - LOI%.
- Equations referenced for calculations are provided in the study documentation (Chambers et al., 2011; LOI/OC relationships).

## File Naming Convention and Data Structure

- File naming and data fields are standardized to facilitate data discoverability and reuse:
  - Site codes: KH = Knockfin Heights, MUN = Munsary
  - ENV = Environmental Monitoring Data
  - SITE = Sub-site A–F (or within-site designations)
  - WT = Water level data (collected separately)
- Data tables include:
  - Peat Depth: waypoint name, OSGB36 coordinates, measured peat surface height, depth (cm), comments.
  - Bulk Density: site, interval, mid-point, wet/dry density, Von Post, ash %, LOI %, moisture %, comments.
  - Teabag Index (TPI): measurement numbers, X/Y coordinates, location, S, K, with citations to the Chambler et al./NatureScot methods.

## Data Management and Stewardship (Implications for Data Leaders)

- Use of established, citable methods (Chambers et al. 2011; FAO 2011; NatureScot 2021) supports data quality, comparability, and potential cross-site synthesis.
- Comprehensive metadata and standardized file naming improve discoverability, interoperability, and reuse across networks.
- Documentation links each data product to its method, units, and measurement context, enabling better governance and potential integration with wider peatland datasets.
- Acknowledgement of data limitations (e.g., deer damage, accessibility constraints) and site-specific issues that affect data completeness and interpretation.
- Potential for co-ownership and collaboration with the broader data community to enhance system-wide understanding of peatland carbon dynamics.