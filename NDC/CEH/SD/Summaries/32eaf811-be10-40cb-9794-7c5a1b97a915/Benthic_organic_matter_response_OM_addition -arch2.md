# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI (before-after-control-impact) study assessing how added leaf litter affects benthic organic matter (BOM) in Welsh upland rivers.
- Each stream has an upstream reference zone and a downstream experimental zone, with a 20–50 m separation to ensure independence.
- The experiment simulates increased allochthonous input by introducing leaf litter over the experimental reach.

## Experimental design and timeline
- Before period (T1): 61–65 days, Nov 2012–early Jan 2013; both reference and experimental zones untreated.
- After period (T2): 57–62 days, Jan–Mar 2013; experimental zone receives leaf litter additions.
- Leaf litter manipulation details:
  - One-tonne bags of oak, birch, and alder leaves, apportioned by experimental zone area.
  - Leaf packs maintained at a minimum wet weight of 1.7 kg m^-2 in the experimental zone.
  - Leaf bags fixed within the wetted channel; designed to reflect natural senescence/abscission.
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb 2013 and 5 Mar 2013 after two large storm events.

## Data collection and processing
- BOM sampling: Six random samples per reach using a Surber net (0.1 m^2 area, 330 µm mesh, 10 cm depth) at five time points (Jan–May 2013).
- On-site preservation: 70% industrial methylated spirit (IMS).
- Lab processing: Separate macroinvertebrates; retain BOM material; dry to constant weight; weigh to 0.01 g.
- Organic matter correction: Correct BOM for inorganic content via ash-free conversion by combusting a subset of samples at 550°C for 5 hours.

## Analytical methods and units
- BOM stocks weighed to 0.01 g precision.
- Measured units: grams for coarse and fine particulate organic matter (CPOM/FPOM).

## Data structure and variables
- Data format: flatbed CSV files.
- Key fields (10 columns):
  - site_code: site identifier
  - landuse: basin land-use
  - region: river basin region
  - time: Before or After manipulation
  - month: sampling month
  - reach: Experimental or Control site
  - replicate: replicate code
  - surber_area: area of the Surber sampler in m^2
  - cpom: coarse particulate organic matter (g)
  - fpom: fine particulate organic matter (g)

## Supporting data and metadata
- Supporting site description: CSV with 10 columns detailing site_code, name, coordinates (Eastings/Northings), Grid reference, Latitude/Longitude, Elevation, Survey, Catchment, etc.
- Data management notes:
  - Quality control: Not reported.
  - Data format designed for storage and portal upload, enabling standardized monitoring outputs.

## Relevance for environmental monitoring analysts
- Demonstrates a standardized, transparent approach to experimental manipulation and monitoring of BOM in streams.
- Provides a structured dataset with clear temporal (Before/After) and spatial (Reference/Experimental) dimensions suitable for trend analysis and policy performance evaluation.
- Emphasizes data reconciliation and documentation through site metadata to support long-term environmental health monitoring.