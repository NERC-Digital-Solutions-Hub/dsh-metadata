# High temporal resolution meteorology and soil physics observations from INCOMPASS land surface stations in India, 2016 to 2018

- Overview
  - A dataset of one-minute time series observations for meteorology and soil physics across three INCOMPASS Land Surface Stations in India, recorded from 2016-01-01 00:01 to 2019-01-01 00:00 (Kanpur dataset ends 2018-08-28 06:23).
  - Sites span southern Karnataka and Uttar Pradesh, with distinct climatic and soil contexts.
  - Data are provided as CSV files with complete time series and -9999 denoting missing records.

- Sites and sampling regime
  - Berambadi, Southern Karnataka: agricultural land on the Deccan Plateau (11.760633 N, 76.585361 E; 873 m amsl); semi-arid tropical monsoon climate (Aw); Alfisol soils; near Bangalore.
  - Dharwad, Dharwad District, Northern Karnataka: agricultural campus site (15.498393 N, 74.985730 E; 692 m amsl); tropical savannah climate (Aw); Vertisol soils; long-standing agricultural field with crop rotations.
  - Kanpur, IIT Kanpur, Uttar Pradesh: semi-natural grassland (26.509072 N, 80.223765 E; 129 m amsl); humid subtropical climate (Csa); Fluvisol soils; periodic surface flooding and shallow standing water.
  - Sampling period: Berambadi and Dharwad collected 2016-01-01 to 2019-01-01; Kanpur collected 2016-01-01 to 2018-08-28.
  - Instrumentation and standardized measurement setup were identical across all sites.

- Measurements and instrumentation
  - Meteorological measurements (10 m mast) include:
    - Barometric pressure (PA, kPa)
    - Air temperature (Ta, °C) and relative humidity (RH, %)
    - Net radiation and components: SWin, SWout, LWin, LWout, Rnet (W m-2)
    - Precipitation (mm per minute)
    - Wind speed (WS, m s-1) and wind direction (WD, degrees)
  - Soil physics measurements (two co-located locations, two depths):
    - Soil heat flux (G, W m-2) at 0.03 m depth
    - Soil volumetric water content (VWC, %) at 0.05 m and 0.15 m depths
    - Soil temperature (Tsoil, °C) at 0.05 m and 0.15 m depths
  - Instruments include LI7500A for pressure, HMP155 for Ta/RH, TS-100 shield, NR01 Net Radiometer, WindSonic, SBS314 rain gauge, HFP01-SC flux plates, ACC-SEN-SDI sensors.
  - Data logged at 0.1 Hz and aggregated to one-minute means; rainfall data summed per minute.
  - Duplicated soil observations at two locations and two depths for QC.

- Data structure and content
  - Each station provides a separate CSV with a uniform column schema (Table 2 reference).
  - Columns include: DateTime (IST, end of each one-minute period), Pa, Ta, RH, SWin, SWout, LWin, LWout, Rnet, Precipitation, WS, WD, G1, G2, Tsoil_0.05_1, Tsoil_0.15_1, Tsoil_0.05_2, Tsoil_0.15_2, VWC_0.05_1, VWC2_0.15_1, VWC1_0.05_2, VWC2_0.15_2.
  - Missing data are denoted by -9999.
  - IST timestamps correspond to UTC+5:30.

- Quality control and data processing
  - QC procedures include basic range checks, spike/dropout visual checks, and cross-verification between paired soil observations.
  - Large soil moisture shifts cross-checked with rainfall and flooding events (notably at Kanpur).
  - Clearly erroneous data are removed to ensure data integrity.
  - Soil data cross-checked across depths and locations for consistency.

- Contextual metadata and data provenance
  - Site characteristics include coordinates, altitude, dominant land use, climate classification, and soil orders (Berambadi: Alfisol; Dharwad: Vertisol; Kanpur: Fluvisol).
  - Cropping schedules around Dharwad documented (Table 2) reflecting agricultural influences on microclimate and fluxes.
  - Observations were collected with identical instrumentation at all three sites.
  - Acknowledgments note UK-India collaboration under INCOMPASS, with funding from NERC and MoES, and contributions from multiple partners.

- Potential uses for analysts
  - Identify correlations among meteorological drivers, soil moisture, and soil temperature at shallow depths.
  - Develop predictive models of surface energy balance components and moisture dynamics under varied climate and land-use contexts.
  - Integrate with other regional data to upscale land-surface processes or validate land-surface models during monsoon onset and nears.
  - Analyze local-scale variability across agricultural (Berambadi, Dharwad) and grassland (Kanpur) environments.
  - Address data gaps and scale challenges by leveraging replicated soil measurements and high temporal resolution data.

- Reuse considerations
  - Data are high-resolution but locally scoped to three stations; consider scale when generalizing.
  - Missing data (-9999) require处理 in analysis (e.g., imputation or QC-aware modeling).
  - IST time zone must be accounted for in temporal analyses and alignment with other datasets.