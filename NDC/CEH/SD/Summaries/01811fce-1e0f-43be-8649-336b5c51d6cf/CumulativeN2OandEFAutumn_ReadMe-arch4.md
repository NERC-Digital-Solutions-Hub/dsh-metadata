# ReadMe file for CumulativeN2OandEFAutumn.csv

- Purpose: Describes a dataset measuring cumulative N2O emissions and N2O-N emission factors (EF) from different urine treatments applied to a humic gleysol in a grazing area in Snowdonia, UK. Randomised block design.

- Location and context: Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).

- Treatments and design:
  - Control: no urine application
  - ArtUrine: artificial sheep urine
  - Urine: real sheep urine
  - Additional treatment references include a nitrate and glucose treatment context for N and C inputs
  - Experimental design: randomised block

- Nitrogen application rates:
  - Artificial urine: 1120 kg N ha-1
  - Nitrate treatment: 106 kg N ha-1
  - Glucose treatment: 213 kg C ha-1

- Data and calculations:
  - Cumulative N2O emissions are calculated from the area under the curve of each replicate chamber, using trapezoidal integration from treatment application onward.
  - EF (N2O-N emission factor) is calculated as the percentage of total N applied that is released as N2O-N, with corrections for chamber areas not covered by the treatment because artificial urine was applied in discrete patches within the chamber.

- Data handling and quality assurance:
  - Data were visually checked for errors.
  - Authors must be acknowledged if data are reused or reproduced.

- Data fields (headers) and meanings:
  - Treatment: 'Control', 'ArtUrine', or 'Urine'
  - Chamber: chamber number from which N2O emissions were measured
  - Cum_N2O: cumulative N2O emissions for each chamber (micrograms N2O-N over 118 days)
  - EF: N2O-N emission factor as a percentage of total N applied

- Implications for data use and governance (for data leaders):
  - Clear link between treatments, measurement units, and derived EF supports reproducibility and comparison across studies.
  - Requires provenance and attribution due to reuse policies; ensure metadata captures treatment, chamber, time window (118 days), and calculation method.
  - Documentation notes a specific post-processing step (area-based correction for patches) that is essential for accurate EF interpretation.
  - Potential enhancements for data stewardship: confirm and extend metadata (e.g., exact dates, chamber volumes, area coverage, measurement apparatus) to improve discoverability and interoperability.