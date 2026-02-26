# Overview of the dataset

- Purpose and GIS relevance
  - Provides spatially explicit measurements of net ecosystem CO2 exchange (NEE) and methane fluxes (CH4) across a transect in a hemi-boreal fen, enabling map-based visualization and spatial-temporal analysis of greenhouse gas fluxes.
  - Useful for comparing ecotype responses (sphagnum, eriophorum, heather, open water) and drought effects (2018 vs 2019) in a GIS context.

- Study site and scope
  - Location: Mycklemossen fen, ombrotrophic bog-like fen, ~100 km north of Gothenburg, Sweden (58.3673 N, 12.1686 E; ~75 m a.s.l.).
  - Part of the Skogaryd research catchment; typical vegetation includes sphagnum, Calluna vulgaris (heather), and Eriophorum vaginatum (sedges).
  - Timeframe: August 2017 to September 2019; drought conditions in 2018 with a recovery observed in 2019.
  - Ecotypes analyzed: sphagnum, eriophorum, heather, and open water (water).

- Experimental design and sampling
  - A transect was established with spatial blocks along the transect; within each block, 24 measurement points were defined (6 replicates per ecotype: sedge/eriophorum, heather, sphagnum, water; total 24 points).
  - At each point, a PVC collar was installed to collect flux measurements.

- Measurement methods and instrumentation
  - Flux measurements along the transect using SkyLine2D, an automated chamber system.
  - Chamber: clear Perspex cylinder, 20 cm inner diameter, 40 cm height; lowered onto collars and measured for four minutes.
  - System cycle: complete cycle ~2.5 hours, yielding ~10 measurements per day per chamber.
  - Instrumentation: LI-COR LI-8100 for CO2; LGR UGGA-91 CRD for CO2 and CH4.
  - Flow and mixing: no fan; headspace flow considered sufficient; data logged with a Campbell Scientific data logger.
  - Corrections: daylight-based adjustment of CO2 fluxes to account for chamber material light attenuation; other standard adjustments for area, air temperature, and gas volume.

- Data processing and quality control
  - Software: SAS 9.4 used for data manipulation and analyses.
  - QC criteria: CO2 flux quality via R^2 ≥ 0.9; CH4 flux regressions with P < 0.05 accepted, else treated as zero flux.
  - Outlier handling: fluxes ±1.96 standard errors excluded.
  - Night-time/atmospheric filtering: excluded fluxes affected by still air conditions (per Koskinen 2014; Lai 2012) and instances where pre/post 20-second CO2 concentration change exceeded 25 ppm (per Jarveoja 2020); 329 fluxes excluded.
  - Result: curated dataset intended for robust regional and ecotype-specific flux analyses.

- Data structure and variables
  - Dataset consists of a single table with eight columns:
    - DATETIME: date-time of measurement (dd:mm:yyyy:hh:mm:ss)
    - DATE: date of measurement (dd/mm/yyyy)
    - TIME: time of measurement (hh:mm:ss)
    - PLOT: experimental plot number
    - ECOTYPE: dominant vegetation type for the plot (sphagnum, heather, eriophorum, water)
    - BLOCK: block identifier (numeric)
    - CH4_flux: methane flux (nmol m^-2 s^-1)
    - CO2_flux: net ecosystem exchange of CO2 (µmol m^-2 s^-1)

- Provenance, references, and contact
  - Primary data collection and interpretation credited to Keane, Toet, Ineson, Weslien, Stockdale, and Klemedtsson; contact Sylvia Toet for inquiries.
  - Related methodological and interpretive context available in cited literature (Keane et al. 2018, 2021; Koskinen 2014; Lai 2012; Jarveoja 2020; Mosier 1989; Heinemeyer 2013).

- Practical GIS considerations and caveats
  - Spatial granularity: 24 measurement points along a transect across four ecotypes; suitable for mapping ecotype-specific flux patterns but limited for fine-scale heterogeneity beyond the transect.
  - Temporal resolution: repeated measurements within days; diurnal and seasonal patterns analyzable, with drought vs nondrought comparison possible for 2018 vs 2019.
  - Data compatibility: flux units and timing standardized for integration with GIS layers (ecotope, plot, and block attributes); careful alignment with meteorological or soil data recommended for interpretation.
  - Limitations: chamber footprint and transect-based sampling may not capture full landscape-scale flux variability; data filtered for quality may reduce sample size in certain periods.