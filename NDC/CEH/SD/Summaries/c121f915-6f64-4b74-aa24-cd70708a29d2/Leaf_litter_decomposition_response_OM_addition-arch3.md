# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

- Objective: Assess leaf litter decomposition in Welsh upland rivers when organic matter is added, using a controlled BACI design to compare upstream reference and downstream experimental zones.

- Experimental design:
  - BACI setup with upstream reference and downstream experimental zones within each stream; zones similar in length and habitat; ~20–50 m separation to maintain independence.
  - Time periods:
    - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated equally.
    - After period (T2): 57–62 days (Jan 2013 to Mar 2013); experimental zone receives leaf litter addition.
  - Leaf litter manipulation:
    - One tonne bags of deciduous leaves (oak, birch, alder) divided proportionally by experimental area.
    - Maintenance of minimum wet weight ~1.7 kg m-2 in the experimental zone.
    - Leaf packs fixed in the wetted channel; additional 630 kg (wet weight) of leaf litter added after two storm events (12 Feb and 5 Mar 2013).
  - Litter bags:
    - Fine mesh and coarse mesh bags deployed; half removed at end of T1 and half replaced to measure decomposition during T2.
    - Sampling labels: bags collected as T1 (initial) and T2 (end of experiment); some left in place for ~18 weeks (T18) for comparison.

- Collection and processing:
  - On collection, litter bags preserved in 70% ethanol on site; transported to laboratory.
  - In the lab: leaves rinsed through 250 µm sieve to remove sediments; air-dried to constant mass; macroinvertebrates separated.

- Analytical methods:
  - Leaves processed to estimate ash-free dry mass (AFDM) by combusting a 1 g subsample at 500°C.
  - Relevant references: Benfield (Methods in Stream Ecology, 2006).
  - Output metrics:
    - Percentage of leaf mass remaining in fine and coarse mesh bags.
    - Decomposition rate of mass loss per day for fine and coarse mesh bags.

- Data structure and content:
  - Data files stored as flatbed CSVs.
  - Leaf litter decomposition dataset includes 10 columns:
    - site, Code of the sampling site, landuse, region, reach, t0, t1, t2, days, time, replicate, fine.percent.remaining, coarse.percent.remaining, fine.precent.loss.day-1, coarse.precent.loss.day-1.
  - Data timing and replication details allow assessment of treatment effects and temporal dynamics.

- Miscellaneous supporting documents:
  - DURESS_CU_site_description.csv providing site-level metadata (Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment).
  - Site descriptions linked in the CEH Data Catalogue; some links may not remain permanently.

- Data governance and sharing notes:
  - Data and references are documented with explicit metadata fields to aid verification and reuse.
  - Links to references may be subject to change; CEH Data Catalogue is a primary source for associated materials.