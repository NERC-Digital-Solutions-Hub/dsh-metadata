# Photosynthesis and respiration data from three common garden sites along an elevation/temperature gradient in the Colombian Andes

## Overview
- A dataset of key photosynthesis and leaf respiration measurements collected June–August 2019 across three elevation sites in the Colombian Andes.
- Contains three CSV files:
  - ACiData_ColombianAndes_2019
  - VcmaxJmaxData_ColombianAndes_2019
  - RdarkData_ColombianAndes_2019
- Measurements target eight mid-successional Andean tropical montane forest species, across 123 individuals (data from 147 initially collected; some values excluded for quality).
- Variables include photosynthetic rate (A), intercellular CO2 (Ci), stomatal conductance (gsw), leaf temperature (Tleaf), relative humidity (RH), chamber CO2 (Qin), chamber pressure (Patm), and model-derived parameters (Vcmax25, VcmaxTg, Jmax25, JmaxTg, Rdark25, RdarkTg).
- All data were processed to assess thermal acclimation of photosynthesis, with corrections to 25°C and site mean annual temperature (MAT).

## Data files and key variables
- ACiData_ColombianAndes_2019.csv
  - A, Ci, gsw, Tleaf, RH, Qin, Patm, Date, Time
  - Measurement conditions for A–Ci curves using LI-6800
- VcmaxJmaxData_ColombianAndes_2019.csv
  - Vcmax25, VcmaxTg, Jmax25, JmaxTg, Rdark25, RdarkTg, and related metadata
  - Derived from fitting A–Ci curves to the Farquhar model
- RdarkData_ColombianAndes_2019.csv
  - Rdark measurements (mean of 12 values per leaf) adjusted to measurement temperatures
  - Dark respiration data collected after A–Ci measurements

## Experimental design
- Three sites across an elevation gradient with mean annual temperatures (MAT): high elevation (~14°C), mid elevation (~22°C), low elevation (~26°C).
- Plots: six blocks per site; each block planted with one individual per species (total per plot: 6x15 plants; per site: 4x90 plants).
- Plant material: eight species, planted from nursery stock completed in 2018; common soils and irrigation used.
- Data collection: June–August 2019, resulting in 123 individuals measured (data quality issues excluded some values).

## A-Ci data collection and processing
- Instrument: LI-6800 portable photosynthesis system.
- Cuvette conditions: standardized at 29°C, 65% RH, 410 ppm CO2; measurements taken after gs ≥ 0.05 mol m⁻² s⁻¹.
- A–Ci protocol: eight ambient CO2 concentrations (Ca values: 410, 300, 175, 60, 410, 800, 1500, 2000 μmol mol⁻¹) with species-specific saturating PPFD.
- Output: raw A–Ci data stored in MontaneAcclim-ACiData2019.csv and used to estimate Vcmax and Jmax.

## Vcmax and Jmax estimation and quality control
- Modeling: A–Ci data fitted to the Farquhar, von Caemmerer & Berry C3 model using the plantarophys R package (fitacis function).
- Inputs: prepared CSVs, measured Rdark values included; temperature corrections applied post-fit.
- Fitting methods:
  - Default method: non-linear regression without assuming Vcmax- or Jmax-limited regions.
  - Bilinear method: used when default fitting deemed data unsuitable.
- Quality checks: curves with implausible Vcmax or Jmax values or Rubisco-limited photosynthesis leading to inaccurate Jmax were removed.
- Retention: 144 of 147 individuals retained for Vcmax/Jmax analysis; 9 Jmax values excluded.
- Temperature corrections:
  - Vcmax and Jmax adjusted to 25°C and to each site MAT using a specified temperature response function (parameters drawn from contemporary literature).
  - Temperature parameters (Ea, ΔS, Hd) and site MAT used to compute corrected values.

## R dark (respiration) data and corrections
- Collection: dark respiration measured after dark adaptation (foil-covered leaves for 30+ minutes); CO2 efflux recorded every 5 seconds for 1 minute within 15:00–16:00.
- Temperature adjustments: Rdark values corrected to A–Ci measurement temperatures using a fixed Q10-based exponential equation, incorporating site MAT to reflect temperature dependence.
- Rdark values are provided alongside temperature-adjusted Rdark25 and RdarkTg where applicable.

## Data usage and notes
- Data are suitable for analyses of thermal acclimation of photosynthesis across species and site temperatures.
- Some data are missing due to instrument error or quality control; 144/147 A–Ci fits and corresponding Vcmax/Jmax values are provided.
- All data have been quality-checked and corrected for temperature effects to enable cross-site comparisons.

## References for methods
- Duursma, R. A. 2015. Plantecophys: an R package for analysing and modelling leaf gas exchange data.
- Farquhar, G. D., von Caemmerer, S., & Berry, J. A. 1980. A biochemical model of photosynthetic CO2 assimilation in leaves of C3 species.
- Kumarathunge et al. 2019. Acclimation and adaptation components of the temperature dependence of plant photosynthesis at the global scale.
- R Core Team 2022. R: A language and environment for statistical computing.
- Scafaro et al. 2017. Thermal acclimation of photosynthesis in tropical and temperate forest species.
- Tjoelker et al. 2001. Modelling respiration of vegetation: evidence for a general temperature-dependent Q10.