# Experimental design/Sampling regime

- Overview of design
  - Before-after-control-impact (BACI) with each stream having an upstream reference zone and a downstream experimental zone.
  - Zones are similar in length and habitat; ~20–50 m separation to ensure independence.
  - Time frame:
    - Before period (T1): 61–65 days from early Nov 2012 to early Jan 2013; no manipulation; equal treatment of reference and experimental zones.
    - After period (T2): 57–62 days from early Jan 2013 to Mar 2013; experimental zone receives leaf litter addition throughout.
  - Leaf litter manipulation:
    - One-tonne bags of oak, birch, and alder leaves added proportionally to experimental zones to simulate natural senescence.
    - Target minimum wet weight: 1.7 kg m^-2 in the experimental zone.
    - Additional litter: 630 kg (wet weight) added on Feb 12 and Mar 5 after two large storm events.

- Experimental setup and measures
  - Six experimental units (algal tiles) placed randomly in each reach (before and after manipulation).
  - Chlorophyll a on tiles used as a proxy for algal production and herbivory rates.
  - Tile design includes paired tiles per brick: one tile coated with Vaseline to deter grazing; the other left uncoated as a control.

- Collection methods and laboratory analysis
  - Field methods described elsewhere; six tiles per reach analyzed pre- and post-manipulation.
  - Laboratory analysis:
    - Algal biofilm scrubbed, frozen at -20°C.
    - Chlorophyll extracted with acetone and quantified spectrophotometrically.
    - Measurements at 664 nm (chlorophyll-a) and 750 nm (turbidity).
    - Chlorophyll-a concentration calculated using a specified equation.
  - Instrumentation note: a mass spectrometer was used in the laboratory (details referenced below).

- Data structure and units
  - Data stored as flatbed CSV files.
  - Chlorophyll-a per area expressed as micrograms per square centimeter (μg cm^-2).
  - Data columns (10): site_code, region, date, time, landuse, reach, treatment (experimental or control; Vaseline or no-vaseline edge treatment noted), replicate, exposure (days), chlorophyll.

- Data quality, calibration, and limitations
  - Calibration steps and quality control: None described.
  - No explicit QA/QC procedures noted in the dataset details.

- Supporting data and metadata
  - Site description file: DURESS_CU_site_description.csv, with fields for site_code, name, coordinates (Eastings/Northings, latitude/longitude), grid, elevation, survey campaign, and catchment.

- References and related data sources
  - Method references for chlorophyll and ecological context:
    - Hladyz et al. 2011
    - Layer et al. 2010
    - Jenkins, Woodward, and Hildrew 2013

- Additional notes
  - The document references collection methods for materials and instruments; exact procedural details available in that section.