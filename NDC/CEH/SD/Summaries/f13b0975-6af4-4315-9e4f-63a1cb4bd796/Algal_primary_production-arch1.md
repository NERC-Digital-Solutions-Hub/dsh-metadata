# Experimental design/Sampling regime

- Study design and aim
  - A before-after-control-impact (BACI) framework comparing upstream reference (control) and downstream experimental (treatment) zones within each stream.
  - Aims to assess how added leaf litter affects algal production (via chlorophyll a) and related ecosystem responses.

- Experimental setup and spatial arrangement
  - Each stream segment divided into an upstream reference zone and a downstream experimental zone.
  - 20–50 m separation between zones to ensure independence.
  - Zones matched for length, habitat (riffle, glide, pool), slope, flow, substratum, and land use.

- Temporal framework
  - Before period (T1): 61–65 days, early Nov 2012 to early Jan 2013; no manipulation; both zones treated equally.
  - After period (T2): 57–62 days, Jan to Mar 2013; experimental zone receives leaf litter throughout.
  - Leaf litter treatment: one-tonne bags of oak, birch, alder distributed proportionally to experimental zone area; initial placement above the experimental zone but below the reference zone; maintain minimum wet weight of 1.7 kg/m^2 using vegetable nets.
  - Additional litter: 630 kg (wet weight) added on 12 Feb 2013 and 5 Mar 2013 after two large storm events, proportionally across streams.

- Experimental units and controls
  - Six algal tiles placed randomly in each reach (experimental sites) before and after manipulation.
  - Tile design: pair of unglazed ceramic tiles mounted on bricks; one tile treated with Vaseline on the vertical edge to deter grazers, the other left untreated as a control.

- Measurements and proxies
  - Algal production proxy: chlorophyll a accumulation on tiles.
  - Herbivory proxy: comparison between Vaseline-treated and untreated tiles.
  - Sampling periods aligned with before/after design and exposure durations.

- Field and laboratory methods
  - Tile collection: algae biofilm scrubbed, suspended, and frozen at -20°C.
  - Chlorophyll extraction: acetone extraction with spectrophotometric measurement.
  - Absorbance measurements: 664 nm (chlorophyll-a) and 750 nm (turbidity); chlorophyll-a concentration calculated with standardized formula.
  - Documentation and references for methods cited (Hladyz et al. 2011; Layer et al. 2010; Jenkins et al. 2013).

- Data structure and recorded variables
  - Data stored as flatbed CSV with 10 columns:
    - site_code, region, date, time (Before/After manipulation), landuse, reach, Vaseline (tile edge treatment) or none, treatment (Experimental/Control), replicate, exposure, chlorophyll (chlorophyll a, μg cm^-2).
  - Additional supporting data: site description file with metadata (site_code, name, coordinates, grid references, elevation, survey, catchment).

- Instrumentation and analysis notes
  - Laboratory instrument mentioned: mass spectrometer (context not detailed).
  - Primary analytical method described: chlorophyll-a quantification via spectrophotometry after acetone extraction.
  - Calibration steps: none reported.
  - Data quality controls: none reported in the document.

- Data and metadata availability
  - Datasets include chlorophyll A per area measurements and associated site/reach/treatment metadata.
  - Supporting metadata file: DURESS_CU_site_description.csv providing site descriptions and geographical coordinates.

- References and related sources
  - Hladyz, Åbjörnsson, Giller, and Woodward (2011) on impacts of riparian influences on stream ecosystems.
  - Layer et al. (2010) on food web structure and stability across pH gradients.
  - Jenkins, Woodward, and Hildrew (2013) on long-term effects of acidity on decomposition.

- Key opportunities for data analysis
  - Assess BACI-style treatment effects on chlorophyll a production across streams.
  - Explore differences between experimental and control tiles to quantify grazing pressure impacts.
  - Integrate leaf litter input, storm events, and exposure duration to model algal response dynamics.
  - Combine site metadata with chlorophyll data to examine spatial influences (land use, region, catchment).