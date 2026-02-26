# Benthic organic matter of Welsh upland rivers in response to organic matter addition

- Objective and design
  - Investigates how leaf litter addition affects benthic organic matter (BOM) in Welsh upland rivers.
  - Uses a BACI (before-after-control-impact) setup: each stream has an upstream reference (control) and downstream experimental (treatment) zone, separated by 20–50 m to maintain independence.
  - Time periods:
    - Before (T1): 61–65 days from early Nov 2012 to early Jan 2013, no manipulation; both zones treated equally.
    - After (T2): 57–62 days from Jan to Mar 2013; experimental zone supplemented with leaf litter (and additional litter after storm events).
  - Leaf litter added via 1-tonne bags of deciduous leaves (oak, birch, alder) proportionally distributed by experimental zone area; minimum wet weight target 1.7 kg m^-2.
  - Additional 630 kg (wet weight) of leaf litter added on 12 Feb and 5 Mar 2013 after two large storm events.

- Sampling and collection
  - Six random BOM samples collected per reach on five occasions (Jan–May 2013) using Surber nets (0.1 m^2 area, 330 μm mesh, 10 cm depth).
  - On-site preservation in 70% IMS; in the lab, macroinvertebrates removed, BOM dried and weighed to 0.01 g.
  - Samples corrected for inorganic content by ash-free conversion (subset combusted at 550°C for 5 h).
  - Data collection resulted in measurements of coarse and fine particulate organic matter (POM).

- Field and laboratory instrumentation
  - Surber net: 0.1 m^2 area, 330 μm mesh, 10 cm sampling depth.
  - Laboratory weight measurement for BOM; ash-free corrections applied as described above.

- Calibration and quality control
  - No calibration steps reported.
  - No explicit quality-control procedures described beyond standard cleaning and processing (e.g., sieving, drying, ash correction).

- Analytical methods and units
  - BOM stocks weighted to the nearest 0.01 g.
  - Units: grams of coarse particulate organic matter (CPOM) and fine particulate organic matter (FPOM).

- Data structure and contents
  - Data stored as flat CSV files.
  - BOM data table contains 10 columns:
    - site_code: site identifier
    - landuse: basin land-use
    - region: stream basin
    - time: Before or After manipulation
    - month: collection month
    - reach: Experimental or Control site
    - replicate: replicate code
    - surber_area: area of the Surber sampler in m^2
    - cpom: coarse particulate organic matter (grams)
    - fpom: fine particulate organic matter (grams)
  - Miscellaneous supporting documents include a site description CSV with 10 columns (Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment).

- Temporal and spatial scope
  - Temporal: January–May 2013 sampling across pre- and post-manipulation periods.
  - Spatial: multiple streams with paired upstream (control) and downstream (experimental) zones; stream reaches characterized by land-use and region attributes.

- Data ready-for-use notes
  - CSV-based data with explicit time labeling (Before/After) and reach designation (Experimental/Control) facilitates self-serve analysis and comparison across zones and months.
  - Documentation includes site descriptions to support geospatial context and replication of sampling locations.