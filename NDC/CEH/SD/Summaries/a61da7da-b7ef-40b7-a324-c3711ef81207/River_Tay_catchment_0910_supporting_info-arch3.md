# Sampling regime

- Objective: Monitor chemical and greenhouse gas concentrations in river water to inform environmental health insights and potential policy or management decisions.
- Study scope: Monthly sampling from February 2009 to December 2010 at nine sites along the River Tay and its tributaries, selected based on existing SEPA flow gauging and sampling sites.

## Sampling design

- Sites located where SEPA already conducts flow gauging and sampling.
- Focus on dissolved CH4, CO2, and N2O concentrations, alongside general water chemistry.

## Sample collection methods

- Headspace technique used to determine dissolved CH4, CO2, and N2O.
  - For each sample: 40 ml of river water equilibrated with 20 ml ambient air in a 60 ml syringe; shaken underwater for 1 minute.
  - Headspace gas collected in pre-evacuated 12 ml gas-tight vials for GC analysis.
  - An ambient air sample collected; water temperature and atmospheric pressure recorded.
- On-site water sampling for complementary analyses:
  - Main water stream collected in a 1 L plastic bottle from 0 to 10 cm depth at the river edge.
  - On-site filtration through pre-combusted 0.7 µm filter paper; filtered sub-samples stored at 5 °C until analysis.
- Temperature measurement: Water temperature at each site using a Hydrolab Quanta Probe.

## Analytical methods

- GHG analysis:
  - CH4 and N2O measured using HP5890 Series II GC with electron capture detector (ECD) and flame ionisation detector (FID).
  - CO2 measured on a separate HP5890 GC.
  - Reported accuracy: ~30 ppb for N2O, ~70 ppb for CH4.
- Calculations:
  - Dissolved gas concentrations derived from headspace measurements using Bunsen solubility relationships (Wiesenburg & Guinasso 1979; Weiss & Price 1980).
  - Gas saturation values computed as the ratio of dissolved concentration to equilibrium water concentration.
- Dissolved inorganic and organic carbon:
  - DOC and TDC measured with a PPM LABTOC analyser using ultraviolet oxidation and infrared gas analysis.
  - DIC calculated as the difference between TDC and DOC.
  - Instrument accuracy ~1% of calibration standard concentration (three-point calibration before each run).
- Nutrients and nitrogen species:
  - TDN, NO3-, and NH4+ analysed with a Skalar San Plus automated flow analyser using standard colorimetric methods.
  - NO3-: copper/cadmium reduction with sulphanilamide/NEDD reaction and absorbance at 540 nm.
  - TDN: oxidation/digestion by peroxodisulfate/UV digestion.
  - NH4+: hypochlorite reaction forming chloroamine, then dye formation measured at 640 nm.
- Data handling: Missing values labeled with an asterisk in the CSV; data reported to two decimal places.

## Data and units

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
- CO2 Sat, CH4 Sat, N2O Sat: %
- Table 1 provides the detailed units for each data column.
- Data handling note: Missing values clearly marked; dataset includes unit specifications.

## References

- Kling et al. 1991; Hope et al. 2004; Billett et al. 2008 (headspace method context)
- Wiesenburg & Guinasso 1979; Weiss & Price 1980 (solubility calculations)
- Billett & Moore 2008; Hope et al. 2004 (gas supersaturation context)