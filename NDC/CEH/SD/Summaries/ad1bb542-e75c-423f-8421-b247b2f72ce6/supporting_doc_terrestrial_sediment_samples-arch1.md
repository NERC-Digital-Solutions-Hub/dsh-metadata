# Collection, generation methods and quality control

- Scope and sampling design
  - Terrestrial sediment samples collected at seven sites across the Harehill and Swineshaw Moors stream network, Stalybridge, Tameside.
  - Sites: Near Harehill (Site 1), Far Harehill (Site 2), Lower Iron Tongue (Site 3), Middle Iron Tongue (Site 4), Upper Iron Tongue (Site 5), Higher Swineshaw (Site 6), Iron Tongue Hill (Site 7).
  - Method: Time Integrated Mass Samplers (TIMS). Samplers removed from uprights, contents emptied into 5-L containers; sampling interval chosen to accumulate sufficient sediment mass.
  - Sample handling: Stored cold (<4 °C) for four days; supernatant siphoned off carefully without disturbing sediment; sediment dried at 40 °C; total sediment mass recorded.

- Laboratory analyses and QA/QC
  - Geochemistry: X-ray fluorescence (XRF) using XEPOS 3 Energydispersive XRF; Pd and Co excitation radiation; helium atmosphere; high-resolution silicon drift detector.
  - Calibration and accuracy: Daily standardization with 18 certified reference materials; accuracies routinely verified.
  - Organic content correction: Loss-on-ignition (LOI) by heating to 105 °C to remove moisture, then 450 °C for 4.5 h to combust organics.
  - Particle size: Measured by Coulter LS 13 320 Laser Diffraction Particle Size Analyzer (0.375–2000 μm).
    - Sample prep: Organic component digested with H2O2; dispersion with Na6O18P6; sonication during measurement.
    - Replicates: Three repeats per sample; outliers removed to reduce intra-sample noise.
  - Data accuracy: Regular calibration checks for the instrument.

- Data structure, units and variables
  - Sample metadata: sample_id; location (sampling location).
  - Elemental analysis: reported as mg/g for elements (e.g., Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, V, Fe, Cu, Ge, Br, Y, Mo, In, Te, Ba, Hf, Hg, Na2O, Al2O3, K2O, CaCO3, Rh, Cr, Co, Zn, As, Rb, Zr, Ag, Sn, I, La, W, Pb, MgO, SiO2, Fe2O3, Tc, Pd, Mn, Ni, Ga, Se, Sr, Nb, Cd, Sb, Cs, Ce, Au, U, P2O5, Ru, Ta, Th).
  - Elemental ratios: Fe/Mn, Si/Al, Zr/K, Zr/Ti.
  - Particle size: median diameter (d50) with units in mm.
  - LOI: reported as percentage (%) [lOi].
  - Data flags and limitations: Missing values shown as blanks; values below detection limit indicated with a preceding "<".
  - Data handling notes: LOI corrections for organic content applied; standard grain-size statistics computed using Folk and Ward (1957) with Gradistat 8.0 (Blott & Pye, 2001).

- Important methodological details
  - Sample processing ensured that <0.5% of total sediment mass remained in supernatant.
  - LOI and organic corrections are integrated into elemental interpretations.
  - Particle-size statistics are based on three repeats with outlier elimination to improve precision.
  - Data provenance maintained through links to sampling sites, procedures, and calibration materials.

- References for methodology
  - Blott, S.J. & Pye, K. (2001). Gradistat: grain size distribution and statistics package.
  - Boyle, J.F., Chiverrell, R.C., Schillereff, D. (2015). Water content correction and calibration for μXRF core scanning.
  - Folk, R.L. & Ward, W.C. (1957). Significance of grain size parameters.
  - Phillips, J.M., Russell, M.A., Walling, D.E. (2000). Time-integrated sampling of fluvial suspended sediment.