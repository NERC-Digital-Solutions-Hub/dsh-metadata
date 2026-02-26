# Overall sampling design

- Objective: Assess how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology.
- Design: All measurements are paired within a column. At each site, 9 soil samples were collected along a 40 x 40 m transect at 20 m intervals.
- Sub-sampling: From these samples, subsamples were stored differently depending on the subsequent analysis.
- Scope: Data address hypotheses about seasonal and geological influences on microbial processes.

## Identifying information

- Time and location: Year and Month of measurement; Month-Year for date; site.name as a short site identifier; underlying geology indicated in site.name (C=chalk, A=clay, G=greensand) and river-related codes (e.g., GA2 = River Avon, CW2 = River Wylye, AS2 = River Sem) with approximate coordinates.
- Geology: geology field captures sub-catchment geology type (Clay, chalk, greensand).

## Carbon

- TOC (Total Organic Carbon): Unit is mg TOC per g soil dry weight.
- Method: Soil dried at 60°C, homogenised; inorganic carbon removed with 2 M HCl; samples dried; TOC measured at 900°C using Shimadzu TOC-V with solid sample module.

## Anions and cations

- Analytes (examples): acetate, fluoride, formate, nitrate, nitrite, phosphate (phos), sulphate, ammonium, calcium, magnesium, potassium, sodium.
- Unit: µmol L-1 for dissolved species.
- Methodology: Dissolved anions and cations measured with a Dionex ion analyser using 0.2 µm filtered and frozen-stored water samples; 7-point calibration curves (0–200 µmol L-1).
- Sampling notes: Water collected from upper reach before destructive sediment sampling.

## Genes

- Targets and units: 16S rRNA gene (genes g-1 soil dry weight); amoA (AOA and AOB), nirS, nirK, pmoA, mcrA (all in genes g-1 soil dry weight).
- Methodology: DNA extracted from 0.25 g wet weight sediment using PowerSoil DNA Isolation Kit; qPCR with SensiFAST SYBR Kit on a BioRad CFX96; absolute quantification against DNA standards (10^2 to 10^6 copies); negative controls included.
- Primers: Provided for each target (e.g., 341F/805R for 16S; amoA AOA and AOB primers; nirS/nirK; pmoA; mcrA).

## Methane

- MOP (Methane oxidation potential): Unit is pmol g-1 soil dry weight.
  - Method: 3 g sediment incubated for 9 days with headspace of CH4; methane measured by GC-FID.
- MPP H (Methane production potential with H2/CO2 headspace): Unit is pmol g-1 soil dry weight.
  - Method: 3 g sediment incubated for 9 days with headspace of 80% H2/20% CO2; methane measured by GC-FID.
- MPP N (Methane production potential with N2/CO2 headspace): Unit is pmol g-1 soil dry weight.
  - Method: 3 g sediment incubated for 9 days with headspace of 80% N2/20% CO2; methane measured by GC-FID.
- Instrumentation: GC-2014 with FID; detailed column, temperatures, carrier gas, and flow parameters specified.

## Data governance and quality notes

- Data provenance: Documentation includes measurement methods, calibration ranges, and exact instruments used (e.g., Dionex ion analyser, Shimadzu TOC-V, qPCR with specified primers, GC-FID setups).
- Data handling: Samples filtered (0.2 µm), stored frozen where applicable; some analyses involve sub-sampling and varying storage/handling depending on analysis type.
- Metadata richness: Includes measurement definitions, units, methodologies, and primer sequences to enable reproducibility.
- Data sharing readiness: Describes pathways for uploading to portals and cataloguing datasets; clear documentation of work performed on datasets is advised to support reuse.

## Data stewardship considerations

- Completeness and standardization: Numerous fields are defined with consistent units and method details, but integration with other systems may require harmonization of site naming, geolocation, and geology coding.
- Access and updates: Procedures to update datasets and respect sharing limitations should be in place; dataset maintenance may involve updating measurement methods or calibration standards over time.
- Interoperability challenges: Multiple systems/formats (geochemical, molecular, and gas measurements) may require careful data mapping and schema alignment for cross-dataset analyses.
- User needs and usability: Rich metadata supports discoverability and usability for data creators, data users, and governance teams, aligning with the goal of datasets being discoverable and usable by others.