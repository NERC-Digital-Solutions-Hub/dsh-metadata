# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment in Clocaenog Forest, North East Wales, established in 1998 to simulate upland moorland climate futures over the next 20–30 years.
- Automated roof technology powers drought and warming treatments, with plots designed to be solar/wind powered and remotely operated.
- Site supports extensive multi-disciplinary environmental monitoring, spanning meteorology, hydrology, soil, vegetation, and biogeochemical processes.

## Key context and site characteristics

- Ecosystem: Wet upland heath dominated by Calluna vulgaris (heather); notable presence of Vaccinium myrtillus, Empetrum nigrum, and bryophytes.
- Soil: Humo-ferric podzol with variable eluvial/illuvial horizons; depth and horizon visibility vary across the site.
- Climate baseline: Site-level data include mean air temperature around 8.0°C and mean annual rainfall ~1411 mm (historic 1997–2014 period); N deposition ~20–25 kg N ha⁻¹ yr⁻¹.
- Vegetation baseline measurements include biomass, species composition, litter, canopy traits, and phenology across several years.

## Climate change treatment information

- Treatments and replication: Two climate manipulation treatments (drought and warming) with three replicate plots each, plus three control plots to mirror shading and allow comparisons (total 9 plots, organized in blocks).
- Drought treatment:
  - Operation: Retractable polyethylene roof over each plot during drought periods to exclude rainfall.
  - Timing: May–September (1999–2011); since 2012: April–October.
  - Rainfall impact: Reduces annual rainfall by about 20% on average; excludes ~80% of rainfall during drought periods due to sensor thresholds.
  - Wind constraints: Curtains do not operate in winds > 10 m s⁻¹.
- Warming treatment:
  - Operation: Retractable aluminium mesh curtains that reflect infrared radiation, reducing night-time heat loss.
  - Trigger: Night-time operation triggered after a period of darkness; rainfall triggers retraction to preserve rainfall.
  - Rainfall impact: Reduces annual rainfall by about 14%.
  - Wind constraints: Curtains retracted during rainfall and do not operate in high winds.
- Controls: Scaffolding mirrors shading from treatment structures to isolate treatment effects.
- Layout: Treatments distributed across plots with block structure to balance environmental variation.

## Equipment, protocols and data processing methodology

- On-site data architecture:
  - Automated Weather Station (AWS) for meteorological data (daily; 1999–current).
  - Micro-meteorological plots for soil/air temperature and soil moisture (daily; 1998–current).
  - Plot-level rainfall and rainfall chemistry (monthly to biweekly).
  - Throughfall (plot-level rainfall) and site rainfall data (biweekly to fortnightly).
  - Groundwater/water table depth via permeable tubes (biweekly from 2009).
  - Soil respiration and trace gas fluxes (CH4, N2O) using soil collars and chamber methods; both historical and automated measurements (1999–present with gaps).
  - Net ecosystem CO2 exchange (NEE) measurements (2002–2004, 2009–2011) using closed-chamber systems.
  - Photosynthesis measurements (ambient and response curves) across multiple years.
  - Vegetation surveys (pin-point biomass), canopy reflectance (NDVI and PRI indices), phenology and pathogen assessment, and vegetation chemistry.
  - Litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC and bulk density, soil solution and leachate chemistry (biweekly to monthly or infrequent).
- Data processing and standardization:
  - Unit conversions between multiple measurement systems (e.g., CIRAS-2, LICOR 8100).
  - Calibration steps: Pin-hit biomass calibration; biomass-adjusted NEE and photosynthesis.
  - Historical methodological transitions: various instruments and methods over time (e.g., soil respiration measurements transitioning from CIRAS-based to LI-COR–based systems; move to automated measurements in 2013–2014).
  - Metadata and supporting documentation provided for many datasets; some legacy data processing steps are not fully documented.
- Data quality and validation:
  - Routine quality control via visual inspection and basic checks; described as less strict than automated limits but incorporating human interpretation.
  - Data completeness varies by dataset and time period; some data are infrequently collected or partially missing due to equipment changes or field conditions.
- Data formats and accessibility:
  - Primary datasets listed with specific filenames (e.g., AWS daily data, Daily micromet data, Rainfall_Clocaenog.csv, Throughfall_Clocaenog.csv, etc.).
  - Some data are stored in CEH Bangor and not all within a centralized database (EIDC); contact points provided for access details.

