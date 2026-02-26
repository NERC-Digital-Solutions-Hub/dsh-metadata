# Overall sampling design

- Aims and approach
  - Measurements are paired within each column to study how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology.
- Sampling scheme
  - At each site, 9 soil samples were collected within a 40 × 40 m transect at 20 m intervals.
  - Sub-samples were taken and stored differently depending on the analysis to be performed.

## Identifying information (metadata)

- Time and site identifiers
  - Year and Month (date, month-year definitions provided)
- Site naming and geology
  - site.name encodes underlying geology and river: first letter = geology (C=chalk, A=clay, G=greensand); second letter = river initial; a River GA2 corresponds to River Avon, CW2 to River Wylye, AS2 to River Sem; a numeric suffix assigns the specific site.
- Geology and location
  - geology = sub-catchment underlying geology type (Clay, Chalk, Greensand)
  - Associated coordinates provided for rivers used in site coding

## Carbon

- TOC (Total Organic Carbon)
  - Measurement: mg TOC per g soil dry weight
  - Methodology: sub-core dried at 60°C, homogenised; inorganic carbon removed with 2 M HCl; samples dried; TOC measured at 900°C using Shimadzu TOC-V with solid sample module

## Anions and cations

- Measured species and units (all in µmol L-1)
  - acetate, fluoride, formate, nitrate, nitrite, phosphate, sulphate, ammonium, calcium, magnesium, potassium, sodium
- Methodology and sampling
  - Water samples collected from the upper reach before destructive sediment sampling; filtered (0.2 µm) and stored frozen
  - Anions and cations quantified using a Dionex ion analyser (ICS3000) with AS18 column; eluents KOH and MilliQ water
  - Calibration: 7-point curve from 0 to 200 µmol L-1

## Genes

- Target genes and measurement
  - 16S rRNA (bacteria)
  - amoA AOA (ammonia-oxidising archaea)
  - amoA AOB (ammonia-oxidising bacteria)
  - nirS, nirK (nitrite reductases)
  - pmoA (particulate methane monooxygenase, methanotrophs)
  - mcrA (methyl coenzyme M-reductase, methanogens)
- Units and methodology
  - Units: genes g-1 soil dry weight
  - DNA extraction from 0.25 g wet weight sediment (PowerSoil kit)
  - qPCR with SensiFAST SYBR No-ROX; absolute quantification against internal DNA standards (10^2 to 10^6 copies)
  - Primers specified for each gene set (with literature references)

## Methane

- Methane-related measurements and setups
  - MOP: Methane oxidation potential (pmol g-1 soil dry weight)
  - MPP H: Methane production potential under headspace of 80% H2 and 20% CO2
  - MPP N: Methane production potential under headspace of 80% N2 and 20% CO2
- Methodology
  - 3 g of sediment in a 120 mL serum bottle incubated for 9 days
  - Headspace sampled every 3 days; methane quantified by GC-FID
  - Instrumental details provided (carrier gas, temperatures, column, flow, etc.)

## Data handling and intent

- Data provenance and accessibility
  - Data sources are tracked; created datasets may be uploaded to portals with metadata to enhance discoverability and reusability
- Analytical workflow (implied)
  - Data quality assurance, cleaning, and transformation anticipated
  - Analyses likely include correlating seasonality and geology with gene abundances, carbon/nutrient metrics, and methane-related potentials