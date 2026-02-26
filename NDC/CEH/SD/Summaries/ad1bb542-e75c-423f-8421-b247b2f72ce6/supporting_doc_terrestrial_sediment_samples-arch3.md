# Collection, generation methods and quality control

- Overview
  - Describes sediment collection, geochemical and particle-size analyses, and quality-control measures across seven sites in the Harehill and Swineshaw Moors stream network to support monitoring and decision-making.

- Sampling and sites
  - Seven sites: Near Harehill (Site 1), Far Harehill (Site 2), Lower Iron Tongue (Site 3), Middle Iron Tongue (Site 4), Upper Iron Tongue (Site 5), Higher Swineshaw (Site 6), Iron Tongue Hill (Site 7).
  - TIMS (Time Integrated Mass Samplers) used; samplers removed from river-bed uprights, contents emptied into 5-L containers.
  - Sediment allowed to settle in cold storage (<4 °C) for four days; supernatant (<0.5% of total mass) siphoned off; sediment dried at 40 °C; mass measured and retained.

- Analytical methods
  - Geochemistry (XRF): XEPOS 3 energy-dispersive XRF; samples ground, pressed; measured in He with Pd-Co excitation; silicon drift detector; daily standardization; 18 certified reference materials used for accuracy checks.
  - Organic correction: LOI (loss-on-ignition) by heating to 105 °C to remove moisture, then 450 °C for 4.5 hours to combust organic matter.
  - Particle size: Laser granulometry with Coulter LS 13 320; digestion with H2O2 to remove organics, dispersion in Na6O18P6, sonication; three repeats with outlier removal; results averaged; GRADISTAT 8.0 used for statistics; D50 (mm) reported; regular calibration checks performed.

- Data structure, units and values
  - Sample data: sample_id; location; elemental analysis as element (mg/g); elements include Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, Cr, Co, Zn, As, Rb, Zr, Ag, Sn, I, La, W, Pb, Mn, Ni, Ga, Se, Sr, Nb, Cd, Sb, Cs, Ce, Au, U, etc.
  - Elemental ratios: Fe/Mn, Si/Al, Zr/K, Zr/Ti.
  - Median particle size: d50 (mm).
  - LOI: LOI (%) with notes on measurement.
  - Data notes: missing values shown as blanks; values below detection limit marked with < (LOD).

- Quality assurance and control
  - Daily standardization of XEPOS 3; use of 18 certified reference materials for validation.
  - LOI corrections applied to account for organic content.
  - Repeats for particle-size measurements with elimination of outliers.
  - Regular calibration checks of the instrument.

- Outputs and interpretation
  - Provides site-specific elemental concentrations (mg/g), elemental ratios, and grain-size distribution (D50) to characterize sediment geochemistry and texture across the stream network.
  - Structure supports comparative analysis over sites and potential temporal monitoring when repeated.

- References
  - Gradistat (grain-size statistics) — Blott & Pye, 2001
  - μXRF core scanning calibration and water-content correction — Boyle, Chiverrell, Schillereff, 2015
  - Folk & Ward (grain-size parameters) — Folk & Ward, 1957
  - Time-integrated sampling methodology for fluvial suspended sediment — Phillips, Russell, Walling, 2000

- Relevance to monitoring frameworks
  - Demonstrates end-to-end data workflow: field collection, laboratory analyses, data structuring, QA/QC, and clear documentation of methods, enabling policy evaluation and decision-making.
  - Highlights data governance considerations: need for standardized metadata, transparent calibration procedures, and open sharing of underlying data to avoid data silos and improve reuse.
  - Addresses common monitoring challenges: data completeness, detection limits, and transformation needs to ensure comparability across sites and over time.