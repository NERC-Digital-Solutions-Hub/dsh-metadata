# Survey Overview

- Part of the NERC InSAR ToPS project conducted at two Flow Country sites in Scotland (Knockfin Heights in Sutherland and Munsary in Caithness) from September 2017 to November 2018.
- Objectives: monitor climate impacts through peatland measurements by collecting peat cores, teabag index data, and peat depth; cores also analyzed for Von Post humification and peat density.

## Survey Area and Sites

- Knockfin Heights: upland blanket bog (>300 m a.s.l.), part of the RSPB Forsinard estate; characterised by erosive features, drained/undrained pools, lochans, and a mix of sedge, sphagnum, heather, and grasses.
- Munsary: lowland blanket bog; part of Plantlife Munsary Nature Reserve; features numerous pool systems and near-natural conditions, with historic grazing, peat extraction, burning, and recent drain-blocking restoration.
- The study used precise site layouts with permanent and temporary markers to locate coring and monitoring points (e.g., OSGB36 coordinates for sub-sites).

## Data Collected and Protocols

- Peat Cores
  - Locations: Munsary A–G (A–F shown as examples) and Knockfin A–F; sampled to a maximum of 4 m using a Russian corer.
  - Sampling: cores sectioned at 50 cm intervals; first 50 cm at 5 cm increments, remaining intervals at 10 cm increments.
  - On-site measurements: interval descriptions and features (texture, air bubbles, etc.); in Knockfin Heights, peat volume measured on-site due to accessibility.

- Teabag Index (TBI)
  - 100 teabag pairs installed at benchmarks at ~5 cm depth in June 2018 and retrieved by September 2018, coinciding with drought.
  - Wet and dry weights recorded; data used to compute S (litter breakdown) and K (decomposition rate).
  - Notes: substantial deer damage led to losses/damages, reducing data recoveries.

- Peat Depth
  - Measurements conducted in Nov 2018 on a predefined 1 km² grid covering Knockfin Heights.
  - Depths relative to peat surface; methodology aligned with NatureScot guidance (2021).

- Von Post Humification
  - Field-based classification following FAO (2011) and Von Post & Granlund (1926) protocols to determine humification.

- Bulk Density
  - Measured by water displacement method; ~2 cm³ peat sub-samples analyzed for wet and dry density; procedure described by Chambers et al. (2011).

- Soil Moisture, Loss on Ignition (LOI), Organic Carbon (OC), Ash
  - Approximately 10 g subsamples weighed; dry/wet weights used to calculate soil moisture.
  - LOI calculated from dry and ash masses; OC inferred from LOI (OC% = LOI%/2); Ash% = 100 - LOI%.
  - Standard lab protocol references: Chambers et al. (2011) and related LOI/OC methods.

## Data Formats, Metadata, and Outputs

- File Naming and Data Structure
  - Site codes: KH = Knockfin Heights, MUN = Munsary; ENV = Environmental Monitoring Data; SITE = sub-site A–F; WT = Water Level (collected separately).
  - Peat Depth data fields: Waypoint_Name, Lat_OSGB, Long_OSGB, Height_m.a.s.l, Peat_Depth.
  - Bulk Density data fields: Site, Interval, Mid, Density_gcm-3_wet, Density_gcm-3_dry, Von Post, Ash%, LOI%, Moisture%, Comments.
  - Teabag Index (TPI) data fields: No, Site, X_BNG, Y_BNG, Location, S, K.
- Coordinate Systems
  - Core locations provided in OSGB36 (British National Grid) coordinates; some datasets also reference lat/long OSGB36 values.
- Data Provenance and Calculations
  - S and K (Teabag Index outputs) derived from post-burial measurements using specified calculation spreadsheets (links/stepwise protocol provided in-text).
  - References for methods include Chambers et al. (2011), FAO (2011), NatureScot (2021), and von Post & Granlund (1926).

## Data Quality, Limitations, and Considerations

- Data Gaps and Losses
  - Teabag data limited by deer damage causing loss/damage of teabags.
- Data Coverage and Formats
  - Coring occurred across many sub-sites with detailed interval-level measurements; data may exist in multiple formats requiring harmonization across datasets.
- On-site Measurement Challenges
  - Accessibility issues at Knockfin Heights necessitated alternative peat volume measurements on-site; interval descriptions rely on field notes.
- Provenance and Reproducibility
  - Protocols explicitly cited; data products are tied to documented methods and standard references to support reproducibility and secondary analyses.

## Data Products and Usage

- Data products enable self-serve analysis for peat properties (density, moisture, LOI, OC, ash), humification status, and decomposition indicators (S and K from Teabag Index).
- Rich metadata and coordinates support spatial analyses across sites and sub-sites.
- Calculated S and K values enable interpretation of litter decomposition dynamics under site-specific hydrology and climate contexts.
- Data sources and methods are well-documented to facilitate reuse and cross-study comparability.