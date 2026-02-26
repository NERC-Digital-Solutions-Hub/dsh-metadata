# Overall sampling design

- Purpose: Address hypotheses about how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology.
- Design: At each site, 9 soil samples collected within a 40 x 40 m transect at 20 m intervals; sub-samples stored differently depending on analysis.
- Data structure: Measurements are paired within a column; data collected span carbon, inorganic ions, microbial genes, and methane-related activities to understand biogeochemical processes.

## Metadata, identifying information and location

- Time and site identifiers: Year, Month, and a short site name; Year-Month defined as Month-Year.
- Site encoding: site.name uses a two-letter geology plus river code scheme (e.g., C=chalk, A=clay, G=greensand; river initials in the second position; example GA2 = River Avon, CW2 = River Wylye, AS2 = River Sem).
- Geology information: geology field indicates sub-catchment underlying geology type (Clay, Chalk, Greensand).
- Location references: geographic coordinates provided for sites (e.g., GA2, CW2, AS2).
- Purpose of metadata: Enables identification, traceability, and linkage of measurements across analyses.

## Carbon measurements

- TOC (Total Organic Carbon): unit mg TOC per g soil dry weight.
- Sample preparation: sub-core dried at 60°C and homogenised; inorganic carbon removed by adding 2 M HCl; samples dried overnight.
- Measurement: TOC determined at 900°C using a Shimadzu TOC-V with solid sample module.

## Anions and cations

- Analytes (examples): acetate, fluoride, formate, nitrate, nitrite, phosphate, sulfate, ammonium, calcium, magnesium, potassium, sodium.
- Unit: µmol L-1 for dissolved species; general approach applies to all listed ions.
- Methodology: Dissolved ions analyzed with a Dionex ion chromatograph (ICS3000) using an AS18 column with KOH and MilliQ eluents; calibration with a 7-point curve from 0 to 200 µmol L-1.
- Sampling and processing: Water samples collected from the upper reach before destructive sediment sampling; filtered through 0.2 µm syringes and stored frozen.
- Notes: Each ion has a consistent description of collection, filtration, storage, and analysis to ensure comparability across samples.

## Genes and microbial markers

- Target genes and units: 
  - 16S rRNA gene (genes g-1 soil dry weight)
  - amoA (AOA and AOB), nirS, nirK, pmoA, mcrA (all in genes g-1 soil dry weight)
- DNA extraction: from 0.25 g wet weight sediment using PowerSoil DNA Isolation Kit.
- Quantification: qPCR with SensiFAST SYBR No-ROX; absolute quantification against internal DNA standards (10^2 to 10^6 copies).
- Quality controls: standard negative controls run for all qPCRs.
- Primers and references: detailed primer sequences and literature references provided for each gene.

## Methane measurements

- Methane oxidation potential (MOP): measured in pmol g-1 soil dry weight.
  - Method: 3 g soil in 120 mL bottle, 9-day incubation with 500 ppm CH4 headspace; sampling every 3 days; CH4 quantified by GC-FID.
- Methane production potential with H2 (MPP H) and with N2 (MPP N): both in pmol g-1 soil dry weight.
  - Headspace: either 80% H2 + 20% CO2 or 80% N2 + 20% CO2.
  - Method: identical incubation and sampling as MOP; CH4 quantified by GC-FID.
- Instrumentation and settings: GC-2014 with FID; specified column and temperature conditions; carrier gas, injection, and flow parameters detailed for reproducibility.

## Data quality and interoperability considerations

- Consistency: All measurements are paired within columns and follow consistent preparation and analysis protocols across replicates.
- Calibration and standards: Use of calibration curves for ions, internal DNA standards for qPCR, and methane standards for GC analyses.
- Traceability: Metadata fields (year, month, site, geology, coordinates) enable temporal and spatial linking of datasets across carbon, ionic, genetic, and methane measurements.
- Storage and handling notes: Samples are filtered and frozen where required; sub-samples stored differently depending on analysis, which should be tracked for traceability and reproducibility.
- Potential integration: Rich, multi-domain data facilitates linking soil chemistry, microbial gene abundance, and methane flux potential to study seasonal and geological effects on biogeochemical cycling.