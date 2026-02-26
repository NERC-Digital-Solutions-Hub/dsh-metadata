# Experimental design/Sampling regime

- Study design
  - Before-after-control-impact (BACI) experiment in streams.
  - Each stream divided into upstream reference zone and downstream experimental zone.
  - Zones within each stream are similar in length, habitat structure, slope, flow, substratum, and land use.
  - 20–50 m separation between reference and experimental zones to ensure independence.

- Temporal framework
  - Before period (T1): 61–65 days, from early November 2012 to early January 2013; no manipulation; both zones treated equally.
  - After period (T2): 57–62 days, from early January 2013 to March 2013; experimental zone manipulated with leaf litter throughout.
  - January samples belong to the before period; February–April samples belong to the after period.

- Leaf litter manipulation
  - One tonne bags containing deciduous leaves (oak, birch, alder) distributed proportionally by experimental zone area.
  - Leaf packs fixed above the experimental zone below the reference zone to simulate natural senescence.
  - Vegetable net bags maintained minimum wet weight of 1.7 kg m-2 (wet).
  - Additional leaf litter (630 kg wet weight) added to each stream on 12 February 2013 and 5 March 2013 after two large storm events.

- Experimental units and measurements
  - Six experimental units (algal tiles) per reach; tiles placed randomly in the reach.
  - Chlorophyll a accrual on tiles used as a proxy for algal production; herbivory rates inferred from grazing pressure assessments.
  - Tile setup: unglazed ceramic tiles (100 x 100 mm) paired on bricks; one tile edges treated with petroleum jelly to deter grazing; other tile serves as a control.

- Field and laboratory methods
  - In-field assembly and sampling described elsewhere; mass spectrometry equipment referenced for laboratory work.
  - Algal biofilm collection: biofilm scrubbed from tiles, frozen at -20°C.
  - Chlorophyll extraction: 20 ml of biofilm suspension filtered and extracted in 90% acetone at 4°C in the dark for 12 hours.
  - Spectrophotometric measurement at 664 nm (chlorophyll-a) and 750 nm (turbidity) using a Biowave spectrophotometer.

- Data and variables
  - Recorded values: chlorophyll a per area (μg cm^-2).
  - Calibration and reference materials include published methodologies (citations provided in the doc).

- Data structure and metadata
  - Data stored as flatbed comma-separated value (CSV) files.
  - Algal production dataset consists of 10 columns:
    - site_code, region, date, time, landuse, reach, treatment, replicate, exposure, chlorophyll
  - NA indicates missing data.
  - Supporting metadata file: DURESS_CU_site_description.csv containing site_code, name, coordinates, grid, latitude/longitude, elevation, survey, catchment, and related descriptors.

- Units and calculations
  - Chlorophyll a concentration per area reported in micrograms per square centimeter (μg cm^-2).
  - The calculation formula and constants are documented (A, K, absorbance at 664/750 nm, volume, surface area, path length).

- Quality control and governance
  - Quality control steps are not documented in the dataset.
  - Data are linked to external site descriptions for geospatial context.
  - Data structure and variable definitions are provided to support interoperability and reuse.

- Relevant references and supporting materials
  - Links and citations to foundational methods and related studies are provided within the document (e.g., Layer et al. 2010; Hladyz et al. 2011; Jenkins et al. 2013).