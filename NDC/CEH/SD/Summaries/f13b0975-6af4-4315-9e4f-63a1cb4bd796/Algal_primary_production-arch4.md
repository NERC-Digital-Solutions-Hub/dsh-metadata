# Experimental design/Sampling regime

- Study design and scope
  - Before-After-Control-Impact (BACI) design with an upstream reference zone and a downstream experimental zone.
  - Each stream section matched in length, habitat type, slope, flow, substratum, and land use; 20–50 m separation to ensure independence.
  - Time periods: before period (T1, ~61–65 days) from early Nov 2012 to early Jan 2013 with no manipulation; after period (T2, ~57–62 days) from early Jan to March 2013 with leaf litter manipulation in the experimental zone.

- Treatments and sampling timeline
  - In Jan 2013, add leaf litter to the experimental zone using one-tonne bags containing deciduous leaves (oak, birch, alder) proportionally to experimental area to simulate natural senescence.
  - Maintain a minimum wet weight of 1.7 kg/m^2 in the experimental zone via vegetable nets; bags fixed within the wetted channel.
  - Additional leaf litter (630 kg wet weight) added to each stream on 12 Feb and 5 Mar 2013 after two large storm-flow events.
  - Experimental design supports evaluation of leaf litter effects on algal production and stream ecosystem processes.

- Experimental units and response measures
  - Six algal tiles per reach placed randomly in the experimental sites before and after manipulation.
  - Chlorophyll a on tiles used as a proxy for algal production; herbivory rates assessed via paired tiles.
  - Tile setup: unglaзed ceramic tiles fixed to bricks; one tile edge treated with petroleum jelly to deter grazing (vaselined tile) and a second tile left as a control.

- Data collection and laboratory methods
  - Field instruments: algal tiles deployed in each reach; sampling periods aligned with before/after manipulation.
  - Laboratory analysis: chlorophyll a extraction and measurement via spectrophotometry; details include acetone extraction, filtration, and absorbance readings at 664 and 750 nm.
  - Calculation: chlorophyll a concentration per area derived from a specified formula with constants and sample-specific parameters (volume of acetone, surface area, path length, etc.).
  - Note: a mass spectrometer is referenced in the laboratory context; chl-a measurements are performed with a spectrophotometer (Biochrom).

- Data structure and metadata
  - Data stored as flat, comma-separated value (CSV) files.
  - Algal production data include 10 columns:
    - site_code, region, date, time (Before/After), landuse, reach, Vaseline (yes/no), treatment, replicate, exposure, chlorophyll (µg/cm^2)
  - Additional site-level metadata provided in DURESS_CU_site_description.csv, including:
    - Site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment
  - Columns capture spatial (site, catchment), temporal (date, time, exposure days), treatment (experimental vs control, vaseline), and response (chlorophyll a) information.

- Quality control and calibration
  - Calibration steps: None specified.
  - Quality control: None specified.

- Supporting documents and references
  - Supporting file: DURESS_CU_site_description.csv with site descriptions and coordinates.
  - Key references for methods:
    - Hladyz et al. 2011 (leaf litter impacts on stream food webs)
    - Layer et al. 2010 (food web structure across pH gradient)
    - Jenkins, Woodward & Hildrew 2013 (acidification effects on decomposition)
  - URLs provided for referencing the sources.

- Units and data interpretability
  - Response variable: chlorophyll a per unit area, expressed as micrograms per square centimeter (µg cm^-2).
  - Time/phase indicators distinguish Before (T1) vs After (T2) and Experimental vs Control conditions.