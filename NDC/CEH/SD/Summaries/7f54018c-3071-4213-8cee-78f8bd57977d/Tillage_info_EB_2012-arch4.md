# Nitrous oxide fluxes from an intensively managed grazed grassland in Scotland

- Purpose: Measure N2O fluxes from two grassland fields (tilled vs un-tilled) before and after a tillage event on 1 May 2012 to understand how tillage affects soil–atmosphere N2O exchange.

- Location and seasonality:
  - Easter Bush, Scotland (55° 51' 55.30"N, 3° 12' 22.17"W)
  - Temperate maritime climate; ~921 mm annual rainfall; ~9°C average temperature (2001–2011)
  - Two adjacent fields (~5.4 ha each) with ~20+ years of intensive livestock production; typical N fertiliser ~200 kg N ha-1 y-1

- Soil and drainage:
  - Clay loam (top 30 cm: ~52/20/28; tilled field slightly different)
  - pH ~5.1; imperfectly drained Macmerry soil; drainage system ~50 years old and poorly functioning, causing surface water during rain

- Management differences:
  - South (tilled) field: ploughed to 30 cm depth on 1 May 2012 after glyphosate kill; harrowed, rolled, seeded with ryegrass; one N fertiliser event (70 kg-N ha-1) on 9 Aug 2012
  - North (un-tilled) field: grazed by ~30 sheep ha-1; continued fertiliser applications (two 70 kg-N ha-1 applications on 28 May and 9 Aug 2012)
  - Tillage occurred in May 2012; tilled field received no earlier tillage for ~20 years

- Data focus:
  - Quantify soil N2O fluxes using two measurement approaches around the tillage event:
    - Eddy covariance system for continuous, landscape-scale flux estimates
    - Static and dynamic chamber flux measurements for localized, soil-surface fluxes

- Data infrastructure and metadata:
  - Detailed event chronology (dates/times of management practices) recorded for both fields
  - Field management data linked to flux measurements to interpret flux responses
  - Data files catalogued with explicit variable definitions and measurement timestamps

- Key methodological elements:
  - Eddy covariance:
    - Instrumentation: 3-axis ultrasonic anemometer at 2.4 m; quantum cascade laser (QCL) analyser for N2O, H2O, CO2
    - Sampling: 10 Hz; fluxes computed at 30 min intervals via covariance (chi prime w prime)
    - Corrections: double coordinate rotation, spike removal, time lag optimization; frequency response correction (Moncrieff et al. 1997); density corrections (Burba et al. 2012)
    - Quality control: Foken et al. (2005) category 2 data removed; wind-direction-based field attribution to separate tilled vs un-tilled data; obstructions excluded
  - Chamber measurements:
    - Static chambers: PVC cylindrical chambers (38 cm ID, 22 cm height) inserted 5 cm; 40-minute incubation with three 100 mL samples (0, 20, 40 min)
    - Dynamic chambers: closed system connected to QCL; 30 m radius from instrument cabin; ~6–7 L min-1 flow; ~22 s lag; data analyzed with linear and non-linear regression to estimate flux
    - Flux calculations: static F = (dC/dt) × (ρV)/A; dynamic fluxes derived from time-series regression
    - Detection limits: static ~0.4 nmol m-2 s-1; dynamic ~0.04 nmol m-2 s-1
  - Footprint and data alignment:
    - Eddy covariance and chambers positioned to represent measurement footprints within ~10–200 m from the mast
    - Data processing aligned with measurement events, footprints, and field management activities

- Data records and structure:
  - Eddy covariance dataset: Easter_Bush_EddyC_Tillage_2012
    - Includes: tau (momentum flux), H (sensible heat), LE (latent heat), co2_flux, h2o_flux, n2o_flux, wind_speed, wind_dir, u* (friction velocity), TKE, L, (z-d)/L, bowen_ratio, and related metadata
  - Chamber dataset: Easter_Bush_Chambers_Tillage_2012
    - Includes: location, field name, chamber method, date, flux (nmol N2O m-2 s-1), time, air temperature, soil temperature, rainfall, PAR, etc.
  - Data organization emphasizes linkage between management events, measurement campaigns, and flux estimates

- References and validated methods:
  - Established approaches for eddy covariance data processing, density corrections, and flux uncertainty
  - Validated chamber methodologies (static and dynamic) for soil N2O flux quantification
  - Key methodological sources cited for calibration, correction, and uncertainty assessment

- Caveats and limitations:
  - Data quality can be affected by wind direction and obstructions (leading to data exclusion)
  - Footprint differences between tilled and un-tilled fields require careful attribution
  - Imaging and measurement gaps around specific events (e.g., tillage timing, equipment access) may influence temporal flux interpretation

- Relevance to data governance and management:
  - Demonstrates comprehensive data collection across multiple flux measurement platforms tied to management events
  - Highlights importance of detailed metadata (field history, tillage timing, fertilisation) for interpretability and cross-field comparisons
  - Emphasizes robust QC, standardized processing workflows, and clear data record structures for reuse and integration with broader datasets