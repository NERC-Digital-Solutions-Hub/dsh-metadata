# Overall sampling design

- Purpose: To examine how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with underlying geology, using paired measurements from sediment samples collected in river reaches.
- Sampling scheme: All measurements are paired within a column. At each site, 5 sediment cores (8 cm internal diameter) were collected within a 25 m river reach; from each core, 4 sub-cores (2 cm internal diameter) were taken to pair measurements.
- Data focus: Designed to address hypotheses about seasonal variation and geologic influence on microbial-mediated carbon and nitrogen processes.

## Identifying information

- date: Date of measurement; date definition is Month-Year.
- site.name: Short site name with encoded geology and river information (First letter = geology: C=chalk, A=clay, G=greensand; Second letter = river initial; Number = river number, e.g., CE1 River Ebble; GA2 River Avon; GN1 River Nadder; CW2 River Wylye; AS1 tributary of River Sem; AS2 River Sem).
- geology: Sub-catchment underlying geology type (Clay, Chalk, Greensand).
- Coordinates: Location data provided for each river/site (latitude and longitude) to characterize site positions.

## Measurements and methods (by category)

- Genes
  - 16s: 16S rRNA gene abundance (genes g-1 sediment DW); DNA extraction from 0.25 g wet sediment; qPCR with SensiFAST kit; calibration 10^2–10^6 copies; primers specified (341F/805R); controls include standard negatives.
  - aoa: Ammonia oxidising archaea amoA gene (genes g-1 sediment DW); same extraction and qPCR approach; primers specified (CrenamoA-23F / 616R).
  - aob: Ammonia oxidising bacteria amoA gene (genes g-1 sediment DW); same extraction/qPCR; primers specified (amoA-1F / amoA-2R).
  - nirs: nirS gene (genes g-1 DW); same extraction/qPCR; primers specified (nirS-Cd3aF / nirS-R3cd).
  - nirk: nirK gene (genes g-1 DW); same extraction/qPCR; primers specified (nirK-1F / nirK-5R).
  - mcra: mcrA gene (genes g-1 DW); same extraction/qPCR; primers specified (mlas-F / mcrA-rev).
  - pmoa: pmoA gene (genes g-1 DW); same extraction/qPCR; primers specified (A189-F / A650-R).
- Carbohydrates
  - colloidal.cho: Colloidal carbohydrates; µg CHO g-1 DW; extraction with UHP water; glucose standard curve; phenol-sulphuric acid assay.
  - hw.cho: Hot-water extracted CHO; µg CHO g-1 DW; extraction at 100°C for 1 h; same quantification approach as colloidal CHO.
  - eps.30: Extracellular polymeric substances (EPS) extracted with 30% EtOH; µg EPS30 g-1 DW; extraction and reconstitution aligned with colloidal CHO method; PSA assay.
  - eps.70: EPS extracted with 70% EtOH; µg EPS70 g-1 DW; extraction and reconstitution aligned with colloidal CHO method; PSA assay.
- Carbon
  - DOC: Dissolved Organic Carbon; mg DOC g-1 sediment DW; subsampled from colloidal CHO fraction; measured with Shimadzu TOC-V against a 5-point calibration using potassium hydrogen phthalate standards.
  - TC: Total Carbon; mg TC g-1 sediment DW; combustion at 900°C; TOC/TC differentiation via inorganic carbon removal with acid pre-treatment.
  - TOC: Total Organic Carbon; (as above) mg TOC g-1 sediment DW; inorganic carbon removed prior to measurement.
- Particle size
  - colloid.pc, clay.pc, silt.pc, v.f.sand.pc, f.sand.pc, m.sand.pc, c.sand.pc, v.c.sand.pc, f.gravel.pc, m.gravel.pc, c.gravel.pc, v.c.gravel.pc, cobble.pc, boulder.pc: Percentages of particle size fractions; methods include sieving through a 0.850 µm mesh, weighing retained material, imaging with a camera, and image calibration; for some fractions, ImageJ analysis and counting a minimum of 6000 particles per sample.
  - Notes: Particle size data were generated from the same cores used for carbon analyses.
- Methane
  - mop: Methane oxidation potential; pmol g-1 sediment DW; incubation of 3 g sediment in 120 mL bottle with 500 ppm CH4 headspace; samples taken over 9 days with GC-FID analysis.
  - mpp.h2: Methane production potential with headspace 80% H2 / 20% CO2; pmol g-1 DW.
  - mpp.n2: Methane production potential with headspace 80% N2 / 20% CO2; pmol g-1 DW.
  - Analysis: Headspace sampling every 3 days; GC conditions specified (Shimadzu GC-FID for production; column and temperature settings provided).
- Anions and cations (river water)
  - Acetate, fluoride, formate, nitrate, nitrite, phosphate, sulphate, ammonium, calcium, magnesium, potassium, sodium: µmol L-1 for river water; measured with Dionex ICS3000 ion chromatography (AS18 column; KOH/MilliQ eluents); 0–200 µmol L-1 calibration; samples filtered (0.2 µm) and frozen before analysis.
- Anions and cations (sediment)
  - Acetate.sed, fluoride.sed, formate.sed, nitrate.sed, nitrite.sed, phos.sed, sulphate.sed, ammonium.sed, calcium.sed, magnesium.sed, potassium.sed, sodium.sed: µmol g-1 DWsediment; sediment-based measurements follow corresponding river water methodologies with units adjusted to per-gram of dry sediment.

## Methodology and data quality

- Consistency and replication: Standard qPCR controls (negative controls) used; internal calibration curves spanned 10^2 to 10^6 copies for gene targets.
- Sample handling: DNA extraction from 0.25 g wet weight sediment; sub-cores processed for paired measurements; subsampling for DOC/TOC/TC via established TOC-V protocols.
- Data definitions: Variables are defined with explicit measurement units, methodologies, and primers where applicable; site.name encodes geology and river origin for traceability.
- Cross-domain measurements: Integrated molecular (gene abundances) and biochemical (carbohydrates, carbon fractions, methane metrics), mineralogical (particle-size), and aqueous chemistry (river water and sediment pore-water) data to support monitoring of carbon and nitrogen cycling processes.