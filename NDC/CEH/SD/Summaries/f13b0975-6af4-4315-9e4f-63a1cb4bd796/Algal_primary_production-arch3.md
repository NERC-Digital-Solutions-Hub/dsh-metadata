# Experimental design/Sampling regime

- Study uses a before-after-control-impact (BACI) design with an upstream reference zone and a downstream experimental zone within each stream; zones are similar in length and habitat, with a 20–50 m gap to ensure independence.

- Time periods:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated equally.
  - After period (T2): 57–62 days (early Jan to Mar 2013); experimental zone manipulated with leaf litter throughout T2.

- Leaf litter manipulation:
  - One tonne bags containing deciduous leaves (oak, birch, alder) divided proportionally by experimental zone area and placed above the experimental zone to simulate natural senescence.
  - Vegetable nets used to maintain a minimum wet weight of 1.7 kg/m2 in the experimental zone.
  - Additional leaf litter (630 kg wet weight) added on 12 Feb 2013 and 5 Mar 2013 after two large storm events.

- Experimental units and response variables:
  - Six algal tiles placed randomly in each reach (experimental sites) before and after manipulation.
  - Chlorophyll a accrual on tiles used as a proxy for algal production; herbivory rates inferred from controls.
  - On bricks, one tile edge treated with petroleum jelly to deter grazing; the other tile serves as a control.

- Collection and analysis methods:
  - Field: tile-based sampling to assess algal biofilm production.
  - Laboratory: extraction of chlorophyll with acetone; spectrophotometric measurement (664 nm and 750 nm) to determine chlorophyll-a concentration.
  - Calculation: chl a (μg cm−2) using a specified equation with constants and measured volumes; references to prior methodological work (Hladyz et al. 2011; Layer et al. 2010).

- Data handling and structure:
  - Data stored as flat CSV files.
  - Algal production data contains 10 columns:
    - site_code, region, date, time (Before/After), landuse, reach, treatment (experimental or control), replicate, exposure, chlorophyll (μg cm−2), plus NA for unavailable data.
  - Miscellaneous supporting documents include site_description CSV with site metadata (coordinates, catchment, survey, etc.).

- Equipment and references:
  - Field instruments summarized under collection methods; laboratory analysis notes a mass spectrometer used (details not provided in the excerpt).
  - Key references cited for methods and context:
    - Hladyz et al. 2011 (leaf litter effects on stream food webs)
    - Layer et al. 2010 (food web structure across pH gradient)
    - Jenkins, Woodward, Hildrew 2013 (acidification effects on decomposition)

- Metadata and governance:
  - Includes a site description file (DURESS_CU_site_description.csv) with location and survey details, facilitating data provenance and reproducibility.
  - Calibrations, quality control steps, and explicit data governance processes are not described in the provided text.