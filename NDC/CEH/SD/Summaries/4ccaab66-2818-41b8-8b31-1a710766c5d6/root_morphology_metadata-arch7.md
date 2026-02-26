# AFEX Experiment

## Overview
- Describes the AFEX nutrient addition experiment in the Biological Dynamics of Forest Fragments Project (BDFFP/INPA) with a focus on root sampling and morphology to assess responses to nutrient treatments.
- Includes experimental design, sampling protocols, analytical methods, and data structure details.

## Location and environmental context
- Location: AFEX project area, BDFFP/INPA, ~80 km north of Manaus, Brazil (02° 25' S, 59° 43' W).
- Climate: mean air temperature ~26 °C; mean annual precipitation ~2,400 mm; relative humidity 75–92%.

## Experimental design and layout
- Design: full factorial nutrient addition with 8 treatments (control, N, P, cations, N+P, N+cations, P+cations, N+P+cations).
- Structure: 4 independent blocks; 8 plots per block; total 32 plots.
- Plot size and layout: each plot 50 m x 50 m; central measurement area 30 m x 30 m.
- Nutrient application: three times per year on the plots; rates are 125 kg ha⁻¹ yr⁻¹ N (as urea), 50 kg ha⁻¹ yr⁻¹ P (triple superphosphate), 50 kg ha⁻¹ yr⁻¹ Ca, 20 kg ha⁻¹ yr⁻¹ Mg (dolomitic limestone), and 50 kg ha⁻¹ yr⁻¹ K (potassium chloride).
- Spatial arrangement: blocks spaced at least 250 m apart; central 30 x 30 m facilites the main measurements.

## Root sampling and study period
- In each plot (n=32), five ingrowth cores (12 cm diameter, 30 cm deep) installed in August 2017 within the central 30 x 30 m area.
- Core collections every three months (by plot and soil depth: 0–10 cm and 10–30 cm; total n=64 samples).
- Focused on fine roots produced in the interval Nov 2017–Feb 2018 (middle of the wet season).
- Sampling of roots lasted 60 minutes per plot; root-free soil reinserted after collection.
- Used Michaelis-Menten asymptotic curve to extrapolate to 180 minutes for biomass estimation.

## Root processing and morphology
- Subsampling: fine roots (<2 mm) from both depths; dried at 60 °C for dry mass.
- Morphology: roots scanned at 600 dpi; analyzed with WinRHIZO to obtain mean diameter, total length, area, and volume.
- Derived traits: Specific Root Length (SRL, cm g⁻¹), Specific Root Area (SRA, cm² g⁻¹), Root Tissue Density (RTD, g cm⁻³), and mean root diameter.

## Data structure and variable metadata
- Spreadsheet fields:
  - Block: block where plots were installed (1–4).
  - Plot: block and plot identifier (Block 1–4, Plot 1–8).
  - TRT: nutrient treatment (one of 8 treatments).
  - Depth: soil layer sampled (0–10 cm; 10–30 cm).
  - root_volume: root volume (cm³).
  - tot_weight: total root dry weight (g).
  - SRL: specific root length (cm g⁻¹).
  - SRA: specific root area (cm² g⁻¹).
  - RTD: root tissue density (g cm⁻³).
  - diameter: root mean diameter (mm).

## Timeline and references
- Key dates: August 2017 (core installation); Nov 2017–Feb 2018 sampling window.
- References for methods: Araújo 2002; Metcalfe et al. 2007; Metcalfe et al. 2008.