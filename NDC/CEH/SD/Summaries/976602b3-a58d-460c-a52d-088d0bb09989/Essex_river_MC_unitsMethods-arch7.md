# Overall sampling design

- All measurements are paired within a column; at each site, 5 sediment cores (diameter 8 cm) were taken within a 25 m river reach.
- From each core, 4 sub-cores (diameter 2 cm) were taken to pair measurements; sub-cores stored according to the analysis performed.
- Sampling aimed to test how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology.

## Identifying information

- date: date of measurement; date definition = Month-Year.
- site.name: short site name; encoding: first letter = underlying geology (C=chalk, A=clay, G=greensand); river code examples provided (e.g., CE1 = River Ebble, GA2 = River Avon, GN1 = River Nadder, CW2 = River Wylye, AS1/AS2 = River Sem).
- site.name coordinates: latitude and longitude for each site.
- geology: sub-catchment underlying geology type (Clay, Chalk, Greensand).

## Genes

- 16s rRNA gene bacteria; unit = genes g-1 sedimentDW; methodology = DNA extracted from 0.25 g wet sediment (PowerSoil kit); qPCR with SensiFAST; absolute quantification against calibration curve (10^2 to 10^6 copies); standard negative controls.
- aoa (ammonia-oxidising archaea), aob (ammonia-oxidising bacteria), nirs (nirS), nirk (nirK), mcra (mcrA), pmoa (pmoA); each with gene-specific primers and same extraction/qPCR approach.
- All gene abundances are reported as genes g-1 sedimentDW.

## Carbohydrates

- colloidal.cho: µg g-1 sedimentDW; method = collect sub-core, extract colloidal CHO, quantify via phenol-sulphuric acid; extract also used for DOC, EPS30, EPS70.
- hw.cho: µg g-1 sedimentDW; hot-water extraction at 100°C for 1 h.
- eps.30: µg g-1 sedimentDW; EPS extracted from colloidal CHO fraction using 30% EtOH.
- eps.70: µg g-1 sedimentDW; EPS extracted from colloidal CHO fraction using 70% EtOH.
- All CHO/EPS measurements calibrated against glucose standards; units standardized to g-1 sedimentDW.

## Carbon

- DOC (dissolved organic carbon): mg DOC g-1 sedimentDW; extracted from colloidal CHO fraction; measured with Shimadzu TOC-V against a 5-point calibration (0–1000 mg/L) using potassium hydrogen phthalate standards.
- TC (total carbon): mg TC g-1 sedimentDW; measured by combusting dried sediment at 900°C; calibration with TOC standards.
- TOC (total organic carbon): mg TOC g-1 sedimentDW; pre-treatment with acid (2 M HCl) to remove inorganic carbon; measured on Shimadzu TOC-V with 5-point calibration.
- This suite captures both inorganic and organic carbon fractions in sediments.

## Particle size

- Colloid.pc, clay.pc, silt.pc, v.f.sand.pc, f.sand.pc, m.sand.pc, c.sand.pc, v.c.sand.pc, v.f.gravel.pc, f.gravel.pc, m.gravel.pc, c.gravel.pc, v.c.gravel.pc, cobble.pc, boulder.pc; units = %.
- Method: carbon analysis cores also used for particle-size analysis; samples sieved at 0.850 µm, particles weighed, imaged (200x), and analyzed (ImageJ); a minimum of about 6,000 particles counted for size classification where specified.
- Particle-size fractions reported as percentages of total sediment.

## Methane

- Mop (methane oxidation potential): pmol g-1 sedimentDW; method = 3 g sediment in serum bottle with 9-day incubation and 500 ppm methane headspace; methane quantified by GC-FID.
- mpp.h2, mpp.n2: methane production potential with headspaces of 80% H2/20% CO2 and 80% N2/20% CO2, respectively; unit = pmol g-1 sedimentDW; identical incubation and GC-FID analysis as Mop.

## Anions and cations

- River-water measurements (upstream samples): acetate, fluoride, formate, nitrate, nitrite, phosphate, sulphate, ammonium, calcium, magnesium, potassium, sodium; units = µmol L-1.
- Sediment-related measurements: acetate.sed, fluoride.sed, formate.sed, nitrate.sed, nitrite.sed, phos.sed, sulphate.sed, ammonium.sed, calcium.sed, magnesium.sed, potassium.sed, sodium.sed; units = µmol g-1 DW sediment.
- River-water analyses: Dionex ICS3000 with AS18 column; KOH/MilliQ eluents; 7-point calibration (0–200 µmol L-1); samples filtered (0.2 µm) and frozen; upstream collection prior to destructive sediment sampling.
- Sediment analyses: same evaluative framework adapted for solid-phase concentrations.

## Methodology

- The document provides protocols and instrumentation across measurement areas, including:
  - Genetics: PowerSoil DNA isolation kit, qPCR with SensiFAST, BioRad CFX96; primers for bacterial 16S and functional genes.
  - Carbohydrates: colloidal and extractable CHO via water/ethanol-based extractions; phenol-sulphuric acid quantification; EPS procedures aligned with standard references.
  - Carbon: TOC analyzer (Shimadzu TOC-V); inorganic carbon removal with acid; calibration curves.
  - Particle size: ecological sieving and image-based particle measurement with ImageJ; large particle counts.
  - Methane: incubation-based assays with GC-FID for Mop, mpp.h2, mpp.n2.
  - Anions/cations: Dionex ICS3000 chromatography for river water and sediment extracts.
- The methodology section consolidates the laboratory steps that underpin the dataset’s measurements.