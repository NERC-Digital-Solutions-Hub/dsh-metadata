# Macroinvertebrate leaf decomposers of Welsh upland rivers in response to organic matter addition

## Overview
- Study investigates how adding organic matter (leaf litter) affects macroinvertebrate communities responsible for leaf decomposition in Welsh upland rivers.
- Uses a before-after-control-impact (BACI) design across eight streams to compare upstream reference zones with downstream experimental zones.

## Experimental design
- Each stream contains an upstream reference zone and a downstream experimental zone of similar length and habitat structure.
- Zones are separated by 20–50 meters to ensure independence.
- Time periods:
  - Before period (T1): 61–65 days, Nov 2012 – Jan 2013; no manipulation; both zones treated equally.
  - After period (T2): 57–62 days, Jan – Mar 2013; experimental zone receives leaf litter addition.
- Leaf litter additions:
  - One tonne bags of deciduous leaves (oak, birch, alder) added to the experimental zones proportionally to area.
  - Vegetable nets used to maintain a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Additional 630 kg (wet weight) leaf litter added on 12 Feb 2013 and 5 Mar 2013 after storm events.
- Litter bags placed in the stream above the experimental zone, randomly fixed along the wetted channel.

## Treatments and sampling regime
- Mesh litter bags:
  - Sizes: 10 x 15 cm with apertures of 500 µm (fine) and 5 mm (coarse).
  - Filled with 5 g (±0.05 g) of air-dried leaves.
  - Purpose: restrict or allow invertebrate colonisation.
- Replication:
  - 48 replicate mesh litter bags per stream (24 reference, 24 experimental) for each mesh type.
  - Bags secured in pairs to metal poles and covered with cobbles to facilitate colonisation.
  - Under low flow, bags remain submerged and distributed across the stretch.
- Sampling schedule:
  - End of T1: half the bags (6 fine and 6 coarse per zone per stream) removed; new bags (6 fine, 6 coarse) added to measure decomposition during T2.
  - End of T2: remaining bags from T0 and bags added at the start of T2 removed; labeled as T18 or T2.

## Collection methods and processing
- On-site preservation: litter bags preserved in 70% ethanol in labeled containers.
- Laboratory processing:
  - Leaf material rinsed through a 250 µm sieve; air-dried to constant mass.
  - Macroinvertebrates separated and identified to species when possible; several taxa identified at coarse taxonomic levels (e.g., Chironomidae, Tipulidae, Limoniidae, Pediciidae, Oligochaeta, Limnephilidae).
  - Identification aided by a microscope.

## Taxonomy and measurement
- Primary metric: invertebrate abundance (count).
- Taxonomic resolution: species-level when possible; otherwise genus, family, or coarse levels.
- Data collected per individual include taxon name and abundance.

## Data structure and variables
- Bag data (10 columns):
  - site_code: sampling site identifier
  - region: river basin region
  - date: sampling date
  - time: Before/After manipulation indicator
  - landuse: basin land-use
  - reach: Experimental or Control site
  - Replicate: replicate code (T1, T2, T18) and letters A–F for replicate within each sampling
  - BagMesh: leaf bag type (fine or coarse mesh)
  - taxon_name: taxon name (lowest resolution possible)
  - abundance: taxon abundance
- Miscellaneous site data:
  - DURESS_CU_site_description.csv provides site codes, coordinates (Eastings/Northings, latitude/longitude), elevation, catchment, and related descriptors.

## Supporting data and site information
- Site descriptive file contains:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey campaign, Catchment
- Field and laboratory instrumentation includes basic microscopy for identification.

## Notes on quality control and calibration
- Calibration steps: none reported.
- Quality control: none reported.