# Amazon Fertilization Experiment (AFEX)

- Study context
  - Location: BDFFP area, KM41 reserve, ~100 km from Manaus, Central Amazon (02°24'S, 59°52'W). Ferralsols soils; annual rainfall 1900–2500 mm with a pronounced dry season (Jun–Oct).
  - Forest structure context: AGB ~322 ± 54 Mg ha-1 (≥10 cm dbh); mean wood density ~0.67 g cm-3; ~280 species per hectare (≥10 cm dbh).

- AFEX experimental design
  - Full factorial fertilization with eight treatments across four replicates (32 plots) arranged in four independent blocks at least 200 m apart.
  - Treatments: Control; N (125 kg N ha-1 year-1 as urea); P (50 kg P ha-1 year-1 as triple superphosphate); cations (K, Ca, Mg as KCl and dolomitic limestone); and all combinations: N+P; N+cations; P+cations; N+P+cations.
  - Plot configuration: 50 x 50 m plots, minimum 50 m apart; plots established in areas with similar soil, vegetation, and topography.
  - Fertilization method: Annual application divided into three applications to mitigate leaching/runoff; fertilizers spread by hand during systemic walks.

- Data collection methods
  - LAI measurement: 36 points per plot using LAI-2200 C instrument; measurements taken from 6:00–17:00 (excluding 12:00–14:00 to avoid direct sun).
  - Protocol details: Above-canopy reference reading required; optical sensor positioned in a clearing; sensor orientation fixed (west in morning, east in afternoon); view cap used to avoid operator intrusion; sensors matched prior to collection.
  - Data processing: LAI computed with FV2200 software at three ring configurations (5 rings, 4 rings, 3 rings) to capture different zenith angle ranges.
  - Sampling timeline: October 2017, March 2018, August 2018, and October 2018 (within a Central Amazon fertilization experiment).

- Data spreadsheet and schema
  - Dataset name: Leaf area index data spreadsheet deposited in the EIDC system.
  - Key columns and content:
    - Col A, B: Sampling number (CENSO) and PlotID (block/plot code)
    - Col C: B_Obs (36 points)
    - Col D, F, H: Time stamps for LAI measurements (LAI_5_rings, LAI_4_rings, LAI_3_rings)
    - Col E, G: LAI values for 5, 4, and 3 rings respectively
    - Col J: Date (campaign date in year_month)
    - Col K, L: coord x and coord y within plots (0–50 m grid)
  - Additional context: Each row corresponds to a measurement event per plot and time, with multiple rings providing LAI estimates.

- Data governance and references
  - Data are organized to enable traceability across plots, treatments, dates, and sampling points; coordinates and timestamps support reproducibility and spatial analyses.
  - References cited for context on Amazonian forest structure and soils, and RAINFOR-related studies.