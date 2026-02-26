# Overall sampling design

- Purpose: Collect data to address hypotheses about how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology.
- Design overview: At each site, 5 sediment cores (8 cm internal diameter) were taken within a 25 m river reach; from each core, 4 sub-cores (2 cm diameter) were taken to create paired measurements. Sub-cores were stored according to analysis.
- Output aim: Generate data to analyze microbial gene abundances, carbon and nitrogen chemistry, viral/particle properties, and methane-related processes, enabling cross-site and seasonal comparisons.

## Identifying information and metadata

- date: Date of measurement; date field defined as Month-Year.
- site.name: Short site name with encoding; first letter indicates underlying geology (C=chalk, A=clay, G=greensand) and second letter indicates river name; a numeric suffix identifies the site (e.g., CE1, GA2, GN1, CW2, AS1, AS2).
- geography: Exact latitude and longitude provided for example sites (e.g., River Ebble, River Avon, River Nadder, River Wylye, River Sem and tributaries).
- geology: Sub-catchment underlying geology type (chalk, clay, greensand).

## Genes and molecular measurements

- 16s rRNA gene (16s): Abundance in genes per gram sediment dry weight; method includes DNA extraction from 0.25 g wet weight, qPCR using SensiFAST kit, and absolute quantification against a standard curve (10^2–10^6 copies).
- Ammonia-oxidizing archaea (aoa) and bacteria (aob): Gene abundances (genes g-1 sedimentDW) with specific primers and qPCR; internal calibration and negative controls included.
- Denitrification and nitrite reduction genes: nirS (nirs) and nirK (nirk) with gene abundance, primers, and qPCR methodology.
-Methanogenesis and methane oxidation markers: mcrA (mcra) for methanogens; pmoA for methane-oxidizing organisms; all with qPCR, internal standards, and calibration.
- General methodology: Use of PowerSoil DNA Isolation Kit; BioRad CFX96 qPCR; standard negative controls; primers referenced in original notes.

## Carbohydrates and extracellular components

- Colloidal carbohydrates (colloidal.CHO) and hot-water extracted carbohydrates (hw.cho): Quantified against glucose standard using phenol-sulphuric acid method; units in µg CHO g-1 sedimentDW.
- Extracellular polymeric substances (EPS30 and EPS70): Extracted from colloidal carbohydrate fraction with ethanol and quantified against a PSA assay; units in µg EPS per g sedimentDW.
- Sub-sample handling: Colloidal extract used for EPS measurements; calibration against glucose standards.

## Carbon fractions and related measurements

- Dissolved Organic Carbon (DOC): mg DOC per g sedimentDW; subsampled from the colloidal CHO fraction and measured with a Shimadzu TOC analyzer using a calibration curve.
- Total Carbon (TC) and Total Organic Carbon (TOC): mg TC g-1 sedimentDW and mg TOC g-1 sedimentDW, respectively; TOC measured after removal of inorganic carbon with 2 M HCl; calibration against TOC standards.

## Particle size and textural analysis

- Particle-size fractions (percentages by weight): Colloid, clay, silt, very fine sand, fine sand, medium sand, coarse sand, very coarse sand, very fine gravel, fine gravel, medium gravel, coarse gravel, very coarse gravel, cobble, and boulder.
- Method: Cores subjected to 0.850 µm sieve; retained vs passed particles weighed; images captured and analyzed (ImageJ) for particle size distribution; minimum 6000 particles counted per sample for gravel/stone fractions; percentages calculated for each size class.

## Methane-related measurements

- Methane oxidation potential (mop): pmol g-1 sedimentDW; incubation of 3 g sediment with CH4 headspace; GC-FID analysis over 9 days.
- Methane production potential with H2 (mpp.h2) or N2 (mpp.n2): pmol g-1 sedimentDW; incubations with 80% H2/20% CO2 or 80% N2/20% CO2 headspace; headspace sampled every 3 days; GC-FID analysis.
- Carrier gas, column, temperature and instrument details included for reproducibility.

## Anions and cations (water column)

- River water measurements (µmol L-1): Acetate, fluoride, formate, nitrate, nitrite, phosphate, sulphate, ammonium, calcium, magnesium, potassium, sodium.
- Instrumentation and processing: Dissolved ions measured with a Dionex ICS3000 ion chromatograph using AS18 column with KOH/MilliQ eluents; 7-point calibration from 0–200 µmol L-1; samples collected from the upper reach and filtered (0.2 µm) before storage.
- Sediment porewater measurements (µmol g-1 DWsediment): Acetate.sed, fluoride.sed, formate.sed, nitrate.sed, nitrite.sed, phosphate.sed, sulphate.sed, ammonium.sed, calcium.sed, magnesium.sed, potassium.sed, sodium.sed; same Dionex-based methodology adapted for sediment matrix (g-1 DW).
- Notes: Data include explicit sediment versus water column contexts; QA includes standard calibration and frozen storage.

## Data provenance, QA, and notes

- Quality controls: qPCR runs included standard negative controls; internal standard calibration curves used for gene targets; triplicate or multiple replicates indicated by methodology (e.g., 4 technical replicates for carbohydrate assays).
- Instrumentation: Detailed instrument models and settings provided (e.g., BioRad CFX96, Shimadzu TOC-V, GC-FID configurations) to enable reproducibility.
- Data structure: Measurements are paired within a column; multiple measurements per site and core/sub-core support cross-comparison across depth and time.
- Access and reuse: The dataset integrates microbial gene abundances with chemical and physical sediment parameters, enabling analysis of links between microbial communities and carbon/nitrogen cycling across geology types and seasons.