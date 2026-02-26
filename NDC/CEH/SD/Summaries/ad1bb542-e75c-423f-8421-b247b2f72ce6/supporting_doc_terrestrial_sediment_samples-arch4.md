# Collection, generation methods and quality control

## Overview
- Describes collection, preparation, analysis, and quality-control procedures for terrestrial sediment samples from seven sites in Harehill and Swineshaw Moors, Stalybridge, UK.
- Aims to obtain geochemical (XRF) and particle-size data with robust QA/QC and clear data structure for reuse.

## Sampling and Site Details
- Time Integrated Mass Samplers (TIMS) used to collect sediment; samplers removed from metal uprights and contents emptied into 5-L containers.
- Sampling interval designed to accumulate sufficient material; samples stored cold (<4 °C) for four days before processing.
- Supernatant siphoned and discarded (<0.5% of total mass), to avoid disturbing sediment.
- Sediment dried in an oven at 40 °C; dry mass measured for further analysis.
- Seven sampling sites:
  - Near Harehill (Site 1), OS Grid SD 99831 01404
  - Far Harehill (Site 2), OS Grid SE 00026 01261
  - Lower Iron Tongue (Site 3), OS Grid SE 00289 01645
  - Middle Iron Tongue (Site 4), OS Grid SE 00625 01096
  - Upper Iron Tongue (Site 5), OS Grid SE 00430 01004
  - Higher Swineshaw (Site 6), OS Grid SK 00911 99937
  - Iron Tongue Hill (Site 7), OS Grid SE 01184 00155

## Analytical Methods
- Geochemistry: X-ray fluorescence (XRF) using XEPOS 3 Energydispersive XRF.
  - Sample prep: light grinding, pressing, analyzed in He atmosphere with Pd and Co excitation; high-resolution silicon drift detector.
  - Daily standardization with 18 certified reference materials to verify accuracy.
  - Light-element corrections for organic content via loss-on-ignition (LOI): moisture removed at 105 °C, organics combusted at 450 °C for 4.5 h.
- Particle-size analysis: Laser granulometry with Coulter LS 13 320.
  - Organic matter removed with H2O2; samples dispersed in Na6O18P6 and sonicated.
  - Three repeats per sample; outliers removed to minimize intra-sample noise.
  - Particle size statistics calculated with Folk and Ward (1957) methods using GRADISTAT 8.0; results reported as D50 (median particle size, mm).
  - Instrument calibration checks performed regularly.

## Data Structure, Nature and Units
- Data fields:
  - Sample id (sample_id)
  - Location (sampling location)
  - Elemental analysis: element (mg/g)
  - Elements listed include Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, V, Fe, Cu, Ge, Br, Y, Mo, In, Te, Ba, Hf, Hg, Na2O, Al2O3, K2O, CaCO3, Rh, Cr, Co, Zn, As, Rb, Zr, Ag, Sn, I, La, W, Pb, MgO, SiO2, Fe2O3, Tc, Pd, Mn, Ni, Ga, Se, Sr, Nb, Cd, Sb, Cs, Ce, Au, U, P2O5, Ru, Ta, Th.
  - Elemental ratios: Fe/Mn, Si/Al, Zr/K, Zr/Ti.
  - Median particle size: d50 (mm)
  - Loss On Ignition (LOI): loi (%)
- Data notes:
  - Missing values represented as blanks.
  - Values reported with “<” indicate values at the limit of detection (LOD).
- Metadata and references accompanying methods include Gradistat, LOI correction approaches, and core-scanning calibration references.

## Quality Assurance and Data Governance
- QA/QC elements:
  - Daily XRF standardization using certified references.
  - LOI corrections to account for organic content.
  - Repetition (three repeats) for particle-size measurements with outlier removal.
  - Regular instrument calibration checks to ensure data reliability.
- Data structure supports discoverability and reuse, with explicit variables, units, and detailed elemental set; includes LOD indicators and handling of missing data.

## References
- Gradistat: Blott and Pye, 2001
- XRF calibration and LOI correction approaches: Boyle, Chiverrell, Schillereff, 2015
- LOI and grain-size methodology: Folk and Ward, 1957
- Time-integrated sampling methodology: Phillips, Russell, Walling, 2000