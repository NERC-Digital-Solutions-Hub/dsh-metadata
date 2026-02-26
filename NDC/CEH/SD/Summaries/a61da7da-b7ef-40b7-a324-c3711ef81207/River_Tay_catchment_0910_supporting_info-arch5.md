# Sampling regime

## Overview
- Monthly sampling of water from the River Tay and its tributaries for chemical analysis and greenhouse gas (GHG) concentrations.
- Study period: February 2009 to December 2010.
- Nine sampling sites chosen based on existing SEPA flow gauging and water sampling locations.

## Sampling design and sites
- Sites selected to align with SEPA infrastructure; sampling occurred monthly over two years.
- Sampling locations cover main river and tributaries to assess chemical and GHG dynamics.

## Sample collection procedures
- Headspace method used to determine dissolved CH4, CO2, and N2O concentrations.
- For each sample:
  - Three 60 ml syringes extract 40 ml river water from 10 cm below the surface.
  - 20 ml ambient air added; syringes shaken underwater to equilibrate headspace with water.
  - Headspace gas injected into pre-evacuated 12 ml gas-tight vials for GC analysis.
  - An ambient atmosphere sample collected; water temperature and atmospheric pressure recorded.
- On-site measurements:
  - Water temperature measured with a Hydrolab Quanta Probe.
  - A 1 L water sample collected from the main stream edge, filtered on-site through pre-combusted GF/F 0.7 µm filters, and stored at 5°C until analysis.

## Laboratory analyses and calculations
- GHG analyses:
  - CH4 and N2O measured with HP5890 Series II GC (ECD and FID); CH4 accuracy ~70 ppb, N2O ~30 ppb.
  - CO2 measured on a separate HP5890 GC.
  - Dissolved gas concentrations derived from headspace measurements using Bunsen solubility relations (CH4; Wiesenburg & Guinasso, 1979; CO2 & N2O; Weiss & Price, 1980).
  - Gas saturation values calculated as the ratio of dissolved gas concentration to the equilibrium water concentration.
- Other water chemistry analyses:
  - DOC and TDC measured with PPM LABTOC analyser (UV oxidation and IR) with ~1% calibration accuracy.
  - DIC derived from TDC minus DOC.
  - TDN, NO3-, and NH4+ measured with Skalar San plus autosampler using colorimetric methods:
    - NO3-: copper/cadmium reduction and sulphanilamide/NEDD, absorbance at 540 nm.
    - TDN: oxidation/digestion with peroxodisulfate/UV digestion.
    - NH4+: hypochlorite reaction forming chloroamine, then nitroprusside/salicylate to form an idophenol dye, absorbance at 640 nm.

## Data structure, units, and quality
- Recorded values reported to two decimal places.
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
- Missing data:
  - Marked in the CSV with an asterisk; indicates incomplete records.
- Documentation:
  - See Table 1 for unit details corresponding to each CSV column.

## Data quality, availability, and provenance
- Data are presented as mean values from triplicate samples collected at each site.
- On-site filtration and immediate cooling help ensure sample integrity prior to laboratory analysis.
- Values are calculated using established solubility relationships and standard reference methods; specific reagent methods and instrument models are documented.

## Documentation and references
- References for methods include:
  - Billett & Moore (2008)
  - Hope et al. (2004)
  - Kling et al. (1991)
  - Weiss & Price (1980)
  - Wiesenburg & Guinasso (1979)
- Table 1 provides the detailed unit specifications for all reported data in the CSV file.

## Governance implications for Data Stewards
- Metadata and data lineage:
  - Ensure metadata records capture sampling design (nine sites, monthly cadence, 2009–2010), methods (headspace protocol, on-site filtration, instrument models), and calculation approaches (solubility relationships).
- Data standards and interoperability:
  - Maintain consistent units across datasets and document any unit conversions if datasets are merged with other sources.
  - Preserve the asterisk-based missing-value notation in the data catalog and data access interfaces.
- Data quality and traceability:
  - Link CSV records to detailed method descriptions, calibration schedules, and QA/QC procedures.
  - Archive raw instrument outputs where feasible and provide access to derived calculations (e.g., saturation values) with reproducible steps.
- Access and reuse:
  - Ensure clear licensing and data access terms for the dataset, given its detailed field and lab methods.
- Documentation completeness:
  - Attach or reference the full method documentation, site locations, sampling dates, and table 1 unit details to facilitate reuse by data users.