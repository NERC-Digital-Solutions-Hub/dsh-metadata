# Sediment collection

- Scope and location
  - Sediment trapping at Rostherne Mere from May 2010 to September 2016 using Technicap PPS 4/3 automatic sequencing traps.
  - Traps deployed at 10 m (shallow) and 25 m (deep) water depth; 12 individual 250 ml bottles per trap representing 2-week collection periods (longer periods of up to 4 weeks in Jan–Feb).
  - Traps reset every 6 months; samples transported cold, dark, sealed, and stored frozen prior to analysis.
  - A sediment core (112 cm) collected at 26 m depth in Sept 2011; stored vertically in dark cold room and sectioned for analysis.

- Sampling design and handling
  - Traps: sequentially opened into bottles, with handling to preserve sediment integrity during transport.
  - Core: ends sealed; sectioning at 1 cm intervals for upper 50 cm, then 0.5 cm intervals thereafter.
  - All samples freeze-dried before analysis.

- Laboratory analysis and chronology
  - Organic matter (OM) determined by loss-on-ignition (LOI) at 550°C for 3 hours.
  - Organic carbon (OC) percentage calculated from %OM using lake-specific factor: OC = OM × 0.56.
  - Calibration relationships established for C and N using mass spectrometry and elemental analysis.
  - 210Pb activity measured by alpha spectrometry to establish chronology using the CRS (constant rate of supply) model; confidence intervals from counting uncertainty.

- Data units and recorded values
  - Recorded variables include water content (LOI), CaCO3, OC, C, N, C/N, C/LOI, and fraction of minerogenic material.
  - Sedimentation rates and fluxes provided in:
    - Traps: grams per square meter per day (g m^-2 d^-1) for organic matter, organic carbon, CaCO3, and minerogenic flux.
    - Core: grams per square meter per year (g m^-2 yr^-1) for related measures and focused organic carbon flux (g C m^-2 yr^-1).
  - Additional core data include AverageDepth, DateOf deposition (EstimatedDate), and SedimentationRate.

- Data structure and files
  - RMLOItoTOC: 9 columns (SampleNo, d13C, C, N, C/N, Trap/core, Depth, LOI, C/LOI).
  - RMSedCore2011LOI: 7 columns (AverageDepth cm, Water, Calcium_Carbonate, LOI, EstimatedDate AD, SedimentationRate, FocusingCorrectedOrganicCarbon).
  - RMTrapSed: 14 columns (SampleCode, DateIn, DateOut, ShallowTrap/DeepTrap, Calcium_Carbonate, LossOnIgnition, MinerogenicFraction, DaysCollecting, TotalSampleDryWeight, TrapArea, FluxOrganicMatter, FluxOrganicCarbon, FluxCaCO3, MinerogenicFlux).

- Calculations and derived metrics
  - Fluxes derived from LOI, OC, CaCO3, sedimentation rate, total collection duration, and trap area.
  - Organic carbon burial rates (FocussingCorrectedOrganicCarbon) calculated for core samples.
  - Age dating and accumulation rates derived from 210Pb CRS model with associated uncertainty.

- Calibration and references
  - Calibration results and conversion factors used for OC and isotopic interpretations are listed (e.g., d13C_cal, C_cal, N_cal, C/N_cal) with specific sample identifiers.
  - Key methodological references:
    - APPLEBY, P. G. 2001. Chronostratigraphic techniques in recent sediments.
    - DEAN, W. E. 1974. LOI method for OM and CaCO3.
    - WRIGHT, H. E. 1967. Piston sampler design for lake sediments.

- Relevance for GIS and data products
  - Spatial-temporal data enabling map-based visualization of sedimentation rates, organic carbon burial, mineral fluxes, and CaCO3 deposition across shallow (10 m) and deep (25 m) trap locations and core depths.
  - Suitable for creating layers representing:
    - Trapping locations with associated fluxes and age estimates.
    - Core-derived deposition rates by depth and date.
    - Temporal trends in OM, OC, and CaCO3 at Rostherne Mere.
  - Valuable for policy, client, or public-facing GIS visualizations of lake sediment dynamics and carbon budgeting at high spatial and temporal resolution.

- Data quality and provenance notes
  - Blank fields indicate samples not analysed.
  - Handling and storage conditions (freeze-drying, cold storage) noted to ensure data integrity.
  - Provenance includes clear methodological citations and calibration data supporting the recorded values and derived fluxes.