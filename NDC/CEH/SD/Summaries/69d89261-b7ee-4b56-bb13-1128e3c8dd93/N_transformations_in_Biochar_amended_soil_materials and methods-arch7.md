# Chemical analysis of nitrogen transformations in Biochar amended soil - materials and methods

- This document describes field and laboratory methods to study how biochar affects nitrogen transformations and N2O emissions in arable soil using two factorial experiments and isotopic tracing.

## Field site and biochar description

- Field site: near Lincoln, Lincolnshire.
- Soil: sandy loam (57% sand, 32% silt, 10% clay); bulk density 1.39 g cm-3.
- Cropping history: three-year wheat rotation followed by one year of oilseed rape; total N input 140 kg N ha-1 yr-1 as NH4+ / NO3-.
- Biochar: slow-pyrolysis, hardwood feedstock (ash, oak, cherry); produced by heating to 180 °C to release volatiles, then to 400 °C for 24 h.
- Biochar characteristics: C 72.3%, N 0.71%, low extractable inorganic-N, pH 9.25, gravimetric moisture content 3.1%.

## Experimental design

- Two separate factorial experiments:
  - Experiment 1: Effects of biochar on N2O emissions under different aeration status.
    - Factors: biochar amendment (yes/no) and water status (un-wetted vs wetted).
    - 5 replicates per treatment; 20 soil cores total.
    - Biochar rate: 3% soil dry weight (~22 t ha-1).
    - Cores prepared to 7 cm depth; incubated at 16 °C in the dark.
  - Experiment 2: Biochar effects on soil N transformations using 15N pool dilution.
    - Four-treatment factorial with 15N labeling; biochar at 2% soil dry weight.
    - 100 g dry soil per container; 80 containers (1.7 L each) prepared to 1 cm depth.
    - Conditions set to 90% WFPS (wetting to optimize N2O emissions).
- Wetting regime and sampling schedule designed to capture N2O dynamics and N transformations over time.

## Sample collection and preparation

- Core collection for Experiment 1:
  - 20 cores; depth 150–180 mm; each core ~1.6 kg dry-weight soil.
  - Stored at 4 °C for 30 days before experimentation.
- Core preparation and treatments:
  - Half of cores received biochar (< 2 mm) mixed at 3% soil dw.
  - After a 7-day stabilization to account for CO2 flush, cores placed at 16 °C in the dark.
  - Wetting: un-wetted (23% GMC) and wetted to 28% GMC with four wetting events on days 17, 46, 67, and 116.
- Experiment 2 container setup:
  - 100 g soil per container; 7 days dark acclimation at 16 °C prior to 15N addition.
  - 15N additions to achieve 90% WFPS with 10 atom% 15N enrichment.
  - Five time points for destructive sampling (for C/N, pH, GMC, BD, inorganic and organic N pools).

## Measurements and analyses

- Soil properties (extractable inorganic N and total C/N):
  - Inorganic NH4+ and NO3- extraction with 5 g soil + 50 mL 0.8 M KCl.
  - Analyzed with a colorimetric analyzer (Seal AQ2).
  - Total C and N via LECO CN analyzer.
  - Gravimetric moisture content, soil pH, particle density, and WFPS following standard methods.
- Headspace N2O analysis:
  - Gas samples analyzed by gas chromatography (GC) with calibration against certified standards.
  - Fluxes calculated from the linear increase in ppm over 0–60 minutes after enclosure.
  - Exclude samples if linearity criterion (r2 ≥ 0.8) is not met.
- N isotopic analyses:
  - Inorganic 15NH4+ and 15NO3- analyzed via acidified filter-disk method; organic 15N used as a proxy for microbial biomass.
  - Samples combusted and analyzed with an elemental analyzer coupled to an isotope ratio mass spectrometer (IRMS) for 15N composition.
  - 15N2O: headspace gas (80 mL) analyzed by IRMS after preparation in serum bottles; δ15N values derived via a trace gas precursor method.
  - 15N2: headspace samples (20 mL) processed through a preparation unit to remove CO2 and water, with N2 measured by IRMS.

## Analytical methods and instrumentation

- Inorganic-N analyses: 5 g soil + 50 mL 0.8 M KCl; colorimetric measurements (Seal AQ2).
- Total C and N: Truspec/LECO CN analyzer.
- pH, GMC, BD, and WFPS: standard soil methods.
- N2O and isotopic analyses:
  - N2O: GC (PerkinElmer) with calibration standards; fluxes from linear ppm increases (0–60 min).
  - 15N analyses: automated CN analyzer + IRMS; 15N in inorganic pools via acidified disks; organic 15N as microbial biomass proxy.
  - 15N2O and 15N2: IRMS-based measurements after vial incubation and gas preparation.

## Quality control and data handling

- Calibration against certified standards for GC and IRMS.
- Exclusion of non-linear N2O flux data (r2 < 0.8) to ensure accurate flux estimates.
- Use of established methods for soil N and C analyses, ensuring comparability with standard soil science protocols.

## GIS-ready data considerations and potential data products

- What can be mapped and analyzed:
  - Spatial distribution of N2O fluxes across cores and time points.
  - Isotopic enrichment patterns (15N) in inorganic pools and gaseous products (N2O, N2).
  - Soil properties (pH, GMC, BD, extractable NH4+/NO3-, total C/N) linked to sampling locations.
- Data requirements for GIS readiness:
  - Precise geolocation of each soil core and container (coords, depth, orientation).
  - Time-stamped measurements (dates of sampling, incubation status, and wetting events).
  - Consistent units and clear treatment labels (biochar presence, aeration/wetting status, 15N labeling).
- Potential GIS data products:
  - Time-series maps of N2O flux by treatment and site, with uncertainty estimates.
  - Spatial layers for soil chemical properties and isotopic fractions at defined depths.
  - Visualization of N transformation pathways by treatment (e.g., inorganic N pools vs. gaseous products).
- Relevance for GIS specialists:
  - Integrates field sampling design, laboratory measurements, and isotopic data into spatial analyses.
  - Highlights the need for metadata standards, data cleaning, and multi-resolution data integration.
  - Supports development of map-based data visualizations for policy colleagues, clients, or the public.