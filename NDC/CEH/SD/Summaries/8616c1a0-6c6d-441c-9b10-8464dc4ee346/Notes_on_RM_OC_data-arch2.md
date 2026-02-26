# Sediment collection

- Study design and sampling
  - Sediment trapping using Technicap PPS 4/3 sequencing traps at Rostherne Mere from May 2010 to September 2016; deployed at 10 m and 25 m water depths.
  - Each trap fed into 12 individual 250 ml HDPE bottles, representing 2-week collection periods (January–February allowed 4-week periods); traps reset every 6 months.
  - Trap sediment stored cool, dark, sealed during transport and frozen prior to analysis.
  - A 112 cm sediment core was collected at 26 m depth in September 2011 using a Livingstone piston corer; stored vertically and sectioned at 1 cm intervals for the upper 50 cm and 0.5 cm intervals thereafter.

- Sediment processing and analysis
  - Samples freeze-dried; organic matter (OM) determined by loss-on-ignition (LOI) at 550°C for 3 hours.
  - Organic carbon (OC) calculated from %LOI using a lake-specific factor of 0.56 (OC = LOI × 0.56), with calibration based on mass-spectrometry OC measurements.
  - d13C isotopic composition measured by mass spectrometry; calibration results provided for two soil samples (e.g., BROC2, SOIL B) to support OC/OC ratios.
  - Core samples analyzed for 210Pb activity by alpha spectrometry to establish chronology via the CRS (constant rate of supply) model; dating intervals include error analysis from counting uncertainty.

- Recorded data and units
  - Datasets include: water content, LOI, calcium carbonate (CaCO3), minerogenic fraction, sedimentation rates, and fluxes.
  - Sedimentation flux outputs: organic matter, organic carbon, CaCO3, and minerogenic fluxes expressed as g m^-2 d^-1 (traps) and g m^-2 yr^-1 (core).
  - Focused organic carbon burial rate (g C m^-2 yr^-1) with corrections applied.

- Data structure and contents
  - Three CSV files:
    - RMLOItoTOC: 9 columns (SampleNo, d13C, C, N, C/N, Trap/core, Depth, LOI, C/LOI).
    - RMSedCore2011LOI: 7 columns (AverageDepth_cm, Water, Calcium_Carbonate, LOI, EstimatedDate_AD, SedimentationRate_gcm2yr-1, FocusingCorrectedOrganicCarbon_gm2yr-1).
    - RMTrapSed: 14 columns (SampleCode, DateIn, DateOut, ShallowTrap/DeepTrap, CaCO3, LossOnIgnition, MinerogenicFraction, DaysCollecting, TotalSampleDryWeight_g, TrapArea_m2, FluxOrganicMatter_gm2d-1, FluxOrganicCarbon_gm2d-1, FluxCaCO3_gm2d-1, MinerogenicFlux_gm2d-1).
  - Units and values include: LOI (%), CaCO3 (%), OM (%), C (%), N (%), C/N, Depth (cm or trap depth), Dates, trap area (m2), fluxes (g m^-2 d^-1 or g m^-2 yr^-1).

- Provenance and references
  - Methods and calibration references: Appleby (2001) for CRS chronostratigraphy; Dean (1974) for LOI carbon/organic matter; Wright (1967) piston sampler design.
  - Data interpretation relies on a lake-specific OC conversion and established isotope and dating protocols.

- Relevance for environmental monitoring
  - Provides standardized, QA-checked sediment records enabling temporal assessment of environmental health and policy performance.
  - Datasets are structured for integration with other monitoring data; underlying raw measurements (d13C, OC/OC ratios, LOI, CaCO3, minerogenic content) support broader analyses.
  - Outputs include both descriptive metrics (rates, concentrations) and derived fluxes/burial rates, suitable for trend analysis and policy evaluation.

- Opportunities and challenges for analysts
  - Facilitates data value enhancement through integration with complementary datasets (e.g., other lakes, regional datasets).
  - Emphasizes accessibility of underlying data for reuse and scrutiny, aligning with standardized monitoring practices.