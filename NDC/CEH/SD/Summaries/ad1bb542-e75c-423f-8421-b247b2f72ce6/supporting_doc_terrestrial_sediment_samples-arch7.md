# Collection, generation methods and quality control

- Purpose and scope
  - Describes collection, chemical and physical analyses, and quality control for terrestrial sediment samples across seven sites in Harehill and Swineshaw Moors, Stalybridge, Tameside.
  - Data produced support map-based geochemical visualisations and spatial analysis in GIS.

- Sampling design and sample handling
  - Time Integrated Mass Samplers (TIMS) used; seven sites across the stream network.
  - Procedure: samplers removed from metal uprights, contents bagged into 5-L containers, settled in cold storage (<4 °C) for four days; supernatant siphoned off (<0.5% of total mass) without disturbing sediment.
  - Sediment dried at 40 °C; dry mass recorded.

- Site details (OS grid references)
  - Site 1: Harehill (Near Harehill) – SD 99831 01404
  - Site 2: Far Harehill – SE 00026 01261
  - Site 3: Lower Iron Tongue – SE 00289 01645
  - Site 4: Middle Iron Tongue – SE 00625 01096
  - Site 5: Upper Iron Tongue – SE 00430 01004
  - Site 6: Higher Swineshaw – SK 00911 99937
  - Site 7: Iron Tongue Hill – SE 01184 00155

- Analytical methods and data produced
  - Geochemistry: X-ray fluorescence (XRF) using XEPOS 3 energy-dispersive XRF
    - Sample preparation: light grinding, pressing; measured under He with Pd/Co excitation; silicon drift detector.
    - Calibration and accuracy: daily standardization; validated with 18 certified reference materials.
    - Corrections: Loss-on-ignition (LOI) for organic content (105 °C drying; 450 °C ignition for 4.5 h).
  - Particle size: laser granulometry (Coulter LS 13 320)
    - Pre-treatment: digestion in H2O2 to remove organics; dispersion in Na6O18P6; sonication.
    - Measurement: averages of three repeats; outliers removed.
    - Output: D50 median particle size (mm).
  - Data outputs: structured data on elemental concentrations, elemental ratios, and particle size with LOI corrections.

- Data structure, units and values
  - Sample metadata
    - sample_id: identifier
    - location: site name or descriptor
  - Elemental analysis
    - Variable: element
    - Unit: mg/g
    - Notes: includes elements such as Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, Fe, Mn, Cu, Zn, Cr, Co, Ni, etc. 
  - Elemental ratios
    - Variables: specific element-to-element ratios (e.g., Fe/Mn, Si/Al, Zr/K, Zr/Ti)
  - Particle size
    - Median particle size: d50
    - Unit: mm
  - Loss on Ignition (LOI)
    - Unit: %
  - Data completeness
    - Missing values appear as blanks
    - Lower Limit of Detection (LOD) values prefixed with "<" (e.g., <0.6)

- Quality control and standardisation
  - Instrument calibration and daily standardization for XRF; verification with certified materials.
  - LOI correction to account for organic matter.
  - Three repeats for particle size measurements with outlier elimination to reduce intra-sample noise.
  - Documentation of detection limits to support data interpretation in GIS analyses.

- GIS and data-usage considerations
  - Location coordinates and site IDs enable spatial layering of elemental concentrations, ratios, D50, and LOI.
  - Consistent units (mg/g for elemental concentrations; mm for particle size; % for LOI) facilitate cross-site comparisons and thematic mapping.
  - Detection limits and missing values should be accounted for in GIS visualisations and any derived indices or classifications.

- References (methodology sources)
  - Blott, S.J., Pye, K. (2001). Gradistat: grain size statistics.
  - Boyle, J.F., Chiverrell, R.C., Schillereff, D. (2015). μXRF core scanning corrections.
  - Folk, R.L., Ward, W.C. (1957). Grain-size parameter significance.
  - Phillips, J.M., Russell, M.A., Walling, D.E. (2000). Time-integrated sampling of fluvial suspended sediment.