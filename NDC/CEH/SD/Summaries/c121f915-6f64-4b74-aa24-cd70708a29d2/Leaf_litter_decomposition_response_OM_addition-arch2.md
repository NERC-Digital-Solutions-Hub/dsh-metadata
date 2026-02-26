# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

- Objective
  - Evaluate how added organic matter (leaf litter) influences leaf litter decomposition in Welsh upland streams using a controlled BACI design, by comparing upstream reference zones to downstream experimental zones over time.
  - Quantify decomposition by measuring the remaining leaf mass in different bag mesh sizes and deriving decomposition rates.

- Experimental design
  - Before-After-Control-Impact (BACI) setup: each stream has an upstream reference (control) zone and a downstream experimental zone.
  - Spatial separation to ensure independence: 20–50 m between zones.
  - Timeline:
    - Before period (T1): 61–65 days, Nov 2012 to Jan 2013; no manipulation; both zones treated equally.
    - After period (T2): 57–62 days, Jan to Mar 2013; experimental zone receives leaf litter manipulation.
  - Organic matter additions:
    - Distributed leaf litter from deciduous sources (oak, birch, alder) to the experimental zone to match its area.
    - Wet weight maintenance target: minimum 1.7 kg m^-2 in the experimental zone.
    - Additional litter: 630 kg (wet weight) added to each stream after two storm-flow events (Feb and Mar 2013).

- Collection and processing methods
  - Leaf litter bags:
    - Type: fine and coarse mesh; contents deployed above the experimental zone and adjusted to reflect natural leaf packs.
    - Sampling points:
      - T1: end of the before period; half of the bags removed for processing and half replaced with new bags to measure after manipulation.
      - T2: end of the after period; remaining bags removed.
      - Bags labeled for processing: T1, T2, and T18 (bags left in situ for ~18 weeks).
  - Processing in the lab:
    - Preserved on site in 70% ethanol, then transported to the lab.
    - Leaves rinsed, air-dried to constant mass.
    - Macroinvertebrates separated from litter bags.
  - Analytical methods:
    - AFDM: 1 g subsample combusted at 500°C to estimate ash-free dry mass.
    - Reference: Benfield (2006) Methods in Stream Ecology.
  - Output metric:
    - Percentage of leaf mass remaining in fine and coarse mesh bags.
    - Decomposition rates expressed as percent mass loss per day.

- Data structure and units
  - Data format: flatbed CSV files.
  - Leaf litter decomposition data includes 10 columns:
    - site, Code of the sampling site, landuse, region, reach, t0, t1, t2, days, time, replicate, fine.percent.remaining, coarse.percent.remaining, fine.precent.loss.day-1, coarse.precent.loss.day-1
  - Outputs summarize mass remaining and decomposition rates for both fine and coarse mesh bags.

- Supporting data and metadata
  - DURESS_CU_site_description.csv provides site-level context:
    - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey campaign, Catchment, etc.
  - Metadata supports linking sites to catchments and geographic coordinates for integration with other datasets.

- Relevance to environmental monitoring and data management
  - Uses a standard, well-documented BACI design and established analytical methods, enabling consistent comparison over time and across streams.
  - Data are structured for easy ingestion into monitoring portals and can be combined with other environmental datasets (e.g., hydrology, water chemistry, broader organic matter inputs) to enhance environmental health assessments.
  - Supporting site metadata facilitates spatial analyses and data interoperability within environmental monitoring programs.