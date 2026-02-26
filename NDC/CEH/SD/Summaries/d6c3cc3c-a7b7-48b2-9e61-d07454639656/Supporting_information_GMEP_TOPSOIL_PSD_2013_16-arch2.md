# Glastir Monitoring & Evaluation Programme: Topsoil PSD Analysis (2013-2016)

## Overview
- Welsh Government programme (GMEP) to monitor soil quality and environmental outcomes of the Glastir agri-environment scheme.
- Aims to collect evidence on effectiveness of management interventions and quantify status/trends in soil quality related to climate change, biodiversity, soil and water quality, and woodland expansion.
- 4-year rolling survey (2013–2016) with two components: Wider Wales (baseline/national trends) and Targeted (Glastir-priority areas); uses a common 1 km square spatial unit for integration.

## Survey Design and Sampling
- 300 x 1 km squares sampled over the 4-year cycle; half randomly sampled within Land Classification strata, half targeted at Glastir priority areas.
- Exclusion criteria: squares with >75% urban land or >90% sea excluded.
- Sample units align with the Countryside Survey GB methodology to enable future integration.
- Within each square, soil samples collected from 5 randomly dispersed locations, using a C-core (15 cm) aligned with vegetation surveys.
- Samples refrigerated and sent to laboratories for PSD analysis.

## Soil Preparation and PSD Analysis (Materials and Methods)
- Primary focus: particle size distribution (PSD) using laser diffraction (LD) with Beckman Coulter LS13 320.
- Complementary reference methods: traditional hydrometer method for comparison.
- Sample preparation: remove organic matter (per UK CEH Bangor peroxide digest), suspend in 5% Calgon, shaken overnight.
- Instrument setup: warm-up, align, background checks, specific run settings (pump 75%, 10 s sonication, 3 runs, soil-eu.rf780d model).
- Sand fraction collected via 63 µm sieve at end of analysis; sand weighed for QA.
- Size class definitions (final LD cut-offs): Sand 64.61–2000 µm, Silt 2.42–63.41 µm, Clay 0.04–2.41 µm.

## Quality Assurance and Quality Control
- Adherence to NERC Joint Codes of Practice; inclusion of standard soils (BS1, BS3) in each batch; QA documentation.
- Instrument calibration, pre-run checks, and flushing with a sand sample to prevent contamination.
- Replicates: about 1 in 10 samples, to assess reproducibility.
- Cross-validation: LD results checked against the sieve sand fraction; organic matter can cause LD overestimation of sand when LOI is high (40–50%).
- Comparison with hydrometer method indicates LD is accurate across low-size ranges; hydrometer may overestimate clay due to sedimentation limitations.
- Standards used for accuracy checks: garnet (~13.8 µm), glass beads (~581 µm); replicates showed LD accuracy and reproducibility.
- Adjustment of LD clay/silt cut-offs suggested to align with sedimentation differences reported in literature.

## Inter-lab Validation and Data Comparability
- Comparisons with ADAS and BGS laboratories using three soils (sand, silt, clay) indicate LD method is accurate, reproducible, and broadly comparable across labs.
- Discrepancies noted between LD and hydrometer methods, especially at finer sizes; LD generally aligns with true values when appropriate standards are used.

## Data Structure and Metadata
- Dataset: GMEP_TOPSOIL_PSD_2013_16.csv
- Key fields include: SQ_ID (anonymised 6-letter code), PLOT_TYPE, PLOTNUM, PLOTYEAR, EASTING_10km, NORTHING_10km, LC (Land Classification), REPEATED, BATCH, and PSD size-bin percentages (e.g., SAND, SILT, CLAY) with TOTAL as QA metric.
- Data are organized to support national and sub-national analyses, enabling integration with other GB datasets.

## Implications for Monitoring and Analysis
- Provides standardized, scalable soil PSD data across Wales to assess soil quality, hydrology, pollutant transport, nutrient availability, and erosion potential.
- The 1 km square framework and 4-year rolling design support detection of spatial and temporal trends and drivers (land use, climate, pollution) beyond Glastir interventions.
- Emphasizes data quality, traceability, and interoperability, enabling reuse and integration with other monitoring datasets.
- Highlights the need to increase dataset value by combining PSD data with other environmental datasets and ensuring open access to underlying data where appropriate.

## Key Takeaways for Analysts Monitoring the Environment
- Establishes a robust, multi-scale, longitudinal PSD monitoring framework aligned with national surveys to evaluate environmental health and policy performance.
- Demonstrates rigorous QA/QC, cross-method validation (LD vs hydrometer), and inter-lab comparability to ensure reliable indicators.
- Facilitates transparent data storage, metadata documentation, and standardized outputs (reports, maps, charts) for stakeholder scrutiny and policy evaluation.