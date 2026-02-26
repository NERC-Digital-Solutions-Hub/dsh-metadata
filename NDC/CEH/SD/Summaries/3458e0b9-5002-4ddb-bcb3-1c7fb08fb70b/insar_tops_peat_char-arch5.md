# Survey Overview

## Purpose and Scope
- Part of the NERC InSAR ToPS project to monitor climate impact in the Flow Country, Scotland, from September 2017 to November 2018.
- Activities included peat core collection, Teabag Index measurements, peat depth mapping, and associated analyses to characterize peat properties and carbon dynamics.
- Study sites: Knockfin Heights (upland blanket peatland) and Munsary (lowland blanket peatland).

## Survey Area
- Knockfin Heights: upland site (>300 m a.s.l.) within the RSPB Forsinard Estate; features include peat hags, drained/undrained pools, and varied vegetation.
- Munsary: lowland site with numerous pool systems (Dubh Lochans), high water table, rare plants; historically grazed and burned with recent peatland restoration.
- Both sites form part of the Flow Country, the largest expanse of blanket bog in Europe.

## Cores and Sampling Protocols
- Cores collected at multiple sub-sites (Munsary A–G and Knockfin A–F) using a Russian corer (max depth 4 m).
- Sampling: cores sectioned into 50 cm intervals; first 50 cm sampled every 5 cm, remaining core every 10 cm; each interval documented for texture and features; Von Post humification assessed on-site.
- Knockfin Heights data included on-site peat volume measurement due to accessibility constraints; Munsary samples processed in-lab following Chambers et al. (2011) protocol.

## Peat Depth Protocol
- Peat depth measured in November 2018 on a predefined 1 km^2 grid at Knockfin Heights, relative to the peat surface.
- Method aligned with NatureScot (2021) Peat Depth and Condition Survey Guidance.

## Teabag Index
- 100 teabag pairs installed at all benchmarks at ~5 cm depth in June 2018; removed September 2018 amid a European drought event.
- Loss calculations (S) and decomposition rate (k) derived from post-burial weights; data input via standard calculation spreadsheets (with online tools referenced).

## Von Post Humification
- Humification assessed in the field using the Von Post scheme following FAO (2011) and Von Post & Granlund (1926).

## Bulk Density, LOI, and Organic Carbon
- Bulk density measured by water displacement (wet and dry masses) with ~2 cm^3 peat samples; dry mass obtained after oven-drying.
- Soil moisture and loss on ignition (LOI) calculated from weights before/after drying and combustion (with equations provided for LOI and OC calculations).

## File Naming Convention and Data Structure
- File naming and metadata conventions to support consistent data sharing:
  - Site codes: KH = Knockfin Heights, MUN = Munsary
  - ENV = Environmental Monitoring Data; SITE = sub-site A–F; WT = Water Level (collected at different times)
- Data sections and example fields:
  - Peat Depth dataset: includes Waypoint_Name, Lat_OSGB, Long_OSGB, Height_m.a.s.l, Peat_Depth, Comments.
  - Bulk Density dataset: includes Site, Interval, Mid, Density_gcm-3_wet/dry, Von Post, Ash_%, LOI_%, Moisture_%, Comments.
  - Teabag Index (TPI) dataset: includes No, Site, X_BNG, Y_BNG, Location, S, K; with references to methods.
- OSGB36 coordinates used for spatial referencing; data are organized by sub-sites and measurement types.

## Data Standards and References
- Core methods cited for reproducibility and interoperability:
  - Chambers, Beilman, Yu (2011): peat humification, bulk density, carbon content methods.
  - FAO (2011) and Von Post & Granlund (1926): humification classification framework.
  - NatureScot (2021): peat depth measurement guidance.
  - Teabag Index protocols (teatime4science.org): method for S and k calculations.

## Data Quality, Limitations, and Governance
- Potential data quality issues:
  - Deer damage caused loss/damage to Teabag Index samples.
  - Accessibility constraints led to on-site peat volume measurements for Knockfin Heights.
  - Some cores and measurements may be incomplete or require bespoke processing due to varied site conditions and legacy formats.
- Metadata and provenance considerations:
  - Clear documentation of sampling locations, intervals, and processing steps is provided; reuse requires adherence to the naming conventions and referenced protocols.
  - Values derived from on-site measurements (e.g., bulk density, LOI) rely on standardized lab procedures and documented equations.

## Data Access, Sharing, and Stewardship
- Datasets are organized for upload to relevant portals; emphasis on consistent metadata, standardized file names, and explicit site/sub-site references.
- Updates and versioning implied by structured file naming and documented protocols; stewardship should ensure timely updates and traceable changes.

## Key Challenges for Data Stewards (Archetype Alignment)
- Aligning user needs with dataset structure: ensuring metadata captures data user requirements (e.g., researchers needing site coordinates, depth intervals, and methods).
- Ingesting data from multiple systems and formats while preserving interoperability across platforms.
- Handling large, high-resolution sampling data and ensuring transfer efficiency between field and archive systems.
- Managing data with legacy or bespoke components (e.g., site-specific volume measurements) to maintain interoperability.
- Maintaining up-to-date documentation in line with evolving guidance (e.g., NatureScot updates, FAO classifications) and ensuring clear references in data records.