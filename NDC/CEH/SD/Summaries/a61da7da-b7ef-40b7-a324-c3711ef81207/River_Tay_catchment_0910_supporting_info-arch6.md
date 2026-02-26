# Sampling regime

## Overview
- Monthly sampling of water from the River Tay and its tributaries to assess chemical composition and greenhouse gas concentrations.
- Study period: February 2009 to December 2010.
- Nine sampling sites chosen based on existing SEPA flow gauging and water sampling sites.

## Sampling design and field collection
- Headspace technique used to determine dissolved CH4, CO2, and N2O. For each sample:
  - Three 60 ml syringes collect 40 ml of river water from 10 cm below the surface and 20 ml ambient air added.
  - Syringes shaken underwater for 1 minute to equilibrate headspace with water temperature.
  - Headspace gas injected into pre-evacuated 12 ml gas-tight vials for GC analysis.
- Additional ambient atmosphere sample collected; water temperature and atmospheric pressure recorded.
- On-site water sampling:
  - 1 L bottle collected from the main water stream at the river edge using an extension pole.
  - On-site filtration through pre-combusted (500°C for 10 h) Whatman GF/F 0.7 µm filters (47 mm).
  - Filtrates stored at 5°C until analysis.

## Laboratory analytical methods
- GHG analysis:
  - CH4 and N2O measured on HP5890 Series II GC with electron capture detector (ECD) and flame ionisation detector (FID).
  - CO2 measured on a separate HP5890 GC.
  - Reported accuracies: N2O ≈ 30 ppb; CH4 ≈ 70 ppb.
  - Dissolved gas concentrations calculated from headspace measurements using Bunsen solubility (CH4; Wiesenburg & Guinasso 1979) and Weiss & Price (1980) for CO2 and N2O.
  - Gas saturation values calculated as the ratio of dissolved concentration to the equilibrium water concentration.
- Organic and inorganic carbon:
  - DOC and TDC measured with a PPM LABTOC analyser using ultraviolet oxidation and infrared gas analysis.
  - DIC derived from TDC minus DOC.
  - Instrument calibration accuracy ≈ 1% of calibration standard concentration.
- Nitrogen species:
  - TDN, NO3-, NH4+ measured with Skalar San Plus automated flow analyser using standard colorimetric methods.
  - NO3-: copper/cadmium reduction and sulphanilamide/NEDD reaction (red/purple) at 540 nm.
  - TDN: oxidation/digestion with peroxodisulfate and UV digestion.
  - NH4+: hypochlorite reaction forming chloroamine, then nitroprusside/salicylate to yield an idophenol dye measured at 640 nm.

## Data types, units, and formatting
- Units (as detailed in Table 1):
  - Temperature: °C
  - N2O-N: µg/L
  - CH4-C: µg/L
  - CO2-C: mg/L
  - NO3-N: mg/L
  - NH4-N: mg/L
  - TDN-N: mg/L
  - DON-N: mg/L
  - DOC: mg/L
  - TDC: mg/L
  - DIC: mg/L
  - CO2 Sat: %
  - CH4 Sat: %
  - N2O Sat: %
- Data reporting:
  - Missing values marked with an asterisk in the CSV output.
  - All data reported to two decimal places.
- Data outputs:
  - Concentrations of dissolved gases (CH4, CO2, N2O) and their saturations.
  - DOC, TDC, DIC (via DIC = TDC − DOC), and TDN-related species (NO3-, NH4+, DON-N) data.