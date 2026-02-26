# Bacterial community structure and soil process data from a sewage sludge amended upland grassland soil experiment, 2000 [NERC Soil Biodiversity Programme]

- This dataset collection is part of the NERC Soil Biodiversity Thematic Programme (1999–2003), focused on linking soil biodiversity with biogeochemical processes at the Sourhope field site in the Scottish Borders.
- Aimed to understand how soil improvement treatments (sludge and lime) affect bacterial community structure and key soil processes, and how changes in community composition relate to ecosystem functions.

## Experimental site and design

- Location: Sourhope Research Station, Cheviot Hills, Southern Scotland; soils are acidic brown forest soils on old red sandstone drift.
- Design: randomised block with three replicates across four treatments: untreated control, lime only, sewage sludge only, sewage sludge followed by lime.
- Treatments applied: lime 600 g m-2 over two years; sewage sludge applications of 10 L m-2 (Aug 1999) and 20 L m-2 (May 2000).
- Sampling strategy: soil cores collected from all plots over spring–summer 1999 and 2000; in 1999 most activity occurred in the root zone, so 2000 sampling focused on the root zone. Sampling days after sludge application: 1, 3, 16, 30, 58 (May 30, 2000).

## Data collected and measurements

- Soil characteristics (per sample): pH (1:2 soil-water), moisture (drying to constant weight), total carbon, total organic carbon, total Kjeldahl nitrogen, soil NH3, and baseline soil/weather/vegetation data (from Environmental Information Centre).
- Soil process measurements: basal respiration (CO2 production), nitrification potential (nitrite accumulation in chlorate-treated slurries).
- Molecular analyses: TTGE (Temporal Temperature Gradient Electrophoresis) of PCR products to profile bacterial communities; analyses for eubacterial 16S rDNA and ammonia-oxidizing bacteria (AOB) 16S rDNA fragments.
- DNA/RNA handling: DNA extracted from soil; subsamples stored at -70°C for molecular analyses.
- Data handling: data stored and quality-assured; outputs summarized in reports and used for downstream analyses.

## Analytical methods

- Basal respiration: CO2 production monitored from incubated soil slurries with a gas chromatography–mass spectrometry setup.
- Nitrification potential: nitrite accumulation measured colorimetrically in chlorate-inhibited slurries.
- TTGE: routine DNA extraction, PCR amplification with GC-clamped primers, and TTGE separation to generate banding patterns representing community structure.
- Image analysis: TTGE gels scanned and bands quantified; intensities and positions used to compare community profiles.
- Statistical analyses: Sorensen similarity coefficients calculated from TTGE band intensities; two-factor (time and treatment) ANOVA; clustering via UPGMA; exploratory PCA not employed due to experimental design.

## TTGE data and numerical analyses

- Datasets 1124, 1125, 1126, and 1127 cover TTGE analyses for:
  - Eubacterial community profiles (across all time points)
  - Ammonia-oxidizer community profiles (across all time points)
  - Sludge-only treatment (ammonia-oxidizer profiles)
  - Untreated soil (ammonia-oxidizer profiles)
- Data components include sample metadata (Block, Main Plot, Sub-Plot, Treatment, Horizon, Days After Sludge) and TTGE band data (band numbers, intensities, relative intensities).
- Datasets also capture sampling unit identifiers and detailed field metadata to enable cross-referencing with soil analyses.

## Datasets and data structure

- Dataset 1034: Soil analysis data (2000)
  - Measurements: soil pH, moisture, total carbon, total organic carbon, total Kjeldahl nitrogen, NH3, soil respiration, nitrification potential, and related metadata (SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, etc.).
- Dataset 1035: Soil analysis data: Bulk Sampling Details
  - Sampling metadata: sampling unit IDs, block/main plot/sub-plot, cell coordinates, treatment, horizon, time after sludge, sample type.
- Dataset 1124: Numerical analysis of eubacterial community profiles (P2116_EUBACTERIAL_CP.csv)
  - TTGE-derived band intensity data across time and treatments for eubacteria.
- Dataset 1125: Numerical analysis of ammonia oxidizer community profiles (P2116_AMMONIA_OXIDISER_CP.csv)
  - TTGE-derived band intensity data for ammonia-oxidizing bacteria.
- Dataset 1126: Numerical analysis of ammonia oxidizer community profiles (sludge) (P2116_AMMONIA_SLUDGE.csv)
  - Ammonia-oxidizer TTGE data focused on sludge-only treatment.
- Dataset 1127: Numerical analysis of ammonia oxidizer community profiles (untreated soil) (P2116_AMMONIA_UNTREATED.csv)
  - Ammonia-oxidizer TTGE data for untreated control.
- Each dataset includes standardized fields for sample identifiers, plot/treatment metadata, time points, and TTGE band data.

## Quality control and data governance

- Verification steps included numeric range checks, formatting validation, and logical integrity checks to ensure data consistency.
- Data are subject to quality assurance, but the issuing body (NERC) cannot warrant the accuracy or fitness for a particular use; liability for data use is explicitly disclaimed.
- Baseline weather, vegetation surveys, soil characteristics, and above-ground biomass data are available from the Environmental Information Centre catalogue for broader context.

## Access and use

- Data are organized for reuse within environmental monitoring and soil biodiversity research contexts.
- Data are linked to published work and supporting information; data availability is complemented by a field data handbook and related references.
- Useful for analysts aiming to compare microbial community structure with soil functional measures (respiration, nitrification) under contrasting sludge and lime treatments, and for integrating TTGE-derived profiles with soil chemistry data.

## References and further reading

- References include standard methods for soil and water analysis, method papers on TTGE and microbial community analysis, and related studies from the Sourhope field experiments.
- Key related works: Scott et al. (Sourhope Field Data Handbook), Gray et al. (soil biodiversity studies), Head et al. (sludge impact on gas dynamics and methanogens), and standard methods compilations (Eaton et al., 1995; Griffiths et al., 2000; Kopp & McKee, 1983).