# Overall sampling design

- Study aim: address how the functional microbial community involved in carbon and nitrogen cycling changes seasonally and with geology.
- Sampling framework: at each site, 5 sediment cores (internal diameter 8 cm) were collected within a 25 m river reach; from each core, 4 sub-cores (internal diameter 2 cm) were taken to pair measurements; sub-cores stored according to analysis type.
- Data structure: measurements are paired within a column to enable direct comparison across analyses.

## Metadata and identifying information

- Date and measurement labeling: date of measurement; date defined as Month-Year.
- Site identification: site.name encodes underlying geology (C=chalk, A=clay, G=greensand) and river initial; includes a unique river number (e.g., CE1, GA2, GN1, CW2, AS1, AS2) with corresponding geographic coordinates.
- Geology: sub-catchment underlying geology type (Clay, Chalk, Greensand).

## Data categories and measurements

- Genes
  - 16S rRNA genes per gram sediment DW; DNA extraction from 0.25 g wet weight; qPCR with specified primers; absolute quantification against internal standard curves (10^2 to 10^6 copies); includes standard negative controls.
  - Target genes include amoA (archaea and bacteria: aoa, aob), nirS, nirK, mcrA, pmoA with genes g-1 sediment DW.
  - Primers and references provided for replication and traceability.

- Carbohydrates
  - Colloidal CHO (glucose equivalents) per g sediment; hot-water extracted CHO; extracellular polymeric substances (EPS) extracted with 30% and 70% ethanol.
  - Extraction and quantification methods described (phenol-sulphuric assay; storage and reconstitution steps).

- Carbon
  - DOC and TOC per g sediment DW; DOC from colloidal CHO fraction; TOC measured after acidification to remove inorganic carbon.
  - Instrumentation: Shimadzu TOC-V; calibration curves used (0–1000 mg/L range).

- Particle size
  - Particle-size fractions expressed as percentages: colloidal, clay, silt, very fine/ fine/ medium sands, coarse/fine gravel, very coarse gravel, cobble, boulder.
  - Methods: 0.850 µm sieve, imaging and ImageJ-based counting (minimum ~6000 particles per sample); multiple granulometry categories defined.

- Methane
  - Methane oxidation potential (mop) in pmol g-1 sediment DW; incubation with methane headspace; GC-FID analysis.
  - Methane production potential (mpp) with 80% H2/20% CO2 or 80% N2/20% CO2 headspaces; analysis by GC-FID.

- Anions and cations (river water and sediment)
  - River water: acetate, fluoride, formate, nitrate, nitrite, phosphate, sulfate, ammonium, calcium, magnesium, potassium, sodium; measured with a Dionex ICS3000; 7-point calibration (0–200 µmol L-1).
  - Sediment: same species (e.g., acetate.sed, nitrate.sed, phosphate.sed, ammonium.sed, etc.) reported per g DW; standardization and calibration implied.

## Data provenance and methodology

- Broad methodological consistency across analyses (sample collection, extraction, qPCR, colorimetric assays, TOC analyses, particle imaging, GC analyses).
- Use of internal standards, calibration curves, technical replicates, and negative controls to ensure measurement reliability.
- Detailed primers, references, and instrument settings provided to enable replication and cross-study comparability.

## Quality assurance and data governance

- QA features: standard negative controls for qPCR; internal calibration curves spanning 10^2–10^6 copies; imaging calibration and counting standards; adherence to specified extraction and measurement protocols.
- Metadata richness supports data discoverability and reuse (date, site name with encoded geology, coordinates, geology, and multi-omics/chemical measurements).
- Data are structured to facilitate cross-site comparisons and integration with broader data networks (consistent units, clearly defined measurements, and documented methodologies).

## Implications for data management and reuse (Data Leaders perspective)

- Strengths: comprehensive, multi-domain dataset with explicit metadata, traceable sampling design, and standardized protocols enabling broader data sharing and interoperability.
- Considerations for data system design:
  - Maintain a centralized data dictionary linking site.name encodings to geology, coordinates, and river identity to support cross-site querying.
  - Ensure all measurement blocks (genes, carbohydrates, carbon, particle size, methane, ions) maintain consistent units and naming conventions; capture method revisions if any.
  - Preserve detailed QA records (calibration ranges, controls, primers, and references) to support data quality assessments.
  - Catalog data by sampling event (date, site, core, sub-core) to enable longitudinal analyses and co-ownership of data products by policy/analytical teams.
  - Plan for data updates and versioning, given iterative analyses and potential methodological updates, to maintain discoverability and reproducibility.