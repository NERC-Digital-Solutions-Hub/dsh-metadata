# Supporting information for Traits data from trees exposed to a 50% reducing in canopy throughfall for 14 years in Caxiuanã, Brazil, September to October 2016

## Overview
- Data来自 Caxiuanã through-fall exclusion (TFE) experiment in eastern Amazonia (1°43' S, 51°27' W).
- Two plots: 1 ha drought (TFE) exclusion plot since 2002 and 1 ha control plot without drought structure.
- Sampling period: September–October 2016 (peak dry season).
- 176 trees sampled (86 control, 90 TFE) across 14 genera and 31 species; aim to cover size classes and light conditions.
- 14 plant–trait measurements with plot-scale means summarized in Table 1.
- Growth data (mean stem increment 2010–2016) collected; light score from 1 (deep shade) to 5 (fully sunlit).

## Data structure and scope
- Records include: Plot, Species, DBH, Tree Light Score, and 14 measured traits.
- Traits (with units) include:
  - Vcmax (μmol CO2 m^-2 s^-1)
  - Jmax (μmol CO2 m^-2 s^-1)
  - R leaf (μmol CO2 m^-2 s^-1)
  - Min gs (mmol CO2 m^-2 s^-1)
  - Max gs (mmol CO2 m^-2 s^-1)
  - R stem (μmol CO2 m^-2 s^-1)
  - LMA (g m^-2)
  - N leaf (g g^-1)
  - P leaf (g g^-1)
  - r (branch wood density, g cm^-3)
  - Ψpd (MPa)
  - Ψmd (MPa)
  - P50 (MPa)
  - Ks_max (mol H2O m^-1 MPa^-1 s^-1 m^-2)
  - PLC (%)
  - SM p50 (Hydraulic safety margin, MPa)
  - LA:SA (leaf area to sapwood area)
- Data processing notes include temperature corrections and quality checks (see below).

## Trait-specific sampling and measurement methods
- Branch-based sampling: three branches per tree collected on separate time windows:
  - Branch 1 (04:30–06:30): Ψpd; rehydrated, used to measure hydraulic vulnerability curve and P50 via pneumatic method.
  - Branch 2 (10:00–12:00): A–Ci curves to derive Vcmax and Jmax using Li-COR 6400; leaf gas exchange measurements (R leaf, Min gs, Max gs); leaves retained for P leaf, N leaf, and LMA.
  - Branch 3 (13:00–14:00): Ψmd; used to measure ks max and PLC after embolism assessment; wood samples analyzed for Ks and PLC; LA:SA via ImageJ from scanned leaves.
- Time and conditions:
  - A–Ci curves conducted with CO2 levels: 400, 200, 75, 400, 800, 1200, 2000 ppm; PAR ≈ 1500 μmol m^-2 s^-1; leaf temperature ≈ 28 °C.
  - R leaf measured at 400 ppm, 0 PAR, ≈28 °C; corrected to 25 °C.
  - Vcmax and Jmax corrected to 25 °C using Sharkey et al. (2007) equations; g_s thresholds used to abort curves if necessary.
- Growth data: mean stem increment calculated from dendrometer readings (2010–2016); growth rate averaged across three monthly values and log-transformed.

## Data processing and standardization
- LA scanned for leaf area; LMA computed from leaf area and dry mass.
- N leaf (Kjeldahl) and P leaf (spectrophotometry) measured on dried leaf material.
- P50 derived from hydraulic vulnerability curves using the pneumatic method.
- Ks and Ks max determined from central branch sections under controlled pressure; PLC calculated as percent difference between ks and ks max.
- Wood density (P) measured from ~1 cm branch segment via water displacement after bark removal and drying.
- All measurements conducted between 08:00–17:00; data quality checks include rejecting linear CO2 slopes with R^2 < 0.98 for stem CO2 efflux; open-vessel artefact considerations addressed during hydraulic measurements.

## Data quality, limitations, and notes
- Patchy data across plots and species due to field conditions; sampling intentionally targeted representative size classes and light environments.
- Some measurements require careful interpretation due to potential open-vessel artefact; methods followed contemporary best practices with additional procedural checks.
- Data include extensive methodological detail and referenced procedures to enable replication or re-analysis.

## Data availability and references
- Comprehensive methods for each trait linked to prior work (Rowland et al., 2015–2018; Rowland et al., 2020; and methodological sources for hydraulic measurements and trait analyses).
- Table 1 enumerates all measured traits, their descriptions, and units for standardization.

## Potential data products and usage
- Cross-plot comparisons of hydraulic and photosynthetic traits under drought vs control conditions.
- Trait distribution analyses by genus/species, DBH categories, and light exposure.
- Integrated analyses combining growth, leaf chemistry, and hydraulic traits to study drought responses.
- Dashboards or pivot tables enabling end-users to explore trait patterns across trees, species, and in relation to plot treatment.