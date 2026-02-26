# Soil aggregate stability data from arable and grassland in Countryside Survey, Great Britain 2007

- Study scope
  - Data on soil aggregate stability and particle size distribution (PSD) from arable and grassland plots across Great Britain, surveyed in 2007 as part of Countryside Survey.
  - Two linked data files: PSD measurements and derived aggregate stability metrics.

- Data files and key variables
  - Particle_Size_Distribution_data.csv
    - Coverage: 419 soils across 150 1 km squares; 5 plots per square.
    - Columns: SQUARE (1 km grid code), PLOT (plot within square), PSIZE (particle size class), VOL_WS (volume proportion in water-stable aggregates), VOL_SON (volume proportion after sonication).
  - Aggregate_stability_metrics.csv
    - Derived metrics for the same 419 soils.
    - Columns: MWD1 (mean weight diameter, water-stable aggregates), MWD2 (Mean Weight Diameter after sonication), DR (Disaggregation Reduction; DR = MWD1 − MWD2), LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07, plus metadata describing land class and location.

- Sampling design and geographic coverage
  - Countryside Survey 2007 framework: GB stratified by Land Classes across environmental gradients; 1 km × 1 km sample squares randomly selected within Land Classes.
  - Sample scale and distribution: 591 squares surveyed nationally (England, Scotland, Wales); 424 plots selected for aggregate stability analysis; 419 plots analyzed.
  - Soil sampling: top 0–15 cm; archived 2007 samples (air-dried, 2 mm sieved) re-homogenized and subsampled for analysis.
  - Representativeness: designed to produce reliable national statistics and reflect variation across England, Scotland, and Wales.

- Measurement approach and protocol
  - Core method: laser granulometry to determine Particle Size Distribution (PSD); Mean Weight Diameter (MWD) derived from PSD.
  - Aggregate stability metric: Disaggregation Reduction (DR) = MWD after water circulation (water-stable aggregates, MWD1) minus MWD after strong disruption via sonication (fundamental particles, MWD2). Higher DR indicates greater stability.
  - Protocol changes for this dataset (DR 2000, not DR 500):
    - No rescaling of PSD to <500 µm; larger mass of aggregates used (approx. 1.8×) and longer PSD measurement (60 seconds) than earlier methods.
    - Aggregate masses by texture: fine 0.55 g, medium 1.0 g, coarse 1.3 g (with a 7 m pipe added to the laser granulometer to increase circulating volume and mass handled).
    - Measurement: PSD analyzed for 60 seconds in both pre- and post-sonication stages; obscuration targets 1–3% before analysis and ≤30% after analysis to ensure accuracy.
    - Instrumentation: Beckman Coulter LS 13320 laser granulometer; sonicator: UP100H; temperature monitoring during tests; PSD measured across 92 size classes (0.375–2000 µm).
  - Pre-wetting and sample handling: standardized pre-wetting (30 minutes) using a two-filter paper setup to ensure even hydration; exact sample mass determined by incremental loading until instrument’s obscuration limit is reached; careful transfer of aggregates to the aqueous vessel.

- Quality control and assurance
  - Field and lab QA: trained field surveyors; use of a Countryside Survey soil work manual; archived palaeosol as an aggregate reference; standard PSD materials (32 µm and 500 µm) to check instrument accuracy.
  - Reproducibility checks: repeat analyses if obscuration exceeded 30% in post-sonication; regular calibration and cross-checks with reference materials.
  - Quality Management: UK Centre for Ecology & Hydrology operates ISO 9001:2015 certified Quality Management System; explicit QA policy and procedures.

- Data interpretation notes and caveats
  - Temporal and scale context: data reflect 2007 soil conditions across GB; potential limitations for local-scale inferences without additional context.
  - Methodological nuances: DR values in this dataset (DR 2000) are not rescaled to <500 µm (contrast with DR 500); ensure consistency when comparing with other studies or protocols.
  - Energy input and variability: the exact energy delivered by the sonicator is not directly quantified; procedure aims to standardize energy delivery, but micro-level variation may occur.
  - Data integration: variables include land class, country, county, and environmental zone descriptors to support cross-dataset analyses and regional comparisons.

- Usage context for analysts
  - Suitable for examining correlations between soil texture, aggregate stability (DR), and landscape factors across GB.
  - Can be combined with Countryside Survey environmental and land-cover data to model drivers of soil stability and to inform soil management or policy decisions.
  - The two linked data files enable both descriptive PSD analysis and stability-focused modeling (e.g., DR as a function of MWD1, MWD2, texture, land class, and region).

- References and provenance
  - Protocols and background described in Rawlins et al. (2013, 2015) for laser granulometry-based stability measurements.
  - Countryside Survey methodologies and soil sampling details outlined in Carey et al. (2008), Emmett et al. (2008, 2010), and related CEH technical reports.
  - Data produced under the Countryside Survey project and funded by NERC; data usage requires acknowledgement of Countryside Survey and UKCEH.