# The effect of biochar addition on N2O and CO2 emissions from a sandy loam soil - the role of soil aeration

## Aim
- Evaluate how adding biochar influences soil N2O and CO2 emissions, with a focus on the role of soil aeration.
- Use standardized, repeatable methods to assess environmental health indicators over time.

## Biochar and soil characteristics
- Soil source: bare soil from a Miscanthus field in Lincolnshire, UK; sandy loam with 53% sand, 32% silt, 15% clay; bulk density ~1.68 g cm-3; low total soil carbon (14.7 g kg-1) and nitrogen (2.70 g kg-1).
- Biochar: produced from hardwood tree thinnings (oak, cherry, ash); particle size < 2 mm; GMC < 5%; bulk density ~0.24 g cm-3; C content ~723 g kg-1; N ~7.12 g kg-1; pH ~9.25; CEC ~145 cmol(+)/kg; NH4+/NO3− extractable-N below detection limits.
- Additional properties (exchangeable cations, heavy metals, PAHs, BETX) available in supplementary information.

## Experimental design

### Experiment 1: Soil cores undergoing wetting/drying cycles
- Fully-factorial setup (n = 4 per condition) at three temperatures (4, 10, 16 °C) and two moisture levels (field moist ~23% GMC and wetted ~28% GMC).
- Biochar treatment: half of the cores receive biochar mixed into the top 7 cm at 2% of dry soil weight (~22 t ha−1); control cores without biochar.
- Cores collected March 2010; stored at 4 °C for equilibration before measurements.
- Wetting events: additional wetting after 51, 72, and 86 days; approximately 120 mL water added per core to reach 28% GMC.
- Gas sampling: headspace samples at 6, 26, 51, 64, and 127 days; gaseous CO2 and N2O analyzed.

### Experiment 1: Chemical analyses
- Soil pH (1:2.5 soil:water), extractable NH4+ and NO3− (2 M KCl), total C and N (CN analyzer).
- Samples collected from top 5 cm; stored appropriately for later analysis.

### Experiment 2: Soil incubations at uniform water holding capacity
- Soil from Oct 2010 (0–10 cm) incubated in 125 mL serum bottles; biochar added at 0, 1, 2, 5, 10% of total dry soil weight (n = 4 per level).
- Incubation at 16 °C in dark; equilibration for 3 days after mixing.
- WHC determined; soils wetted to 87% WHC (WFPS ~78%).
- Gas sampling: headspace samples at 0, 12, 24, 36, 48, 60, and 168 hours after wetting.

### Experiment 2: Chemical analyses
- Post-incubation measurements: extractable NH4+, NO3−, pH; total C and N; bulk density.
- Field soil used as control for comparison.
- Methods aligned with Experiment 1.

## Headspace gas analysis
- CO2: analyzed by GC with two FID detectors ( temperatures 130 °C and 300 °C with methaniser); calibrated with certified standards.
- N2O: analyzed by GC with an electron capture detector at 360 °C; standard Porapak Q column.
- Flux calculations: experiment 1 via linear accumulation of concentrations over 0–60 minutes for each 6-day interval and cumulative flux within 48 hours after a wetting event; experiment 2 via change in sealed headspace from t0 to sampling time.

## Statistical analyses
- Data transformed with log10(gas flux + 1) for normality where appropriate.
- Experiment 1: linear mixed-effects models for gas fluxes; three-way ANOVA for cumulative flux within 48 hours after wetting and chemical properties.
- Experiment 2: one-way ANOVA with biochar level as factor; Tukey’s HSD for pairwise comparisons.
- Analyses conducted in R (version 2.14.0).

## Outputs and relevance for environmental monitoring
- Generates standardized measurements of N2O and CO2 fluxes under varying biochar amendments, temperatures, and soil moisture regimes.
- Provides datasets linking biochar application rates to greenhouse gas emissions and soil chemical properties.
- Methods align with established soil monitoring practices, enabling integration into environmental health and policy performance assessments.