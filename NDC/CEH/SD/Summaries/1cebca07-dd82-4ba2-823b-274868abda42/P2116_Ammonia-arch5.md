# Bacterial community structure and soil process data from a sewage sludge amended upland grassland soil experiment, 2000 [NERC Soil Biodiversity Programme] Gray, N.D., Hastings, R.C., Sheppard, S.K., Loughnane, P., Lloyd, D., McCarthy, A.J. and Head, I.M

## Overview
- A data package from the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biodiversity and biogeochemical processes in a large field experiment at Sourhope, Scotland.
- Aims to link soil microbial community structure with functional soil processes under different soil-improvement treatments.

## Project and site scope
- Experimental site: Sourhope Research Station, Cheviot Hills, Southern Scotland; acidic brown forest soils.
- Design: randomized block with 12 plots and four treatments: untreated (control), lime, sewage sludge, and sewage sludge after lime; lime applied in 1999–2000; sludge applied August 1999 and May 2000.
- Temporal and spatial sampling: soil cores collected spring–summer 1999–2000; key analyses focused on the root zone; sampling days after sludge application include 1, 3, 16, 30, and 58 (May 30, 2000).
- Primary questions: whether sludge/liming treatments select for specific bacterial populations and how community structure relates to soil biogeochemical function.

## Datasets and contents
- Dataset 1034: Soil analysis data (2000)
  - Measures: soil pH, moisture, total carbon, total organic carbon, total Kjeldahl nitrogen, NH3, basal respiration, nitrification potentials, TTGE-related analyses, and other soil-process metrics (e.g., CO2 evolution, nitric species).
  - Methods: standard soil chemistry and gas-phase CO2 detection; nitrification potential via chlorate-treated slurries; TTGE analysis of PCR-amplified 16S rDNA and ammonia-oxidizer rDNA fragments.
  - Source and handling: analyses undertaken at University of Newcastle; samples stored at 4°C (short-term) and -70°C (molecular analyses).
- Dataset 1035: Soil analysis data – Bulk Sampling Details
  - Metadata for sampling units: unique sampling unit identifiers (SUID), blocks, main plots, sub-plots, cell coordinates, treatment, soil horizon, time after sludge, and sample type.
- Dataset 1124: Numerical analysis of eubacterial community profiles (TTGE)
  - TTGE banding data for eubacteria (bands 1–54) across treatments and times; includes band intensity and position data for similarity analyses.
- Dataset 1125: Numerical analysis of ammonia oxidizer community profiles (TTGE)
  - TTGE data for ammonia-oxidizing bacteria (bands 1–54) across time points; includes band positions and intensities.
- Dataset 1126: Numerical analysis of ammonia oxidizer community profiles (TTGE) for sludge-only
  - TTGE data focusing on sludge-treated plots across all time points; band data and relative intensities.
- Dataset 1127: Numerical analysis of ammonia oxidizer community profiles (TTGE) for untreated soil only
  - TTGE data focusing on untreated plots across all time points; band data and relative intensities.

## Data collection, analysis, and structure
- Analytical methods
  - TTGE (Temporal Temperature Gradient Electrophoresis) to profile predominant microbial members; DNA extraction via Griffiths et al. (2000) method; gel electrophoresis and staining for visualization.
  - PCR products with GC clamps; analysis of 16S rDNA (eubacteria) and ammonia-oxidizer 16S rDNA fragments; image analysis for band presence/intensity; similarity and cluster analyses (Sorensen coefficients, UPGMA); ANOVA to assess time vs. treatment effects.
  - Soil processes: basal respiration (CO2), autotrophic nitrification potential (nitrite accumulation), and related soil chemistry (pH, moisture, TOC, TKN, NH3).
- Data formats and structure
  - Data provided as eight CSV files with clearly defined fields (SampleID, SUID, BLOCK, MAIN_PLOT, SUB_PLOT, TREATMENT, HORIZON, DAYS_AFTER_SLUDGE, etc.).
  - TTGE datasets (1124–1127) include BAND_NUMBER or BANDS1-54, RELATIVE_INTENSITY, and related metadata.
  - Missing values coded (e.g., -999) in numeric fields; time and sampling metadata aligned to Scott et al. references (2003).
- Quality control
  - Numeric range checks, formatting checks, and logical integrity checks implemented.
  - While QA procedures were performed, the data provider (NERC Soil Biodiversity Programme) does not warrant accuracy or fitness for a particular use; no liability for data use is assumed.
- Documentation and references
  - Supporting methods and contextual references linked (e.g., Eaton et al. 1995; Griffiths et al. 2000; Head et al.; Scott et al. 2003; related works on sludge impact on gas dynamics and methanogen communities).

## Data governance, access, and reuse
- Data discoverability and provenance
  - Project code P2116 (Effects of soil improvement treatments on bacterial community structure and function); data generated at Sourhope, University of Newcastle; linked to published papers and the SOURHOPE FIELD DATA HANDBOOK.
- Access and reuse considerations
  - Baseline data and additional environmental context are available through the Environmental Information Centre catalogue (eidc.ceh.ac.uk); the dataset package includes comprehensive metadata to support reuse and replication.
- Standards and interoperability
  - Metadata align with field plot design (BLOCK, MAIN_PLOT, SUB_PLOT), sampling times, and treatment codes; TTGE and molecular data are structured for comparative analyses across time and treatments.
- Practical stewardship implications
  - Documentation facilitates data discovery, cross-study integration, and re-use in meta-analyses; however, users should consult referenced publications for methodological nuances and data interpretation.
  - Data may require harmonization with other datasets (e.g., different TTGE platforms or newer sequencing methods) for broader interoperability.

## Key considerations for Data Stewards
- Ensure continued accessibility and linkage to the EIDC catalogue and related publications.
- Maintain clear provenance, including project code, sampling framework, and treatment descriptions.
- Preserve data formats (CSV) and the accompanying metadata schemas to support discoverability and re-use.
- Provide guidance on interpretation of TTGE-derived data alongside soil-process measurements.
- Monitor for potential updates or derived datasets that may be produced from these data (e.g., re-analyses with new statistical methods).