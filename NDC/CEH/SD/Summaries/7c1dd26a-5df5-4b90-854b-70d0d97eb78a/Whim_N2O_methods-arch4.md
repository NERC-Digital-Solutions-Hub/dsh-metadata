# Nitrous oxide emissions from a peatbog after thirteen years of experimental nitrogen deposition - Materials and methods

- Overview
  - Long-term field experiment at Whim bog, Scottish Borders, examining responses to nitrogen deposition on a transition between lowland raised bog and blanket bog.
  - Site characteristics: deep peat (3–6 m), acidic soil (pH ~3.4), wet hollows, variable vegetation with Calluna vulgaris and Sphagnum species.
  - Treatments implemented from 2002: 
    - Dry deposition: NH3 fumigation over downwind sector using a free-air release system.
    - Wet deposition: increasing NH4+ and NO3− via sprinkler system to replicated plots.
  - Experimental design includes four blocks and 28 plots, with target total N deposition rates of 8 (control), 16, 32, and 64 kg N ha−1 y−1.

- Data assets and structure
  - ancilliaryData-byChamber.csv: per-chamber metadata including chamberID, chamberCode, experimental grid (Wet/Dry/Ozone), block/plot IDs, location (lon/lat), and fluxes (Fnh3, Fnh4, Fno3, Ndep-total).
  - ancilliaryData-byChamber-byDate.csv: chamber/date-specific metadata and measurements, including gasName (N2O), date, coordinates, deposition fluxes, and environmental variables.
  - RCfluxOutput.csv: flux estimates for N2O produced by multiple models (linear, quadratic, asymptotic, HMR, best-fit) with confidence intervals and model fit metrics.
  - vegetation-speciesPercentCover-Whim-byChamber.csv: percent cover data for each plant species by chamber (e.g., Calluna vulgaris) and related monthly ammonium metrics.
  - chemistry-NH4mgNperl-Whim-byChamber-byDate.csv: soil water ammonium concentrations by chamber and date.
  - chemistry-NO3mgNperl-Whim-byChamber-byDate.csv: soil water nitrate concentrations by chamber and date.
  - chemistry-pH-Whim-byChamber-byDate.csv: soil water pH by chamber and date.
  - Table/figure references (e.g., Figure 1: Layout of N deposition plots) provide context for spatial arrangement.

- Data collection and measurement methods
  - Field site data:
    - Soil and climate context recorded (air/soil temperatures, rainfall, water table depth).
    - Vegetation cover documented by chamber.
  - Gas flux measurements:
    - Nitrous oxide fluxes measured with the static chamber method (collars inserted into peat; lids sealed for 30–40 minutes; four gas samples collected per chamber).
    - Measurements typically conducted monthly.
  - Deposition and chemistry measurements:
    - Dry NH3 deposition estimated using passive samplers and a calibrated deposition-velocity method.
    - Wet deposition delivered via sprinkler system with controlled concentrations of NH4Cl or NaNO3; pattern designed for high-frequency, extensive deposition (~120 applications y−1).
    - Soil solution analyses (NH4+, NO3−) by ion chromatography; detection limits specified.
    - Soil pH and vegetation metrics collected periodically.

- Data processing and analysis
  - Gas flux calculation:
    - F = (dC/dt0) × (ρ × V) / A, where dC/dt0 is the initial rate of concentration change derived from time-series concentrations using linear or non-linear asymptotic regression.
    - Time resolution (~10 minutes) limits detectability of non-linearity; potential flux underestimation acknowledged.
  - Calibration and quality control:
    - Gas samples analyzed by gas chromatography with four standard gases spanning relevant mole fractions.
    - Four-point calibration for converting to mole fractions; standards run roughly every 20 samples.
  - Statistical analysis:
    - Linear mixed-effects model used to relate N2O flux to soil temperature, water table depth, and deposition fluxes (NH3, NH4+, NO3−).
    - Random effects account for repeated measures at chamber locations nested within blocks.
    - Data set includes 729 flux measurements after outlier removal (four high outliers >10 nmol m−2 s−1 and two <−2 nmol m−2 s−1 removed).

- Quality, limitations, and governance implications
  - Methodological notes emphasize uncertainty quantification in flux measurements (cited references on flux calculation methods and uncertainty assessment).
  - Data are richly annotated with per-chamber and per-date metadata, facilitating cross-study comparability and re-use within data networks.
  - The multi-file structure (per-chamber, per-date, model outputs, chemistry, and vegetation data) supports integrated analyses but requires careful adherence to metadata definitions (e.g., units, IDs, and descriptions) to ensure discoverability and interoperability.
  - Potential use cases for Data Leaders:
    - Integrating these data with other long-term N deposition datasets to benchmark soil–atmosphere N2O flux responses.
    - Developing standards for metadata and file naming conventions to enhance cross-project discoverability and re-use.
    - Assessing data gaps (e.g., granularity of deposition rates, spatial coverage, and date resolution) to guide future data collection and collaboration across networks.