## Datasets and major data streams (high-level)

- AWS meteorological data: daily meteorological variables (temperature, humidity, rainfall, radiation, wind, pressure).
- Micro-meteorological plot data: soil/air temperature and soil moisture at multiple depths.
- Rainfall and rainfall chemistry: site rainfall and chemical constituents (pH, NO3, Cl, SO4, DOC, NH4) from biweekly sampling.
- Throughfall data: plot-level rainfall measurements used to infer treatment-specific rainfall adjustments.
- Water table depth: depth measurements from perforated tubes (2009 onward).
- Soil respiration: soil CO2 efflux measurements using various chambers and systems; both fortnightly and automated campaigns.
- Trace gases (CH4 and N2O): flux estimates using static chambers and gas analysis.
- Net ecosystem CO2 exchange (NEE): flux measurements, biomass adjustments based on plant material inside chambers.
- Photosynthesis: ambient photosynthesis measurements and response curves (A/Ci and light response) for dominant species.
- Vegetation survey data (Pin-point biomass): multi-year biomass estimates across species via pin-hit method and biomass calibration.
- Canopy reflectance: NDVI and PRI derived from ground-based spectrometry.
- Vegetation phenology, annual growth and pathogen assessment: budburst, shoot elongation, flowering, leaf counts, and pathogen observations.
- Vegetation chemistry: carbon, nitrogen, phosphorus, potassium, calcium, magnesium, lignin, tannin, alpha-cellulose, carbohydrates (green and senesced material).
- Litterfall: annual litter production via collectors; subsequent carbon and nitrogen analyses.
- Root biomass: root mass estimates from soil cores across multiple years and methods.
- Soil microbial biomass: chloroform fumigation–extraction method.
- Nitrogen mineralisation: ammonium and nitrate production rates from buried cores.
- SOM, SOC and bulk density: carbon and density measurements from soil cores.
- Soil solution and leachate chemistry: lysimeters and tensioned samplers for DOC and nutrient analyses.

## Data access, governance and stewardship

- Access and contact points: Some data reside in CEH Bangor or the Ever-increasing Data Repository; for details, contact Sabine Reinsch or Bridget Emmett at CEH Bangor.
- Documentation: Supporting RTFs and site reports accompany many datasets; ongoing data governance and provenance are described, though some legacy data processing steps are not fully documented.
- Data sharing considerations: The site collects extensive environmental data intended to inform policy-relevant monitoring; however, some datasets may have access or metadata limitations, and some data are not fully Open Data due to legacy practices or storage arrangements.

## Key challenges and considerations for monitoring frameworks

- Data availability and completeness:
  - Gaps due to equipment changes, biweekly vs. daily cadence, and occasional data exclusions in throughfall and rainfall dispersion.
  - Legacy datasets may lack full metadata or processing details.
- Data accessibility and governance:
  - Some data not centrally stored or easily accessible; need to coordinate with CEH Bangor for access.
  - Public sharing of datasets is sometimes constrained by legacy data handling practices.
- Metadata and data quality:
  - Inadequate or evolving metadata across datasets; some QC is visual and manual rather than automated.
  - Calibration and unit conversion steps are documented but complex; ensure clear provenance and reproducibility.
- Data transformation and comparability:
  - Multiple measurement methods across time require careful harmonization (e.g., soil respiration instruments, canopy reflectance protocols).
  - Throughfall adjustments rely on multiple datasets and assumptions; methods are described but may introduce uncertainties.
- Communication of findings:
  - Rich, multi-disciplinary data require careful synthesis for policy evaluation; datasets include diverse ecological and biogeochemical indicators suitable for evaluating climate policy outcomes.

## Appendices and site layout

- Appendix: Site and plot layout, including grid references and plot designations.
- Appendix: Quadrat layout and vegetation sampling frameworks.
- Appendix: Plot layout with quadrats and measurement areas.

- Overall, the Climoor dataset collection provides a comprehensive, long-term, multi-disciplinary monitoring framework for assessing drought and warming treatments on upland moorland ecosystems, with numerous physically-grounded measurements, documented protocols, and explicit governance and accessibility considerations suitable for policy evaluation and future decision-making.