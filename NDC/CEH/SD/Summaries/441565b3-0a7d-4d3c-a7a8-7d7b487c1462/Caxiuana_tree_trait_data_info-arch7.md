# Supporting information for Traits data from trees exposed to a 50% reducing in canopy throughfall for 14 years in Caxiuanã, Brazil, September to October 2016

- Experimental site: Caxiuanã through-fall exclusion (TFE) experiment, eastern Amazonia (1°43' S, 51°27' W). Two plots of 1 hectare each: a TFE plot excluding 50% of canopy throughfall since 2002 and a control plot without drought structure.
- Sampling frame and scope: September–October 2016 (peak dry season). 176 trees sampled (86 control, 90 TFE) across different size classes (DBH from 10 cm upwards) and canopy light conditions; 14 genera and 31 species represented.
- Traits and data coverage: 17 traits measured; table provided lists trait descriptions, units, and plot-scale means.
- Data collection cadence and provenance: Branches from the same tree sampled daily (three branches per tree) to measure multiple traits; end-products include plant hydraulic, leaf, stem CO2 efflux, and wood properties. Data intended to support cross-site comparisons and GIS-based visualization of trait variation in relation to drought treatment.

## Sampling design and data captured

- Plot design and treatments: Two 1-hectare plots (Control vs Drought/TFE) with a long-term drought manipulation context.
- Tree selection and distribution: Trees spread across size classes and light environments to capture variability; 176 trees sampled across both plots.
- Growth and light characterization: Growth rates derived from dendrometers (mean stem increment 2010–2016; three-monthly measurements) and a light score (1–5) indicating canopy exposure.
- Data products: Trait measurements summarized as mean plot-scale values in Table 1.

## Traits measured (Table 1) and units

- Plot and tree identifiers: Plot (Control or Drought/TFE), Species, DBH
- Forest structure and light: Tree Light Score
- Leaf-level physiology: Vcmax (μmol CO2 m−2 s−1), Jmax (μmol CO2 m−2 s−1), R leaf (μmol CO2 m−2 s−1), Min gs (mmol CO2 m−2 s−1), Max gs (mmol CO2 m−2 s−1), LMA (g m−2), N leaf (g g−1), P leaf (g g−1), r (g cm−3)
- Plant water status and hydraulics: Ψpd (MPa), Ψmd (MPa), P50 (MPa), Ks max (mol H2O m MPa−1 s−1 m−2), PLC (percentage), SM p50
- Structural and foliar traits: LA:SA (leaf area to sapwood area)
- Stem and growth traits: R stem (μmol CO2 m−2 s−1)
- Additional notes: Table includes detailed unit descriptions and trait definitions.

## Methods and measurements by trait

- Leaf trait data (Vcmax, Jmax, R leaf, Min gs, Max gs, LMA, N leaf, P leaf)
  - Sampled from ~1 m branches excised from trees; branches placed in water and re-cut underwater.
  - Vcmax and Jmax derived from A–Ci curves using Li-COR 6400 at PAR ≈ 1500 μmol m−2 s−1 and ~28°C; CO2 concentrations included 400, 200, 75, 400, 800, 1200, 2000 ppm.
  - A–Ci curves fitted in R (optim) with Sharkey et al. (2007) equations; Vcmax and Jmax temperature-corrected to 25°C.
  - R leaf measured on a dark-leaf sample adjacent to the A–Ci leaf; corrected to 25°C.
  - LMA calculated from scanned leaf area and dry mass; N leaf by Kjeldahl method; P leaf by spectrophotometry.
  - LA:SA calculated from scanned leaf area relative to sapwood area (ImageJ used for leaf area).
- Stem CO2 efflux (R stem)
  - 213 cm3 acrylic chamber sealed on 75 cm2 sapwood area for 120–220 seconds in a closed-loop gas analyzer.
  - Linear slope used to derive R stem; measurements temperature-corrected to 25°C via a Q10 = 2.0.
- Plant hydraulic traits (Ψpd, Ψmd, ks max, PLC, P50)
  - Ψpd and Ψmd measured with a plant pressure chamber (three to four leaves per 1 m branch, sampling times 04:30–06:30 for Ψpd and 13:00–14:30 for Ψmd).
  - P50 estimated using pneumatic method after rehydration and progressive drying; sigmoid fit to percent air discharge vs leaf Ψ.
  - ks and ks max measured on ≥2 m long branch sections to minimize open-vessel artefacts; high-pressure water flow method used to estimate ks, followed by emboli removal and re-measurement of ks max.
  - PLC calculated as the percent difference between ks and ks max.
  - Wood samples were used to measure stem properties and to ensure vessel length considerations; longer samples (>2× maximum vessel length) used to better reflect in situ conductivity.
- Wood density (P)
  - From branch samples (~1 cm diameter): bark removed; dried to constant mass; volume measured by water displacement; density = dry mass / volume.

## Data processing and quality notes

- Data processing tools: A–Ci curve fitting in R (R 3.4.2); ImageJ for leaf-area measures.
- Temperature adjustments: All Vcmax/Jmax and related parameters temperature-corrected to 25°C.
- Open-vessel artefact mitigation: ks/ks max measurements designed with long vessel segments to minimize artefacts.
- Measurement window: All measurements conducted between 8 am and 5 pm.
- References and methodology provenance: Methods and data linked to Rowland et al. (various years) and supporting references (e.g., Sharkey et al. 2007; Pereira et al. 2016; Tyree 2000; Torrez-Ruiz et al. 2017; Rowland et al. 2015–2020).

## Notes and access

- The document provides extensive methodological details and references enabling replication or GIS-ready data integration for spatial analyses of trait variation under throughfall exclusion.
- Additional details and methodological context are available in Rowland et al. (2015a, 2015b, 2018, 2020) and the cited references.