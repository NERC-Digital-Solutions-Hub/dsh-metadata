# Overview of the data

- Study context: Mesocosm experiment in West Greenland (Kangerlussuaq area) across three lakes to assess how dust addition affects water chemistry and phototrophs in water and sediments. Data collected by Suzanne McGowan and Amanda Burson.

- Experimental design and sampling regime:
  - In situ mesocosms installed in three lakes in July 2018 and run for 14 days.
  - Each lake contained 6 enclosures (polythene tubes, 60 cm diameter, ~1 m depth; water inside 49–84 cm).
  - Dust treatment: three enclosures received dust at 0.196 g/L (roughly 25–35 g per enclosure, adjusted for depth); three served as controls.
  - Dust sourced from a thawed snowbank, filtered and freeze-dried.
  - Experimental layout: alternating dust and control in a 3x2 arrangement.
  - Measurements: in situ conductivity, temperature, and dissolved oxygen (via YSI multiprobe in upper 20 cm); water and phytoplankton sampled from mesocosms at start and end (or end only if sampling destructive); surface sediments collected at start and end; terracotta pots placed at enclosure bottoms for phytobenthos sampling (conducted at end).
  - Timings: start (day 0) and final sampling; lake-site timing entries include specific calendar dates (e.g., SS17b: 8-7-2018 and 22-7-2018; SS1590: 9-7-2018 and 23-7-2018; SS906: 10-7-2018 and 24-7-2018).

- Collection, generation, and transformation methods:
  - Water samples filtered in the field through GF/F filters; filtered water stored refrigerated for lab analyses of dissolved nutrients.
  - Chlorophyll a estimated from filter papers; terracotta pots scraped for biofilms; solids frozen for later analysis; volumes recorded and aliquots taken for quantitative analysis.
  - Surface sediments stored frozen prior to analysis.

- Analytical methods and units:
  - Water chemistry: soluble reactive phosphorus (SRP), ammonium, silicate, total phosphorus (TP), total nitrogen (TN). Units: µg/L or mg/L (silicate in mg/L); major ions via ion chromatography.
  - Chlorophyll analysis: chlorophyll a from water, phytobenthos, and sediments; units: µg/L (water), µg/cm2 (phytobenthos), µg/g (sediments).
  - Pigment analysis (HPLC): chlorophylls and carotenoids quantified; results expressed as nanomoles per gram of sediment or per cm2 for pot scrapes; pigment suite includes chlorophyll a/b, β-carotene, fucoxanthin, lutein, zeaxanthin, diadinoxanthin, diatoxanthin, pheophytins, among others.
  - Detailed extraction and HPLC method parameters provided (solvents, gradient, detectors, calibration, and quality checks).
  - Totals and pigments per sample type (water, surface sediments, artificial substrate scrapes) are captured with explicit units and concentrations.

- Quality control and data integrity:
  - Colorimetric water chemistry calibrations validated with r2 ≥ 0.998.
  - Ion chromatography calibrated with 10-point curves.
  - YSI probes calibrated daily for pH and DO, and conductivity/calibration performed weekly.
  - HPLC pigments calibrated with 8-point curves; stability checked with control extracts at start and end of runs; manual verification of pigment identifications and peak integrations by an expert.
  - Data and pigment quantifications rely on reference standards and established methods (APHA 2005; Chen et al. 2001; Parsons & Strickland 1963).

- Data structure and scope:
  - Dataset contains 37 rows and 46 data columns.
  - Columns 1–5: experimental descriptors (lake code, dust treatment, replicate, time point, sample date).
  - Columns 6–17: water measurements at start and end (e.g., chlorophyll a, nutrients, etc.).
  - Columns 18–31: surface sediment analyses (chlorophyll pigments and related metrics).
  - Columns 32–46: terracotta pot scrape analyses (pigments and related metrics).
  - Data organization supports comparisons across lake sites, dust treatment, time points, and sample types (water, sediments, and phytobenthic substrates).

- References and methodological basis:
  - APHA (2005) Standard Methods for the Examination of Water and Wastewater.
  - Chen et al. (2001) pigments as biomarkers for historical hypoxia.
  - Parsons & Strickland (1963) spectrophotometric determination of marine-plant pigments; chlorophyll and carotenoid quantification methods.

- Data handling and accessibility notes for data leadership:
  - Data include detailed metadata on sampling dates, locations, treatment, replicates, and sample types.
  - Physical samples were preserved (frozen) for subsequent laboratory analyses, with explicit procedures for volume, weights, and preparation.
  - Comprehensive QA/QC records accompany the analytic methods to support data reliability and reproducibility.
  - Potential opportunities for data reuse include cross-lake comparisons, treatment effects on nutrient dynamics, and pigment-based assessments of phytoplankton and biofilm communities under dust perturbation.