# Montane Acclimation Data Colombian Andes 2019

## Overview
- Dataset of key photosynthesis and respiration measurements from three common garden sites along an elevation/temperature gradient in the Colombian Andes, collected June–August 2019.
- Three CSV files: ACiData_ColombianAndes_2019, VcmaxJmaxData_ColombianAndes_2019, and RdarkData_ColombianAndes_2019.
- Variables include leaf temperature, humidity, pressure, photosynthesis (A), intercellular CO2 (Ci), stomatal conductance (gsw), light (Qin), and site-specific temperature corrections (Vcmax25, VcmaxTg, Jmax25, JmaxTg, Rdark25, RdarkTg).
- Data were collected and analyzed to assess thermal acclimation potential across eight key tropical montane forest species; some values missing due to instrument error or quality screening.

## Data files and column definitions
- Core columns (examples and meanings):
  - ID: genus, species, and individual ID (e.g., 'C.multiflora 1001')
  - Date, Time: measurement timestamp (GMT)
  - A: photosynthesis rate (µmol m⁻² s⁻¹)
  - Ci: internal leaf CO₂ concentration (µmol mol⁻¹)
  - gsw: stomatal conductance (mmol m⁻² s⁻¹)
  - Tleaf: leaf temperature (°C)
  - RH: relative humidity (%)
  - Qin: incident light in cuvette (µmol m⁻² s⁻¹)
  - Patm: chamber pressure (kPa)
  - Vcmax25, VcmaxTg: Vcmax at 25°C and growth temperature
  - Jmax25, JmaxTg: Jmax at 25°C and growth temperature
  - Rdark25, RdarkTg: Rdark at 25°C and growth temperature
- Quality notes: initial dataset includes 147 individuals; 144 retained after quality checks; 9 Jmax values excluded due to fitting issues.

## Experimental design and sites
- Three experimental sites at different altitudes with mean annual temperatures (MAT): high (~2516 m, ~14°C MAT), mid (~1357 m, ~22°C MAT), low (~736 m, ~26°C MAT).
- Layout: plants organized in plots with six blocks per plot; 15 plants per block; four plots per site (~90 plants per site). Eight species represented, totaling 123 individuals measured.
- Common soils and irrigation provided to maintain uniform moisture.
- Plants propagated from seed for two years in nursery at mid-elevation before planting in late 2018.

## Data collection and processing

### A-Ci data
- Collected with a LI-6800 portable photosynthesis system.
- Cuvette conditions: 29°C, 65% RH, 410 ppm CO₂; gs ≥ 0.05 mol m⁻² s⁻¹; eight ambient CO₂ concentrations (Ca: 410, 300, 175, 60, 410, 800, 1500, 2000) at saturating PPFD tailored per species.
- A-Ci curves stored in MontaneAcclim-ACiData2019.csv.

### Vcmax and Jmax data
- Derived by fitting A-Ci data to the Farquhar et al. (1980) model using the plantarophys R package (Duursma 2015).
- Fitting with fitacis: include measured Rdark, use site-specific Patm, and compare default nonlinear fit with bilinear fallback when needed.
- Quality control: curves with poor fits or Rubisco-limited Jmax excluded; 144 of 147 individuals retained; 9 Jmax values excluded.
- Temperature corrections: Vcmax and Jmax converted to 25°C and to site MAT using a temperature response function with Ea, ΔS, and Hd parameters (values from Kumarathunge et al. 2019).

### Rdark data
- Rdark measured after A-Ci in dark-adapted leaves (foil-wrapped) using LI-6800 at 5 s intervals for 1 minute between 15:00–16:00; mean of 12 values used.
- Rdark adjusted to measurement temperature and corrected to 25°C and site MAT using an exponential Q10 model.
- Rdark data stored in RdarkData_ColombianAndes_2019.csv.

## Data processing and quality control
- Curve fitting and extraction of Vcmax and Jmax performed in R; quality checks applied; unsuitable curves re-fitted with alternative methods.
- Final dataset comprises corrected Vcmax/Jmax values and Rdark values aligned to each site’s temperature context.
- All three data files accompany the study: MontaneAcclim-ACiData2019.csv, VcmaxJmaxData_ColombianAndes_2019.csv, RdarkData_ColombianAndes_2019.csv.

## Temperature corrections and equations
- Vcmax and Jmax corrected to 25°C and to site MAT using an Arrhenius-type relationship with Ea, ΔS, and Hd (parameters drawn from Kumarathunge et al. 2019).
- Rdark corrected using a fixed Q10 temperature dependence:
  - Rd(T) = Rd(Tref) × Q10^((T − Tref)/10)
  - Q10 itself modeled as Q10 = 3.09 − 0.043 Tg, where Tg is the MAT at study sites.

## Data availability and references
- Data files are provided alongside the study:
  - MontaneAcclim-ACiData2019.csv
  - VcmaxJmaxData_ColombianAndes_2019.csv
  - RdarkData_ColombianAndes_2019.csv
- Key references: Duursma (2015), Farquhar et al. (1980), Kumarathunge et al. (2019), Scafaro et al. (2017), Tjoelker et al. (2001), R Core Team (2022).

## Reusability and access
- Aims to increase dataset value by integrating with other environmental datasets and enabling access to underlying data.
- Data are stored and intended for upload to appropriate data portals; standardised methods used to facilitate cross-study comparisons and time-series monitoring of environmental health indicators.

## Notes and caveats
- Some data missing due to instrument error or quality filtering; corrective processing retained 144 of 147 individuals, with 9 Jmax values excluded.
- The dataset focuses on eight mid-successional Andean tropical montane forest species under a gradient of thermal environments, enabling assessment of thermal acclimation in photosynthesis-related traits.