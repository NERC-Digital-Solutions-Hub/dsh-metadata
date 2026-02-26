# Dissolved Si, UNITS = µg/l.

- Overview
  - Longitudinal dataset of dissolved inorganic constituents in water, aligned to standardized environmental monitoring practices.
  - Aims to demonstrate environmental health and policy performance over time with consistent formatting and QA.
  - Data are verified, cleaned, transformed, stored, and designed for reuse and interoperability.

- Data Coverage and Scope
  - Timeframe elements include START = 15-Sep-92 and END = 04-Nov-94 for initial components; later sections reference broader periods (e.g., electrical conductivity data from 1997 to 2009).
  - Laboratory: Wallingford; Field and lab workflows applied consistently.
  - Analytes referenced include Dissolved Si and numerous other dissolved constituents (SO4, Sr, Th, U, Y, Zn, and additional elements), with units varying by analyte (e.g., µg/l, mg/l, etc.) and pH/gran alkalinity among major ions.
  - Data fields exist for each analyte (UNITS, LQDC, QUOTE TO, START/END, LAB, METHOD, Filtration, Preservation, and measured values), though many entries are placeholders indicating missing or not-reported values.

- Analytical Methods and QA
  - Filtration: 47 mm, 0.45 µm membrane in field (field measurements may vary with rain; laboratory re-analysis when required).
  - Preservation: Acidification to 1% with concentrated high-purity nitric acid; samples stored at 4°C in the dark where applicable.
  - Instrumentation:
    - ICP-OES for many elements on a PerkinElmer 3300 DV.
    - ICP-MS for select elements on a VG PlasmaQuad PQ1.
    - pH measured with a Radiometer meter/electrode.
    - Gran Alkalinity determined via Gran plots using 0.1 N H2SO4.
  - Quality assurance:
    - Data qualifiers and method quality control fields present; limits of quantification/detection (LQDC) specified per analyte where reported.
  - Data storage/portal: Datasets created and stored in the Wallingford lab portal; intended for reuse and cross-dataset integration.

- Data Structure and Quality
  - Data are field-driven and structured to support time-series analysis and policy evaluation.
  - Many fields show placeholders (".") indicating missing or unreported values for certain attributes.
  - Gran Alkalinity data accompany major ion measurements, enabling comprehensive water chemistry interpretation.

- Relevance to Analysts Monitoring the Environment
  - Demonstrates standardized data handling from verification and cleaning to storage and interoperability.
  - Provides a broad, time-resolved set of dissolved constituents enabling trend analysis, standards comparisons, and policy performance assessment.
  - Emphasizes data accessibility and the ability to integrate underlying datasets with complementary data sources.

- Practical Considerations for Use
  - Suitable for time-series analyses of dissolved silicon and co-measured dissolved constituents, with cross-analytical compatibility due to standardized filtration, preservation, and instrumentation.
  - Leverage alongside other environmental datasets to maximize dataset value via data integration (as highlighted by the challenges).
  - Pay attention to data qualifiers, LQDC values, and the presence of missing data when interpreting results.