# Collection, generation methods and quality control

## Overview
- Terrestrial sediment samples were collected at seven sites across Harehill and Swineshaw Moors, Stalybridge, using Time Integrated Mass Samplers (TIMS).
- Samples were processed to produce dry, mass-measured material for subsequent analyses.
- A multi-method data workflow was employed to generate elemental composition, particle size distributions, and organic content data for data products and exploration.

## Sampling sites
- Near Harehill, Site 1, OS Grid SD 99831 01404
- Far Harehill, Site 2, OS Grid SE 00026 01261
- Lower Iron Tongue, Site 3, OS Grid SE 00289 01645
- Middle Iron Tongue, Site 4, OS Grid SE 00625 01096
- Upper Iron Tongue, Site 5, OS Grid SE 00430 01004
- Higher Swineshaw, Site 6, OS Grid SK 00911 99937
- Iron Tongue Hill, Site 7, OS Grid SE 01184 00155

## Sample collection and preparation
- TIMS samplers removed from river bed uprights and contents emptied into 5-L containers.
- Sampling interval ensured sufficient sediment mass; samples settled in cold storage (<4 °C) for four days.
- Supernatant siphoned off (<0.5% of total mass) with care not to disturb sediment.
- Sediment rinsed from container, dried at 40 °C, and weighed for subsequent analysis.

## Analytical methods

### Elemental analysis (XRF)
- Instrument: XEPOS 3 Energy-dispersive XRF; analysis under He atmosphere with Pd and Co excitation.
- Sample preparation: light grinding, pressing; standardization performed daily; accuracy checked with 18 certified reference materials.
- Organic correction: LOI used to adjust for organic content, determined by drying at 105 °C overnight and combusting at 450 °C for 4.5 hours.
- Reported units: elemental concentrations in mg/g.
- Data captured: broad suite of elements (including Na, Mg, Al, Si, P, S, Cl, K, Ca, Ti, Fe, Mn, Ni, Cr, Co, Zn, Sr, Zr, Y, etc.) and oxide forms (e.g., Na2O, Al2O3, K2O, CaCO3, SiO2, Fe2O3, etc.).

### Particle size analysis (laser granulometry)
- Instrument: Coulter LS 13 320 SingleWavelength Laser Diffraction Particle Size Analyzer.
- Sample preparation: organic matter removed with H2O2; dispersed in Na6O18P6; sonicated.
- Replicates: results are the average of three repeats with outliers removed to minimize intra-sample noise.
- Size range: 0.375–2000 μm.
- Output metric: median particle size (D50) reported in millimeters.
- Calibration: regular checks with samples of known size distributions.

## Data structure, units and recording conventions
- Data schema includes:
  - Sample id (sample_id)
  - Sampling location (location)
  - Elemental analysis variables (element in mg/g)
  - Elemental oxide forms (e.g., Na2O, Al2O3, K2O, CaCO3, SiO2, Fe2O3, etc.)
  - Elemental ratios (e.g., Fe/Mn, Si/Al, Zr/K, Zr/Ti)
  - Median particle size (D50 in mm)
  - Loss on Ignition (LOI in %)
- Missing values are shown as blanks; values below detection limits are preceded by a '<' sign (e.g., <0.6).
- Notes contain element-specific details and clarifications as needed; structure supports self-service data exploration and integration with related datasets.

## Quality control and references
- Daily calibration and validation of XRF measurements against certified reference materials.
- LOI corrections applied to account for organic content in samples.
- Triplicate measurements for particle size with outlier exclusion to improve precision.
- References informing methods and data processing include Gradistat for grain-size statistics and μXRF core-scanning calibration approaches.