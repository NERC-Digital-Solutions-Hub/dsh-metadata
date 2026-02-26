# Laboratory soil incubation respiration rates from permafrost in subarctic Canada

## Overview
- Dataset documents laboratory incubations of soil samples to quantify gas production rates (CO2 and CH4) with depth along soil profiles.
- Samples come from three soil cores per site with three replicates; four depths per core labeled A (shallow) to D (deep).
- Sites cover diverse forest and peatland environments (FFU, FFB, BLF, WHF, TPP, TW) and include permafrost contexts, including a note on TW where layers C and D are labeled as permafrost due to peatland thaw history.
- Measurements focus on aerobic (oxic) and anaerobic (anoxic) conditions at 5°C and 15°C.

## Sampling design and metadata
- Three soil cores per site, with three replicates (columns labeled replicate).
- Depths sampled along the profile: four depths per core (A–D), with soil_depth_interval_cm indicating the exact depths.
- Layers include active layer and permafrost, with a special note for TW permafrost labeling.
- Soil preparation includes manual mixing, removal of top vegetation and large roots, and sieving to remove pebbles from mineral fractions when needed.

## Incubation conditions
- Incubations conducted under:
  - Oxic (aerobic) conditions
  - Anoxic (anaerobic) conditions (jars flushed with N2)
- Temperature treatments: 5°C and 15°C.
- Aerobic setup: 0.5 L glass jars containing soil in pots; CO2 measured at time 1 (sealing) and time 2 within 24 h (15°C) or 48 h (5°C) for specific sites (TPP and TW).
- Anaerobic setup: jars flushed with N2 at start; 30 mL headspace samples withdrawn for analysis; CO2 measured with EGM-4 and CH4 with DP-IR Detecto Pak; dilution corrections applied.

## Measurements and data processing
- Gas concentrations (CO2 and CH4) measured using:
  - CO2: EGM-4 Infrared Gas Analyzer (PP Systems)
  - CH4: DP-IR Detecto Pak
- Production rates calculated from the difference between time 1 and time 2 concentrations, assuming linear increase.
- Rates expressed as mg of C per day per gram of dry soil (for both C-CO2 and C-CH4).
- Carbon and nitrogen content reported as percent dry mass.

## Data quality, provenance, and sharing considerations
- Documentation notes the exact sampling depths, sites, and permafrost status to support reproducibility.
- Important to capture:
  - Site code, soil_layer (A–D), soil_depth_interval_cm, Permafrost flag, replicate
  - Incubation conditions (aerobic/anaerobic), temperatures (5°C, 15°C)
  - Measurement times and intervals (time 1, time 2), instruments used, dilution corrections
  - Calculated production rates and units
  - Carbon and nitrogen content if available
- Be explicit about units, measurement corrections, and any treatment-specific timing (e.g., differences in time2 measurement window for high vs. low temperature).
- Note the special labeling in TW for permafrost-related history to avoid misinterpretation of layer status.