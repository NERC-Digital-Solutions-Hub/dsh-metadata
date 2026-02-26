# Brief description of the dataset

- Overview
  - Weekly water quality monitoring data from 7 sites along the River Thames and 15 major tributaries, covering March 2009 to February 2013.
  - Parameters include nutrients (phosphorus forms, nitrogen species), dissolved silicon, water temperature, pH, Gran alkalinity, suspended solids, chlorophyll, major dissolved anions and cations, and dissolved/total metals.
  - Accompanied by daily mean river flow data; part of the Centre for Ecology & Hydrology's Thames Initiative monitoring programme.

- Monitoring and analytical information
  - Sampling: bulk samples collected from the main river flow on Mondays or Tuesdays each week; subsamples filtered in the field at 0.45 μm.
  - Sample handling: samples stored in the dark at 4°C before analysis.
  - Measurements and methods:
    - pH measured with a calibrated Radiometer pH meter (buffers 4, 7, 10; traceable to NIST).
    - Gran alkalinity by acidimetric titration to pH 4 and 3 with 0.5N H2SO4.
    - Suspended solids by filtering ~500 ml, drying, and reweighing.
    - Chlorophyll a by filtration, acetone extraction, and spectrophotometric analysis.
    - Total and dissolved phosphorus via persulfate digestion and colorimetric detection; SRP via Murphy & Riley method with modified protocol.
    - Soluble reactive phosphorus (SRP) via 0.45 μm filtered samples with molybdate chemistry.
    - Dissolved reactive silicon by molybdate reduction to silicomolybdenum blues and spectrophotometry.
    - Ammonium by indophenol-blue colorimetric method.
    - DOC and TDN by thermal oxidation (until Dec 2010) and then using a Vario Cube analyzer (from 2011).
    - Major dissolved anions by ion chromatography.
    - Total and dissolved cations by ICP-OES after appropriate filtration and acidification.
  - QA: all analyses conducted with reference Aquacheck QC standards.

- Data, flow, and site coverage
  - Water quality data provided alongside mean daily flow data from the National River Flow Archive.
  - Most sites near Environment Agency gauging stations.
  - Exceptions and data handling:
    - Jubilee River flow data derived from Windsor gauges (amalgamated river flows, not Jubilee River alone).
    - Flows at Hannington Wick, Wallingford, and Sonning interpolated from catchment-area data using multiple gauging stations along the Thames.
    - Cut and River Kennet sites use gauging data upstream of monitoring sites.

- Format and dataset structure
  - Date/time format: day/month/year; sampling time in hour:minute.
  - Concentration data expressed as phosphorus concentrations (TP, TDP, SRP) and other measured concentrations in specified units.
  - Total vs. dissolved metals derived from unfiltered vs filtered samples.
  - Temperature in °C; pH (no units); alkalinity in micro-equivalents per litre.
  - Solids, chlorophyll a, various anions and cations, ammonium, and other constituents with specified units (e.g., mg/L, μg/L, μg/L, etc.).
  - Flow data: mean daily flow in cubic metres per second.

- References and methodological basis
  - Eisenreich et al. (1975) – simplified phosphorus analytical technique.
  - Leeks et al. (1997) – LOIS river monitoring network strategy.
  - Marker et al. (1980) – measurement of photosynthetic pigments in freshwaters.
  - Mullin & Riley (1955) – silicate colorimetric method.
  - Murphy & Riley (1962) – phosphorus determination (molybdate method).
  - Neal et al. (2000) – phosphate measurement and silica interference considerations.

- Relevance for monitoring framework authors
  - Demonstrates a comprehensive, field-implemented monitoring dataset with detailed analytical methods, QA practices, and metadata.
  - Shows integration of water quality data with river flow data to support interpretation and policy evaluation.
  - Highlights practical data governance considerations (transparent methodology, QC standards) and potential data-availability challenges (flow data interpolation, site coverage, temporal scope).
  - Useful for informing the design of monitoring measures, data quality requirements, and data sharing practices in environmental health monitoring frameworks.