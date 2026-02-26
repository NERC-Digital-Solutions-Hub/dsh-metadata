# Overall sampling design

- Purpose and design
  - Measurements are paired within each column to assess seasonal and geological influences on the functional microbial community involved in carbon and nitrogen cycling.
  - At each site: 5 sediment cores (8 cm internal diameter) within a 25 m river reach; from each core, 4 sub-cores (2 cm dia) are taken to pair measurements.
  - Sub-cores are stored according to the analyses performed; data collection addresses hypotheses on seasonal and geology-driven changes.

- Identifying information (metadata for discovery and reuse)
  - date: measured date; date definition = Month-Year.
  - site.name: short site identifiers (e.g., CE1, GA2, GN1, CW2, AS1, AS2); encoding reflects geology and river name.
  - geology: sub-catchment underlying geology type (Clay, Chalk, Greensand).
  - site coordinates (latitude/longitude) provided for each site.

- Genes
  - Target genes and units:
    - 16s: genes g-1 sedimentDW; bacteria.
    - aoa: amoA gene from ammonia-oxidising archaea; genes g-1 sedimentDW.
    - aob: amoA gene from ammonia-oxidising bacteria; genes g-1 sedimentDW.
    - nirs: nirS gene; genes g-1 sedimentDW.
    - nirk: nirK gene; genes g-1 sedimentDW.
    - mcra: mcrA gene (methyl coenzyme M reductase); genes g-1 sedimentDW.
    - pmoa: pmoA gene (particulate methane monooxygenase) from methanotrophs; genes g-1 sedimentDW.
  - Methodology and quality controls:
    - DNA extraction from 0.25 g wet weight sediment (PowerSoil kit).
    - qPCR with SensiFAST kit; absolute quantification using calibration curves (102–106 copies).
    - Negative controls included; primer sets referenced (with sources).
  - Documentation supports traceability of gene abundances to specific organisms/processes.

- Carbohydrates
  - Colloidal CHO, HW CHO; EPS30, EPS70 with units in µg glucose equiv. g-1 sedimentDW.
  - Extraction and measurement:
    - Colloidal CHO: 60°C drying; UHP water extraction; phenol-sulphuric acid quantification; glucose standard curve.
    - HW CHO: hot water extraction at 100°C; calibration as for colloidal CHO.
    - EPS30/EPS70: extract from colloidal fraction using ethanol; PSA assay; calibrated against colloidal CHO.

- Carbon
  - DOC: mg DOC g-1 sedimentDW; digested from colloidal CHO fraction; measured with Shimadzu TOC-V against glucose-based standards.
  - TC: mg TC g-1 sedimentDW; TOC measured after removal of inorganic carbon (acidification) and high-temperature combustion.
  - TOC: mg TOC g-1 sedimentDW; method as for TC with inorganic carbon removal.

- Particle size
  - Fractions expressed as percentages:
    - colloid.pc, clay.pc, silt.pc, v.f.sand.pc, f.sand.pc, m.sand.pc, c.sand.pc, v.c.sand.pc, and various gravel/coarse fractions (e.g., v.f.gravel.pc, f.gravel.pc, m.gravel.pc, c.gravel.pc, v.c.gravel.pc).
  - Methodology:
    - Cores passed through 0.850 µm sieve; retained material weighed; images captured for particle counting and sizing.
    - ImageJ-based analysis; minimum ~6000 particles counted per sample; particle size calibration performed.

- Methane
  - Methane oxidation potential (mop): pmol g-1 sedimentDW.
  - Methane production potential (mpp.h2, mpp.n2): pmol g-1 sedimentDW for headspace with 80% H2:20% CO2 or 80% N2:20% CO2.
  - Methodology:
    - 3 g sediment in serum bottles; incubation ~9 days; headspace sampling every 3 days; GC-FID analysis with detailed instrument settings.

- Anions and cations (water and sediment extracts)
  - River water measurements (µmol L-1):
    - Acetate, Fluoride, Formate, Nitrate, Nitrite, Phosphate, Sulphate, Ammonium, Calcium, Magnesium, Potassium, Sodium.
    - Analysis via Dionex ICS3000 with AS18 column and KOH/MilliQ eluents; 7-point calibration (0–200 µmol L-1); filtration (0.2 µm) and freezing prior to analysis.
  - Sediment measurements (µmol g-1 DW):
    - Acetate.sed, Fluoride.sed, Formate.sed, Nitrate.sed, Nitrite.sed, Phos.sed, Sulphate.sed, Ammonium.sed, Calcium.sed, Magnesium.sed, Potassium.sed, Sodium.sed.
  - Documentation indicates comprehensive chemical profiling for both dissolved and particulate phases.

- Methodology note
  - The document includes a Methodology section header for several measurement groups, but the content appears incomplete or cut off at the end of the provided text.
  - Data Stewards should verify the completeness of the Methodology sections and ensure all procedural details are captured in the final dataset.

- Data governance and quality considerations for Data Stewards
  - Ensure consistent use of site codes, geology categories, and spatial coordinates to enable cross-dataset linking.
  - Maintain standardized units and measurement naming (e.g., genes g-1 sedimentDW, mg DOC g-1 sedimentDW, µmol L-1 river water, etc.).
  - Capture full provenance: extraction kits, qPCR kits, primers, calibration ranges, and reference publications for traceability.
  - Validate completeness of the Methodology sections (currently incomplete in the provided text) to support reproducibility.
  - Plan for data publication and portal ingestion, including metadata templates that reflect the fields listed (date, site, geology, coordinates, measurement type, unit, methodology).
  - Acknowledge potential data sharing constraints (embargoes, proprietary concerns) and document updates to datasets as measurements are refined or expanded.