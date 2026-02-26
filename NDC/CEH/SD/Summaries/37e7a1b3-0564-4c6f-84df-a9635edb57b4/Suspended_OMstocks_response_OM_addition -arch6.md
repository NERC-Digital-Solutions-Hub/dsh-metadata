# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

- Overview
  - Investigates how adding leaf litter (organic matter) influences suspended organic matter (SOM) stocks in Welsh upland rivers.
  - Uses a before-after-control-impact (BACI) design with upstream reference and downstream experimental zones across multiple streams.

- Experimental design
  - Each stream divided into an upstream reference zone and a downstream experimental zone, with 20–50 m between zones to ensure independence.
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); both zones treated equally.
  - After period (T2): 57–62 days (early Jan to Mar 2013); experimental zone received leaf litter addition throughout.
  - Leaf litter addition: 1 tonne bags containing oak, birch, and alder leaves added proportionally to experimental zone; leaf packs maintained with net bags to keep ~1.7 kg m^-2 wet weight; additional 630 kg (wet weight) added on two storm-event dates (12 Feb and 5 Mar 2013).

- Data collection and measurements
  - Suspended Organic Matter (SOM) sampling: filtered 100 L of stream water through 10 µm and 1 mm filters; samples refrigerated, freeze-dried, ground, and subsampled for analyses.
  - Analytical focus: elemental (C, N) and stable isotopes (δ13C, δ15N) in SOM; inorganic content correction via ash-free conversion factor.
  - Materials measured: coarse (CPOM) and fine (FPOM) particulate organic matter; both reported per sample and per liter of water; additional subsample weights for isotopic and elemental analyses.
  - Documentation of sample characteristics: sampling site, land use, region, time (Before/After), date, and sampling month; discharge (L s^-1); reach (Experimental or Control); replicate (A–F).
  - Data units include: CPOM/FPOM in grams per sample and ash-free dry mass equivalents, CPOM/FPOM concentrations in mg L^-1, and subsample contents in µg (C, N, δ13C, δ15N).

- Data structure and content
  - Data stored as flatbed CSV files.
  - Main SOM dataset includes 33 columns with fields such as:
    - site_code, landuse, region, time (Before/After), date, time, discharge, reach (Experimental/Control), replicate (A–F)
    - cpom.g.per.sample, cpom.afdm.mg.l, cpom.subsample.wt.ug, cpom.ug.C.per.subsample, cpom.ug.N.per.subsample, cpom.d13C, cpom.d15N
    - fpom.g.per.sample, fpom.afdm.mg.l, fpom.subsample.wt.ug, fpom.ug.C.per.subsample, fpom.ug.N.per.subsample, fpom.d13C, fpom.d15N
  - Includes both CPOM and FPOM measurements, along with concentration and isotopic data.

- Supporting data and metadata
  - Additional site description file (DURESS_CU_site_description.csv) with coordinates, elevation, and catchment details (Site_code, Name, Eastings, Northings, Latitude, Longitude, Elevation, Survey, Catchment).
  - Data capture and processing steps emphasize ash-free corrections and standardized sample handling.

- Quality control and methods
  - Inorganic content correction for SOM samples (ash-free conversion).
  - Consistent sample handling: refrigeration, freeze-drying, grinding, and subsampling for isotopic and elemental analyses.
  - Replication across streams and multiple replicates (A–F) to support robust comparisons between reference and experimental zones.

- Potential analyses and applications
  - Compare upstream reference vs downstream experimental zones to assess the impact of leaf litter addition on SOM stocks.
  - Evaluate temporal changes from Before (T1) to After (T2) periods, including responses to storm-driven litter inputs.
  - Assess CPOM vs FPOM contributions and their isotopic signatures (δ13C, δ15N) to infer sources and processing.
  - Integrate discharge data to explore relationships between hydrology and SOM dynamics.
  - Use the data to support self-serve data exploration, dashboards, or reports on organic matter dynamics in river ecosystems.