# Supporting information for Traits data from juvenile trees exposed to a 50% reducing in canopy throughfall at the Caxiuanã drought experiment, Brazil, August to September 2017

## Overview
- Data from the Caxiuanã through-fall exclusion (TFE) experiment in eastern Amazonia, comparing a 1 ha through-fall exclusion plot (TFE) since 2002 with a 1 ha control plot.
- Sampling occurred in September–October 2017 (peak dry season): 76 trees total (43 control, 33 TFE) across common genera.
- For each tree, up to 17 functional traits were measured to assess carbon and hydraulic physiology under reduced canopy throughfall.
- Data were quality controlled and prepared for integration with other datasets; missing or non-fit values are flagged as NA.

## Experimental setup and sampling design
- Location: Eastern Amazonia, coordinates approximately 1°43' S, 51°27' W.
- Experimental plots: two 1 ha plots—Control (no drought structure) and Drought/TFE (50% canopy throughfall exclusion) operational since 2002.
- Tree selection: sampling aimed to cover different size classes (1 cm to 10 cm DBH) and include the most common genera.
- Sampling cadence: three branches collected per tree on separate days, with branches chosen to capture sunlit upper canopy or top-of-canopy conditions as appropriate.

## Traits measured and data structure
- Traits are reported per-tree with an explicit plot designation (Control or Drought plot) and species identity. A total of 17 traits were measured.
- Trait list (descriptions and units in Table 1):
  - Vcmax: Maximum carboxylation capacity (μmol CO2 m−2 s−1)
  - Jmax: Maximum electron transport capacity (μmol CO2 m−2 s−1)
  - R leaf: Leaf respiration in the dark (μmol CO2 m−2 s−1)
  - Min g s: Minimum stomatal conductance (mmol CO2 m−2 s−1)
  - LMA: Leaf mass per area (g m−2)
  - N leaf: Leaf nitrogen content (g g−1)
  - P leaf: Leaf phosphorus content (g g−1)
  - Thickness: Leaf thickness (mm)
  - ρ: Branch wood density (g cm−3)
  - Ψpd: Pre-dawn leaf water potential (MPa)
  - Ψmd: Midday leaf water potential (MPa)
  - P50: Xylem pressure for 50% loss of conductance (MPa)
  - P88: Xylem pressure for 88% loss of conductance (MPa)
  - Ksmax: Max lumen conductance (mol H2O m−1 MPa−1 s−1 m−2)
  - PLC: Percentage loss of conductivity
  - LA:SA: Leaf area to sapwood area ratio
- Data notes:
  - Values are reported per-tree, with some per-branch-derived measurements (see methods).
  - NA indicates missing or unusable data (e.g., failed curve fitting or damaged samples).
  - Data include both mean plot-scale values and per-tree measurements, with quality control removing values that could not be fitted to the required models.

## Measurements and methods (workflow)
- Branch 1 (0430–0630): Ψpd measured, then branches sealed, rehydrated (24 h), re-cut underwater for P50 via pneumatic method (Pereira et al. 2016).
- Branch 2 (1000–1200): Leaves used for A–Ci curves to derive Vcmax and Jmax; Li-COR 6400 also measured R leaf, Min gs, and Max gs; leaves dried for P leaf, N leaf, and LMA.
- Branch 3 (≥2 m, 1300–1400): Three leaves for Ψmd; branch sealed for PLC and Ksmax; 1 cm wood section used to measure ρ; LA:SA calculated from scanned leaves using ImageJ (area measurements).
- Data sources and references:
  - Primary trait descriptions and methodology summarized by Bartholomew et al. (2020) and Giles et al. (2022).
  - Specific methods for pneumatic P50 (Pereira et al. 2016) and low-cost xylem conductance measurements (Pereira & Mazzafera 2012).
  - Image analysis for LA:SA using ImageJ (Schneider et al. 2012).

## Data quality and curation
- Quality control steps:
  - Removal of data points where curves could not be fitted to the corresponding models (P50, P88, Ksmax, PLC, Vcmax, Jmax).
  - NA values used to denote data missing due to lost or damaged samples or measurement issues.
  - Remaining data checked to ensure consistency with ranges reported in related studies.
- Data provenance notes:
  - Detailed methodology available in cited literature (Bartholomew et al. 2020; Giles et al. 2022) for trait collection specifics.
  - Dataset prepared to support cross-study comparisons and integration with GIS-based analyses.

## GIS and data product considerations
- Spatial context: two defined plots (Control and Drought) within a single experimental site; suitable for mapping per-tree trait distributions and changes under reduced throughfall.
- Potential GIS applications:
  - Map per-tree trait values or plot-level summaries to visualize spatial patterns of drought response.
  - Combine with tree-size class (DBH) data and species information for habitat- or community-level analyses.
  - Link with other environmental layers (soil, microclimate) to explore drivers of hydraulic and carbon trait variation.
- Data integration notes:
  - Ensure alignment of plot-level identifiers with GIS layers representing plot boundaries and tree locations (where available).
  - Handle NA values appropriately in spatial analyses and consider imputation only with justification if needed for visualization.

## References
- Bartholomew, D. C., et al. 2020. Small tropical forest trees have a greater capacity to adjust carbon metabolism to long-term drought than large canopy trees. Plant Cell Environ. 43: 2380-2393.
- Giles, A. L., et al. 2022. Small understorey trees have greater capacity than canopy trees to adjust hydraulic traits following prolonged experimental drought in a tropical forest. Tree Physiol. 42(3): 537-556.
- Pereira, L., Bittencourt, P. R. L., Oliveira, R. S., Junior, M. B. M., Barros, F. V., Ribeiro, R. V., et al. 2016. Plant pneumatics: stem air flow is related to embolism—new perspectives on methods in plant hydraulics. New Phytol. 211: 357-370.
- Pereira, L. & Mazzafera, P. 2012. A low-cost apparatus for measuring the xylem hydraulic conductance in plants. Bragantia 71: 583-587.
- Schneider, C. A., Rasband, W. S., & Eliceiri, K. W. 2012. NIH Image to ImageJ: 25 years of image analysis. Nat Methods 9: 671-675.