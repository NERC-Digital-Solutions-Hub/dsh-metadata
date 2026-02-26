# Supporting information for Traits data from trees exposed to a 50% reducing in canopy throughfall for 14 years in Caxiuanã, Brazil, September to October 2016

- Experimental context
  - Data come from the Caxiuanã through-fall exclusion (TFE) experiment in eastern Amazonia, with two plots: a 1 ha through-fall exclusion plot (excludes 50% canopy throughfall since 2002) and a 1 ha control plot.
  - Sampling occurred in Sep–Oct 2016 (peak dry season).
  - 176 trees were sampled across both plots (86 control, 90 TFE), representing 14 genera and 31 species; efforts aimed to capture size classes and canopy light environments.

- Traits measured (14 traits; overview of descriptions and units)
  - Plot and tree metadata: Plot (Control or Drought/TFE), Species, DBH, Tree Light Score.
  - Photosynthesis and leaf traits: Vcmax (μmol CO2 m-2 s-1), Jmax (μmol CO2 m-2 s-1), Rleaf (μmol CO2 m-2 s-1), Min gs (mmol CO2 m-2 s-1), Max gs (mmol CO2 m-2 s-1), LMA (g m-2), Nleaf (g g-1), Pleaf (g g-1).
  - Hydraulic and water relations: Ψpd (MPa), Ψmd (MPa), P50 (MPa), Ks_max (mol H2O m MPa-1 s-1 m-2), PLC (%), SMp50 (MPa).
  - Stem and structural traits: Rstem (μmol CO2 m-2 s-1), r (g cm-3), LA:SA.
  - Additional notes: A table lists all trait names, descriptions, and units (Table 1 in the document).

- Trait sampling and branch allocation
  - For each tree, three branches were collected daily:
    - Branch 1: from sunlit upper canopy to measure Ψpd; then rehydrated and used for P50 via pneumatic method after re-cutting underwater.
    - Branch 2: used for A–Ci curves to derive Vcmax and Jmax; also used for leaf gas exchange to obtain Rleaf, Min gs, and Max gs.
    - Branch 3: ≥2 m long for Ψmd measurements; used to estimate Ks_max and PLC from hydraulic measurements; leaves scanned for LA:SA.

- Measurement protocols and instruments
  - Photosynthetic traits:
    - A–Ci curves measured with Li-Cor 6400 under specified CO2 levels (400, 200, 75, 400, 800, 1200, 2000 ppm) with PAR ~1500 µmol m-2 s-1 and ~28 °C.
    - Vcmax and Jmax derived using Sharkey et al. (2007) equations and temperature-corrected to 25 °C.
  - Leaf respiration and stomatal conductance:
    - Rleaf measured at 400 ppm CO2, zero PAR, ~28 °C; corrected to 25 °C.
    - Min gs and Max gs determined from the A–Ci curves and the Rleaf measurement.
  - Leaf morphology and chemistry:
    - LMA determined via scanning and drying; Nleaf by Kjeldahl; Pleaf by spectrophotometry.
  - Hydraulic traits:
    - Ψpd and Ψmd measured with a plant pressure chamber.
    - P50 estimated from vulnerability curves using the pneumatic method after controlled dehydration.
    - Ksmax and PLC derived from measurements on central woody segments; embolism removal performed to obtain Ks and Ksmax; PLC calculated as percent difference.
  - Wood and stem traits:
    - Ks and Ksmax measured on long sections to minimize open-vessel artefacts; wood density P determined by drying mass and water displacement volume.
  - Growth:
    - Growth rates calculated from mean stem increments measured quarterly since 2010–2016 (dendrometers).

- Quality control and data processing
  - Vcmax and Jmax temperature-corrected to 25 °C; curves fitted using optimization routines in R (e.g., Sharkey et al. 2007 framework).
  - P50 derived from sigmoid fit to vulnerability curves (percentage air discharge vs leaf Ψ).
  - Ks and Ksmax measurements include checks to avoid open-vessel artefacts; measurements on longer segments (> two times vessel length) to reflect true conductivity.
  - Rstem calculated from CO2 slope in a closed-loop chamber with temperature corrections; linear slopes with r^2 < 0.98 discarded.
  - Data processing and methods are supported by extensive references (Rowland et al. and colleagues, plus methodological papers on plant hydraulics and gas exchange).

- Data provenance and governance considerations
  - This document constitutes supporting information for the broader Traits dataset from a long-term drought experiment, enabling traceability of measurements, methods, and units.
  - Key metadata to capture for data stewardship: plot type (control vs. TFE), species, DBH, tree light score, sampling dates, instruments used, measurement protocols, QC criteria (e.g., r^2 thresholds), and the references underpinning the methods.
  - The data are linked to published work and prior methodological studies, supporting reproducibility and future reuse across datasets with similar throughfall-exclusion experiments or tropical forest hydraulics measurements.

- Practical implications for data access and reuse
  - The dataset provides calibrated physiological, hydraulic, and structural trait values across two contrasting water availability environments, enabling comparative analyses of drought responses in tropical trees.
  - Suitable for integration with other datasets using consistent trait definitions (e.g., Vcmax, Jmax, P50, Ks, PLC, LMA, Nleaf, Pleaf) and standardized units.
  - beinformed by rigorous field and lab protocols facilitates data quality assessment and interoperability with similar trait datasets.