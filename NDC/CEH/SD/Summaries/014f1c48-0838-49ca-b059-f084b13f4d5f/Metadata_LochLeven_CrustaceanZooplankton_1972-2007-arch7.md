# METADATA FOR 'LOCH LEVEN CRUSTACEAN ZOOPLANKTON 1972-2007' DATASET

## Overview
- Long-term dataset of crustacean zooplankton densities from Loch Leven (1972–2007), collected by CEH Edinburgh and predecessor bodies.
- Measures densities (ind/l) of three major crustacean zooplankton taxa per sample: Cyclops abyssorum (+ nauplii), Eudiaptomus gracilis (+ nauplii), and Daphnia sp.
- Data collected as part of an ongoing lake monitoring programme; dataset was quality controlled by senior researchers on the project.

## Spatial and Temporal Coverage
- Spatial: multiple sampling sites around Loch Leven with GB National Grid coordinates (Eastings/Northings) provided in Table 1.
  - Centre Loch, Kinross Bay, North Deeps, Public Pier, Castle Bay, Reed Bower, Outflow.
- Temporal: 1972–2007.
- Notes: When a sample used more than one location/method, site values were averaged. Zero values indicate absence at the given resolution; blanks indicate missing data.

## Data Structure and Variables
- Core columns per record: date, sampling information for that date, sampling methodology, and densities per litre for the three taxa.
- Values: densities expressed as individuals per litre (ind/l).
- Coordinate data: GB national grid locations for sampling sites included (Easting and Northing).

## Sampling Methods by Period
- 1972–1974: fortnightly samples using a 5 litre Friedinger sampler.
- 1975–1982: vertical plankton net haul (depth-specific) with mesh sizes around 100 µm or using an integrating tube sampler with a 125 µm filter.
- From 1992: samples collected with a 45-degree angled net haul (mesh 120 µm).
- All samples preserved immediately after collection in 4% formaldehyde.

## Laboratory Procedures and Taxonomy
- In the lab, samples placed in 250 ml vessels, mixed, and sub-sampled (typically 3 subsamples counted) using a 5 ml sub-sample.
- Zooplankton identified (to species level where preservation allowed) and counted under a low-power microscope.
- Sub-sample counts converted to ind/l using appropriate multiplication factors; samples reconstituted and archived afterward.
- Species names updated when taxonomic changes occurred; references provided for identification keys.

## Data Quality, Provenance, and QA
- Quality control performed by Dr Linda May (pre-1992 data) and Iain Gunn (1992–2007 data); May reviewed pre-1992 data, Gunn analyzed and checked 1992–2007 data.
- Documentation includes key references for identification and methodology used.

## Data Handling Notes for GIS Use
- Averaging: when multiple sites/methods present in a single sampling date, values are averaged.
- Zeros vs missing: zero indicates non-detection at resolution, not necessarily true absence; blanks indicate missing values.
- Data are suitable for map-based visualization (spatial distribution over time) with explicit site coordinates and temporal records.
- Data are tied to historical methods and taxonomic references; consider method changes when analysing trends.

## References (taxonomic keys and methods)
- Dussart & Defaye (1995); Einsle (1996); Flößner & Kraus (1986); George & Owen (1978); Harding & Smith (1974); Johnson (1977); Scourfield & Harding (1966).