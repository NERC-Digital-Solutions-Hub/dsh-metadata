# Macroinvertebrate composition of Welsh upland rivers in response to organic matter addition

## Aim
- Demonstrates environmental condition over time by analyzing macroinvertebrate communities in Welsh upland rivers, focusing on responses to added organic matter (leaf litter) within a BACI framework to monitor ecosystem health and policy-relevant indicators.

## Experimental design
- Before-after-control-impact (BACI) design: each stream has an upstream reference (control) zone and a downstream experimental zone.
- Zones are similar in length and habitat structure; a 20–50 m gap separates zones to ensure independence.
- Time periods:
  - Before (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated identically.
  - After (T2): 57–62 days (Feb–Apr 2013); experimental zone receives leaf litter additions to simulate increased organic matter.
- Leaf litter treatment:
  - One-tonne bags of deciduous leaves (oak, birch, alder) added proportionally to experimental zone area.
  - Vegetable net bags maintained to ensure a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Additional 630 kg (wet weight) of leaf litter added on Feb 12 and Mar 5 after two storm-flow events.

## Sampling regime and collection
- Macroinvertebrates collected with Surber net (0.1 m^2, 330 μm mesh, 10 cm depth).
- Six random samples per stream reach, collected in five months: January, February, March, April, May 2013.
- On-site preservation in 70% IMS; laboratory processing included rinsing, sorting, and preservation in IMS.

## Analytical methods and measurements
- Taxonomic identification to the lowest possible level using standard keys.
- Body size measurements recorded for each individual:
  - Size1 and Size2 in mm (head width or body length).
  - Taxon_name captures species-level identification when possible; otherwise genus/family/coarse levels.
- Data structure captures both taxonomic and morphometric data.

## Data structure and content
- Data stored as flatbed CSV files.
- Surber data includes 11 columns:
  - site_code, region, month, collection month, time (Before/After), landuse, reach (Experimental or Control), replicate, taxon_name, Size1, Size2, Measurement, Comment.
- Measurements link Size1/Size2 to a specific body part (e.g., head width, body length) via the Comment field.

## Site metadata and supplementary data
- Miscellaneous site descriptions available in DURESS_CU_site_description.csv with 10 columns:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.
- Site data provide geographic coordinates, grid references, elevation, catchment information, and survey campaign (WAWS—Welsh Acid Water Survey, with relevant catchments).

## Data handling, quality, and accessibility
- Calibration steps: None.
- Quality control: None explicitly described.
- Data storage and sharing: Datasets are stored in flat CSV format and uploaded to appropriate portals for access and reuse.
- Value for monitoring: The standardized BACI design and detailed taxonomic/morphometric data support temporal and spatial assessment of environmental health and the ecological impact of organic matter inputs. The inclusion of site metadata facilitates data integration with other environmental datasets.