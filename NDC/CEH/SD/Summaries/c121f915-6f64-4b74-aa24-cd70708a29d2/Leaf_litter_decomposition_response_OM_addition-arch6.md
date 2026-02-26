# Leaf litter decomposition of Welsh upland rivers in response to organic matter addition

- Objective
  - Assess how leaf litter decomposition in Welsh upland streams responds to added organic matter using a BACI design.

- Experimental design
  - Before-after-control-impact (BACI) setup in multiple streams.
  - Each stream divided into an upstream reference (control) and downstream experimental (treatment) zone, separated by 20–50 m to maintain independence.
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013) with no manipulation; both zones observed similarly.
  - After period (T2): 57–62 days (early Jan to Mar 2013) with leaf litter addition in the experimental zone.
  - Leaf litter: 1 tonne bags containing deciduous leaves (oak, birch, alder) added to the experimental zone, proportionally by area; minimum wet weight target of 1.7 kg m-2.
  - Additional litter: 630 kg (wet weight) added on 12 Feb 2013 and 5 Mar 2013 after two large storm events.

- Data collection and sampling regime
  - At the end of the before period (T1), half of the litter bags were removed from both zones; 6 fine and 6 coarse mesh bags were kept as controls, and 6 new fine and 6 new coarse mesh bags were added to measure after-manipulation (T2) conditions.
  - At the end of the experiment, bags from T0 (left ~18 weeks) and T2 (beginning of T2) were collected and labeled accordingly (T18 and T2).
  - On collection, litter bags were preserved in 70% ethanol on site, then transported to the lab for processing.

- Analytical methods and data
  - In the lab, leaf material was rinsed, air-dried to constant mass, and macroinvertebrates were separated from the contents.
  - Leaves: a 1 g subsample from each bag was combusted at 500°C to estimate ash-free dry mass (AFDM) following standard methods.
  - Key metrics:
    - Percentage of leaf mass remaining for fine and coarse mesh bags.
    - Decomposition rate (percent loss per day) for fine and coarse bags.

- Data structure and variables
  - Data stored as flatbed CSV files.
  - Core variables (example, 14 fields):
    - site: site code
    - landuse: stream basin land-use category
    - region: basin land-use region
    - reach: experimental vs. control designation
    - t0: date bags were placed
    - t1: date of leaf addition to the experimental reach
    - t2: end date of the experiment
    - days: duration of the experiment
    - time: Before or After manipulation
    - replicate: replicate code
    - fine.percent.remaining: percentage of leaf mass remaining in fine mesh bags
    - coarse.percent.remaining: percentage of leaf mass remaining in coarse mesh bags
    - fine.precent.loss.day-1: decomposition rate for fine bags (loss per day)
    - coarse.precent.loss.day-1: decomposition rate for coarse bags (loss per day)

- Miscellaneous supporting materials
  - DURESS_CU_site_description.csv: site metadata (Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey Campaigns)
  - Data references note: links to source references are provided in the CEH Data Catalogue Record; however, link stability cannot be guaranteed.

- Context for data use
  - Data enables comparison of leaf litter decomposition under natural conditions (control) and enhanced organic matter inputs (treatment) across multiple streams.
  - Useful for analyses of how increased organic matter affects aquatic decomposition processes and for meta-analyses of BACI-designed ecosystem experiments.
  - Provides both raw bag-level measurements (percent remaining) and derived decomposition rates to support self-service data exploration and interpretation.