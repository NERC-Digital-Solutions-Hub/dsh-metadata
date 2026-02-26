# The effect of biochar addition on N2O and CO2 emissions from a sandy loam soil - the role of soil aeration

- Objective
  - Examine how adding biochar affects soil N2O and CO2 emissions and how soil aeration modulates these effects.

- Study system and materials
  - Soil source: Bare soil from a Miscanthus field in Lincolnshire, UK; dense, compacted sandy loam with 53% sand, 32% silt, 15% clay; low total C and N; recent PK fertiliser applied in 2010.
  - Biochar characteristics: Made from hardwood thinnings; produced by ring kiln (180 °C devolatilisation, then ~400 °C for 24 h); fresh biochar < 2 mm with GMC < 5%; bulk density 0.24 g cm-3; total C 723 g kg-1; total N 7.12 g kg-1; pH 9.25; CEC 145 cmol(+)/kg; minimal extractable NH4+/NO3-; supplementary data available for metals, PAHs, BETX.
  - Additional data: Moderately detailed chemical/physical properties and analytical methods provided; metal contents measured by ICP-OES; PAHs by GC-MS; BETX by HS-GC-MS.

- Experimental design overview
  - Experiment 1: Wetting/drying cycles
    - Full factorial style with four replicates (n = 4) at three temperatures (4, 10, 16 °C) and two soil moisture levels (field moist ~23% GMC, wetted ~28% GMC).
    - Biochar treatment: half of the cores received biochar added to the top 7 cm at 2% dry soil weight (~22 t ha-1); control cores without biochar.
    - Setup: soil cores (depth ~150–180 mm) placed in PVC tubes, incubated with maintained moisture, and subjected to wetting events.
    - Gas sampling: unvented static enclosure method; sampling at 6, 26, 51, 64, and 127 days; additional sampling within 72 hours after wetting events.
  - Experiment 2: Uniform water holding capacity incubations
    - Soil (0–10 cm) collected and incubated at 16 °C; biochar added at 0, 1, 2, 5, 10% of total dry soil weight (n = 4 per level).
    - Pre-incubation: 3 days to equilibrate after mixing and warming.
    - Water status: soil adjusted to 87% WHC to mimic wetting impact observed in pilot tests.
    - Gas sampling: headspace sampling at 0, 12, 24, 36, 48, 60, and 168 hours after wetting.
  - Measurements emphasized: N2O and CO2 fluxes; impact of biochar and moisture/aeration conditions on gas production.

- Analytical methods
  - Chemical analyses
    - pH by deionised water extraction (1:2.5 soil:water); NH4+ and NO3- by 2 M KCl extraction; analyses via discrete colorimetric procedures.
    - Total carbon and nitrogen by dry combustion (LECO Truspec) after drying; bulk density measurements.
  - Gas analytics
    - CO2: GC with two flame ionization detectors (FIDs) at configured temperatures.
    - N2O: GC with electron capture detector (ECD) at 360 °C.
    - Columns: Porapak Q 50–80 mesh; calibration with certified standards.
    - Data processing: cumulative gas production calculated from time-series concentrations; fluxes derived from headspace measurements.
  - Data handling and timing
    - Initial equilibration period implemented to account for respiration flush after mixing.
    - Descriptive timing aligned with wetting events and cumulative gas calculations.

- Data analysis and statistics
  - Software: R (version 2.14.0).
  - Data transformation: log10(gas flux + 1) to improve normality where appropriate.
  - Experiment 1: linear mixed-effects models for gas fluxes; three-way ANOVA on cumulative flux within 48 hours after wetting and on selected chemical properties.
  - Experiment 2: one-way ANOVA across biochar amendment levels for cumulative N2O/CO2 production at 60 hours post-wetting, plus related soil chemical properties (NH4+, NO3-, pH, total C, total N, WHC); post hoc comparisons with Tukey's HSD.
  - Model validation and references follow established ecological statistics guidelines.

- Key considerations and approach to interpretation
  - rationale for dual experiments: to capture both dynamic wetting/drying responses (Experiment 1) and controlled water-holding scenarios (Experiment 2) to disentangle biochar effects from moisture/aeration dynamics.
  - Acknowledgement of initial emission flushes and the need for equilibration before measurements.
  - Emphasis on robust analytical methods and clear data processing to support comparisons across treatments and conditions.

- Notes on limitations and scope
  - Results are not shown in the provided text; interpretations depend on the statistical outputs and observed gas flux patterns across treatments.
  - Biochar properties and soil context are specific to the Lincolnshire Miscanthus soil system, which may influence generalizability to other soils or climates.