# Brief description of the dataset

- Hourly physical and nutrient monitoring data of the River Enborne near Brimpton (National grid reference SU568648)
- Time period: November 2009 to February 2012
- Parameters: total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen, pH, chlorophyll
- Accompanying hourly averaged flow data from the Environment Agency (EA) gauging station at the same site

## Overview

- Dataset provides high-frequency water quality and flow measurements for a rural lowland river system
- Includes detailed instrumentation and method descriptions to support reproducibility and data reuse
- Cross-validated TRP and nitrate data with laboratory analyses cited in related publications

## Data collection and instrumentation

- Instruments and setup
  - Micromac C automated nutrient analyser (Systea S.p.A.) for TRP
  - YSI 6600 sonde for in situ measurements (DO, pH, temperature, conductivity, turbidity, chlorophyll)
  - Nitratax Plus probe (Hach Lange) for nitrate
  - All instruments housed in an insulated shed ~2 m from the riverbank
- Sampling and flow handling
  - Water pumped from river intake ~1 m from riverbank; intermittent pumping to minimize sediment resuspension
  - Flow-through arrangement: water processed through two cells for TRP and other analyses
- TRP measurement details
  - Colorimetry using phosphomolybdenum blue (Murphy and Riley, 1962)
  - Detection limit: 0.025 mg P L^-1
  - Daily check standard; manual recalibration when reagents changed (fortnightly)
  - TRP data cross-checked with laboratory analysis (Seal AA3)
  - No 06:00:00 GMT sample for TRP (check standard measurement timing)
- Nitrate measurement details
  - Nitratax Plus uses UV absorption with 210 nm measurement and 350 nm reference
  - Detection limit: 0.07 mg N L^-1
  - Cross-checked with weekly laboratory Ion Chromatography analyses
- YSI 6600 measurements
  - Advantages: Hourly in situ data for DO, pH, temperature, conductivity, turbidity, chlorophyll
  - Turbidity: corrected for temperature; optical interference from sediment acknowledged
  - Chlorophyll: measured by fluorometer (470 nm) and reported as μg L^-1; interference accounted for in analysis
  - Calibration: performed every 2–3 weeks by EA staff

## Measurements and quality control

- Turbidity
  - Measured via light scattering at 830–890 nm; NTU units; temperature compensation applied
- Chlorophyll
  - Reported as total chlorophyll (a, b, c); corrected for turbidity interference
- Data validation
  - Cross-checks against laboratory analyses for TRP and nitrate
  - Quality control records tied to calibration/maintenance events
- Data gaps and limitations
  - Missing data indicated by NaN
  - 06:00:00 GMT TRP sample intentionally absent due to standard measurement timing

## Data format and variables

- Time format: day/month/year hour:minute
- Flow data: 15-minute flow measurements, averaged to hourly values; units in cubic metres per second (m^3/s)
- TRP: concentration of phosphorus (unfiltered sample; dissolved and acid-extractable particulate)
- Nitrate: concentration of NO3 per litre (mg N L^-1)
- Turbidity: nephelometric turbidity units (NTU)
- Other YSI-derived variables: DO, pH, temperature, conductivity, chlorophyll (μg L^-1)

## Data provenance, validation, and governance

- Provenance
  - Data collected at a single field site with multiple calibrated instruments and documented procedures
  - Cross-referenced with laboratory analyses and published studies (Bowes et al. 2015; Halliday et al. 2014; Wade et al. 2012)
- Quality assurance
  - Regular calibration/maintenance; instrument checks linked to reagent changes and standard solutions
  - Independent laboratory verification of TRP and nitrate data
- Metadata and documentation
  - Detailed methodological description enables reproducibility and interoperability
  - References provided for supporting data and context

## Data availability and access

- Dataset includes both in situ hourly measurements and accompanying hourly flow data
- Documentation outlines measurement methods and quality checks to support data reuse and integration into broader datasets
- Potential considerations for data reuse
  - Instrument-specific calibration details may be needed for cross-dataset comparisons
  - Temporal coverage ends February 2012; users should note any gaps during the study period

## References

- Bowes MJ, et al. Characterising phosphorus and nitrate inputs to a rural river using high-frequency concentration-flow relationships. Science of The Total Environment, 2015
- Halliday S, et al. The Water Quality of the River Enborne, UK: Observations from High-Frequency Monitoring in a Rural, Lowland River System. Water, 2014
- Wade AJ, et al. Hydrochemical processes in lowland rivers: insights from in situ, high-resolution monitoring. Hydrology and Earth System Sciences, 2012