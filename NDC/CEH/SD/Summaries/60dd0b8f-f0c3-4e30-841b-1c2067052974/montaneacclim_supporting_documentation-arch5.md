# Summary

## Overview
- Dataset of key photosynthesis and respiration measurements from three common garden sites along an elevation/temperature gradient in the Colombian Andes, collected June–August 2019.
- Three CSV files accompany the dataset:
  - ACiData_ColombianAlso_2019
  - VcmaxJmaxData_ColombianAndes_2019
  - RdarkData_ColombianAndes_2019
- Data include standardized column names, units, and descriptions (Table 1) and cover leaf gas exchange, temperature, humidity, and pressure data across eight tree species.

## Data products and schema
- Data files:
  - ACiData_ColombianAndes_2019.csv: A-Ci curve measurements (photosynthesis, intercellular CO2, stomatal conductance, leaf temperature, RH, chamber CO2, etc.).
  - VcmaxJmaxData_ColombianAndes_2019.csv: Derived Vcmax (carboxylation) and Jmax (electron transport) values, plus temperature-corrected estimates.
  - RdarkData_ColombianAndes_2019.csv: Dark respiration data (Rdark) adjusted to measurement temperatures.
- Column definitions (Table 1) include:
  - ID (plant/genotype, e.g., "C.multiflora 1001")
  - Date, Time
  - A (photosynthesis rate)
  - Ci (internal CO2)
  - gsw (stomatal conductance)
  - Tleaf (leaf temperature)
  - RH (relative humidity)
  - Qin (in-chamber light, µmol m-2 s-1)
  - Patm (chamber pressure)
  - Vcmax25, VcmaxTg (Vcmax at 25°C and at growth temperature)
  - Jmax25, JmaxTg (Jmax at 25°C and at growth temperature)
  - Rdark25, RdarkTg (Rdark at 25°C and at growth temperature)
- Experimental design details (below) provide context for data provenance and enabling metadata capture.

## Experimental design and sites
- Three experimental sites along an elevational gradient in the Colombian Andes:
  - High elevation: ~2516 m, mean annual temperature (MAT) ~14°C
  - Mid elevation: ~1357 m, MAT ~22°C
  - Low elevation: ~736 m, MAT ~26°C
- Plot structure:
  - One individual from each species planted in each of six blocks per plot
  - 6x15 plants per plot; 4x90 plants per site
- Species and sampling:
  - Eight species, measurements from 123 individuals
  - Soils were common across sites (400 kg soil per tree) with irrigation to maintain consistent moisture
  - Seeds grown for two years in nursery at mid-elevation before field planting (Nov–Dec 2018)

## Data collection and processing

### A-Ci (photosynthesis) data
- Instrument: LI-6800 portable photosynthesis system
- Leaf cuvette conditions: 29°C, 65% RH, 410 ppm CO2
- Measurement protocol: once stable at g_s ≥ 0.05 mol m-2 s-1, measurements across eight ambient CO2 concentrations (Ca): 410, 300, 175, 60, 410, 800, 1500, 2000 µmol mol-1
- Light: saturating PPFD selected per species based on preliminary A-Q curves
- Data file: MontaneAcclim-ACiData2019.csv

### Estimation of Vcmax and Jmax
- Derived from A-Ci curves by fitting Farquhar et al. (1980) C3 photosynthesis model using the R package plantecophys (fitacis)
- Incorporates measured Rdark values adjusted to respective A-Ci measurement temperatures
- Modeling details:
  - Initial method: default non-linear regression (no a priori region constraints)
  - If default deemed unsuitable, switch to bilinear approach (two linear regressions to estimate Vcmax and then Jmax)
- Quality control:
  - All curves and estimates quality-checked
  - Some curves rejected (unusual Vcmax/Jmax, or photosynthesis consistently Rubisco-limited affecting Jmax)
  - Outcome: 144 of 147 individuals retained; 9 Jmax values excluded
- Temperature corrections:
  - Vcmax and Jmax corrected to both 25°C and site MAT using a temperature response function with Ea, ΔS, and Hd parameters
  - Temperature response parameters drawn from Kumarathunge et al. (2019)
- Data file: VcmaxJmaxData_ColombianAndes_2019.csv

### Dark respiration (Rdark) data
- Procedure: after A-Ci measurements, leaves dark-adapted (≥30 minutes, sometimes hours) with leaf area covered, CO2 efflux measured with LI-6800 at 5 s intervals for 1 min (between 15:00–16:00)
- Measurements: 12 values per leaf, mean used as Rdark, measured at site ambient temperature
- Temperature correction:
  - Rdark adjusted to A-Ci measurement temperatures using an exponential fixed Q10 equation
  - Q10 temperature dependence also adjusted by Tg (MAT of study site: 14, 22, or 26°C)
  - Rdark values corrected to 25°C and site MAT
- Data file: RdarkData_ColombianAndes_2019.csv

## Data governance, quality and accessibility

- Metadata and provenance:
  - Clear documentation of column definitions, units, and data transformations (Table 1)
  - Transparent experimental design, sampling, and processing steps
- Quality assurance:
  - Rigorous curve-fitting and quality checks for Vcmax/Jmax
  - Documentation of exclusions (unusual values, Rubisco-limited curves)
- Data availability:
  - All three CSVs are provided as part of the dataset, with the accompanying methodological details and references
- Reuse considerations:
  - Temperature-corrected Vcmax/Jmax values and Rdark allow cross-site comparisons
  - Notes on potential data gaps due to instrument errors or post-processing exclusions
  - Publications and methods cited for reproducibility (Farquhar et al. 1980; Duursma 2015; Kumarathunge et al. 2019; Scafaro et al. 2017; Tjoelker et al. 2001; R Core Team 2022)

## Key data governance considerations for stewardship
- Ensure metadata remains linked to all derived variables (VcmaxJmaxData and RdarkData) to preserve interpretability
- Maintain traceability of temperature corrections and site-specific parameters (Patm, Tg, Tg-related constants)
- Document any data exclusions and the criteria used to determine data quality
- Provide access guidance on how to reproduce the curve-fitting and corrections (code snippets or workflow steps, e.g., fitacis usage and correction equations)

## References (for methods and provenance)
- Duursma, R. A. (2015). Plantecophys—an R package for analysing and modelling leaf gas exchange data. PLoS One.
- Farquhar, G. D., von Caemmerer, S., & Berry, J. A. (1980). A biochemical model of photosynthetic CO2 assimilation in leaves of C3 species. Planta.
- Kumarathunge, D. P. et al. (2019). Acclimation and adaptation components of the temperature dependence of plant photosynthesis at the global scale. New Phytologist.
- R Core Team (2022). R: A language and environment for statistical computing.
- Scafaro, A. P. et al. (2017). Strong thermal acclimation of photosynthesis in tropical and temperate wet-forest tree species. Global Change Biology.
- Tjoelker, M. G. et al. (2001). Modelling respiration of vegetation: evidence for a general temperature-dependent Q10. Global Change Biology.