# Sampling Regime

- Study area and timeframe
  - Western Amazonian basin, Tambopata National Reserve, Madre de Dios region, Peru (12°49'54.30"S, 69°16'52.37"W)
  - Data collected Feb 2011 – May 2012
  - Targeted fluvial carbon metrics across different seasons (wet and dry)
  - Sampling sites include two small streams (MT/Main Trail; NC/New Colpita) and two rivers (LT/La Torre; TP/Tambopata)
  - MT dries out in the dry season; NC flows year-round
  - Upstream catchments: MT/NC ~4.9–7.2 km2; LT ~2000 km2; TP ~14000 km2

- Datasets and measurements
  - Fluvial carbon data (streams and rivers): dissolved inorganic carbon (DIC) and its δ13C-DIC; dissolved organic carbon (DOC); particulate organic carbon (POC)
  - Rainfall fractions: rain water, throughfall, stemflow, and overland flow; analysed for DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na, total dissolved P (totP), and Si
  - Data points: DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na, P, Si values collected per site
  - Rainfall fractions data points: subset collected for each fraction (DIC, δ13C-DIC, DOC, POC, Ca, Mg, K, Na, totP, Si)

- Data submission and availability
  - Data previously submitted for DIC and/or related measurements with DOIs:
    - DIC and related data: DOI 10.5285/507a5e1f-e056-454c-8ff6-d185f3da8556
    - DIC data (rivers) with flux and velocity measurements: DOI 10.5285/02d5cea7-10aa-4591-938a-a41e1c5bc207
  - Current document references and consolidates multiple campaigns and data re-submissions
  - Data structure: two CSV files
    - Amazon streams C and nutrients (14 data columns)
    - Amazon rainfall fractions C and nutrients (12 data columns)

- Sampling and collection methods
  - Fluvial sampling campaigns: Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012
  - DIC: collected in pre-acidified exetainers; headspace method via GasBench/Delta V Plus; triplicate samples with a backup
  - DOC: collected in pre-cleaned bottles; filtered (0.7 μm GF/F); acidified to pH 3.9; degassed; concentration by TOC combustion
  - POC: determined by loss on ignition of filtered sample filters
  - Ca, Mg: atomic absorption spectrometry (AAS) with N2O flame
  - K, Na: flame photometry
  - TotP: colorimetric phosphomolybdate/ascorbic acid method
  - Si: colorimetric heteropoly blue molybdosilicate method
  - Throughfall, stemflow, rainwater: collected using replicated collectors near TAM9 plot and an open area near Explorer’s Inn Lodge
  - Stemflow: eight sampled trees, various species; stemflow collected via half-pipe tubing around tree trunk
  - Overland flow: simple collection on river banks; volume not quantified, but samples collected for composition analyses

- Quality control and calibration
  - DIC: drift correction standards every ~10 samples; randomised sample order; regular drift/quality control standards
  - DOC: eight-point calibration; blanks and drift checks; subset calibrations compared for consistency
  - Cations (Ca, Mg) and nutrients (K, Na): calibration standards (five-point for Ca/Mg; K/Na with appropriate ranges); blank and mid-range standards checked
  - Si and totP: instrument stability monitored via repeated standard analyses

- Data structure and contents
  - Streams and Rivers file: 14 columns per record
  - Rainfall fractions file: 12 columns per record
  - Common fields include:
    - Time (hh:mm:ss) and Date (dd/mm/yyyy)
    - Type (Streams/Rivers; or TF/SF/OF/RW for rainfall)
    - Site/Collector ID (MT, NC, LT, TP; TF collector numbers; SF tree names; EI for Explorer’s Inn)
    - Concentrations: DOC, POC, DIC, δ13C-DIC
    - Nutrients: Ca, Mg, K, Na
    - Analytes: TotP, Si
  - Data qualifiers: NA indicates not analyzed for that entry
  - Units follow standard methods described in the methods section

- References and further reading
  - American Public Health Association (1999), Standard methods for the examination of water & wastewater
  - Waldron, S., et al. (2014), Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry

- GIS relevance and potential applications
  - Spatial mapping of sampling sites (MT, NC, LT, TP) and catchment extents
  - Visualization of spatial patterns in DIC, DOC, POC and isotopic signatures across streams and rivers
  - Seasonal/hydrological analysis by linking sampling campaigns to wet/dry seasons
  - Integration of rainfall fraction data with river data to study carbon fluxes and nutrient transport in the Amazonian rainforest
  - Linking to upstream catchment areas (LT and TP) for exploring watershed-scale carbon dynamics