# The effect of biochar addition on N2O and CO2 emissions from a sandy loam soil - the role of soil aeration

## Overview
- Investigates how biochar amendments influence N2O and CO2 emissions from a sandy loam soil, focusing on soil aeration effects.
- Two experiments: Experiment 1 examines wetting/drying cycles under varying temperatures and moisture; Experiment 2 examines biochar dose effects under uniform water holding capacity.
- Data collected include gas flux measurements, soil chemical properties, and biochar characteristics to assess treatment impacts and interaction effects.

## Materials: soil and biochar
- Soil source: Bare soil from a Miscanthus field in Lincolnshire, UK; sandy loam (53% sand, 32% silt, 15% clay); bulk density ~1.68 g/cm3; low total C (14.7 g/kg) and total N (2.70 g/kg); low inorganic N (NH4+-N and NO3--N).
- Biochar: Produced from hardwood thinnings (oak, cherry, ash); manufactured by ring kiln (180 °C release of volatiles, then ~400 °C for 24 h).
  - Properties: <2 mm particle size, GMC <5%, bulk density 0.24 g/cm3, C content ~723 g/kg, N content ~7.12 g/kg, pH ~9.25, CEC ~145 cmol+/kg.
  - Additional properties provided in supplementary info (exchangeable cations, heavy metals, PAHs, BETX).

## Experimental design

### Experiment 1: Wetting/drying cycles
- Fully factorial design with n = 4 cores per treatment.
- Factors: 3 temperatures (4, 10, 16 °C) and 2 moisture conditions (field moist ~23% GMC; wetted ~28% GMC).
- Biochar application: 2% biochar by dry soil weight in half of the cores; controls without biochar.
- Setup: Cores collected March 2010, incubated, and gas samples collected at days 6, 26, 51, 64, 127; wetting events occurred after days 51, 72, 86 with ~120 ml water to reach 28% GMC.
- Headspace gas sampling via unvented static enclosure method.

### Experiment 2: Uniform water holding capacity
- Soil 0–10 cm depth collected Oct 2010; stored at 4 °C for 8 weeks.
- Biochar treatments: 0, 1, 2, 5, 10% of total dry soil weight (n = 4 per level).
- Incubation: 16 °C in the dark for 3 days post-equilibration.
- WHC determination and wetting: wet to 87% WHC (WFPS ~78%).
- Gas sampling: 0, 12, 24, 36, 48, 60, 168 hours after wetting; bottles sealed with headspace sampling.

## Measurements and analyses

### Gas analysis
- CO2: Measured with GC-FID system (two detectors, temps 130 °C and 300 °C); calibration with standards.
- N2O: Measured with GC-ECD at 360 °C; calibration with standards.
- Flux calculations:
  - Experiment 1: cumulative gas production per area derived from linear gas concentration accumulation over 0–48 h after wetting.
  - Experiment 2: cumulative production from headspace concentration differences (t0 to sampling time).

### Chemical and physical analyses
- Soil pH (1:2.5 soil:water), extractable NH4+ and NO3- (KCl extraction), total C and N (CN analyzer after drying).
- Bulk density measured for each biochar treatment; WHC and WFPS estimated as in methods.
- Sampling focused on top 5 cm for chemical analyses.

### Statistical analysis
- Software: R (version 2.14.0).
- Data transformation: log10(gas flux + offset) to normalize distributions.
- Experiment 1: Linear mixed-effects models for gas fluxes; three-way ANOVA for cumulative gas flux within 48 h of wetting and for chemical properties.
- Experiment 2: One-way ANOVA across biochar levels; Tukey HSD for pairwise comparisons.
- References cited for methods and analysis approaches.

## Data characteristics and GIS relevance

- Spatial and temporal dimensions
  - Field coordinates provided for soil source (latitude 53.315580, longitude -0.596335).
  - Time-resolved measurements: multiple gas flux time points across weeks (Experiment 1) and hours (Experiment 2).
  - Treatments include multiple biochar doses, temperature regimes, and moisture conditions, enabling scenario analysis.

- Variables and measurements relevant for mapping
  - Gas fluxes: N2O and CO2 fluxes (temporal series, per core/bottle and per treatment).
  - Soil properties: pH, extractable NH4+/NO3-, total C and N, bulk density, WHC, WFPS.
  - Biochar properties: dose, physical-chemical characteristics (pH, CEC, C/N ratio).

- Potential GIS outputs
  - Spatio-temporal maps of gas flux responses to biochar dose across temperature/moisture scenarios.
  - Layered visuals combining flux data with soil chemical properties to identify hotspots and interactions.
  - Data fusion opportunities: link experimental results with field-scale soil maps and management practices to extrapolate potential field outcomes.

- Data integration considerations
  - The study combines laboratory core data with field soil provenance; harmonization needed for scaling to field or landscape levels.
  - Handling of multiple data sources (gas flux measurements, soil chemistry, biochar characteristics) requires careful metadata documentation and consistent units.

## Endnotes and context
- The research supports understanding how soil aeration and biochar amendments influence greenhouse gas emissions, with implications for data-driven, map-based communication of soil–biochar dynamics to policy makers, clients, and the public.