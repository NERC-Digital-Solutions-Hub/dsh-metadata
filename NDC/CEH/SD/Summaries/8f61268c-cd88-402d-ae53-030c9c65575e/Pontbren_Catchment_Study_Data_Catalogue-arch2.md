# Introduction to the Database Catalogue

- Purpose: Describes the Pontbren Database, including instrumentation, data structure, quality assurance, and descriptive metadata to support consistent environmental monitoring and policy evaluation over time.
- Goal for analysts: Enable data verification, cleaning, transformation, and sharing; support reproducible analyses across multiple environmental variables and sites; promote data reuse through documented instrumentation, schedules, calibrations, and QA codes.

## Data Organization and Framework

- Data files are organized into directories; most data are .txt files, typically split into six-month blocks (January–June and July–December).
- Each data point includes a quality assurance (QA) code when available; QA details are provided in Appendices.
- Documents reference instrument locations and site layouts (e.g., Pontbren study site, Bowl study site, tree shelterbelt).

## Data Types and Site Coverage

- Automatic Weather Station (AWS) data from Bowl site: high-frequency sensors (1-minute samples; 1–10 minute averages; daily max/min, wind, soil temp, humidity, air temp, net radiation); sensor changes after 2009.
- Bowl runoff and soil water tension: weir-box and tipping bucket runoff measurements; units in litres per second; evaporation can affect readings; sampling frequency varied over time.
- Groundwater: five boreholes at Hillslope; Diver pressure transducers with barometric correction; water height relative to soil surface and temperature; 10–30 minute sampling intervals (changes in 2006).
- Hillslope runoff and soil tension: tree shelterbelt hillslope data; overland and drain runoff; tensiometers at 10, 30, 50 cm; central data logging; layout documented.
- Llyn Hir: tensiometer arrays at 10, 30, 50 cm; sampling frequency adjusted (10–15 minutes) in 2009.
- Land use manipulation plots: Ungrazed, Trees, Grazed treatments; replicates; tensiometer depths and overland flow data by replicate; detailed plot layouts provided.
- Neutron probe soil moisture: profile measurements (10 cm to 120 cm); calibration equation y = α(Soil_count / Water_count) + β (α ≈ 0.96, β ≈ -0.01) with peat-aware notes.
- Rain gauges: tipping bucket and storage gauges; site locations referenced in figures.
- Field diaries: qualitative monitoring notes highlighting data quality concerns.
- Streamflow: multiple sites using Starflow ADCPs or weirs; calibration against manual measurements; low-flow data excluded from calibration.

## Calibration and Site-Specific Details

- Starflow calibration: site-specific linear relationships linking Starflow estimates to manual measurements; parameters α*, β* and their uncertainties provided per site.
- Neutron probe calibration: moisture content derived from counts using clay-specific calibration; peat and soil composition notes may modify parameters.

## Appendices and Metadata

- Appendix A: Quality assurance coding system; codes describe data quality status (e.g., good, questionable, calibration issues, logger faults) and site-/equipment-specific fault codes.
- Appendix B: Groundwater borehole logs; drilling methods, equipment, water levels, diameters, casing, and datum references.
- Appendix C: Neutron probe access tube logs; locations and access details.

## Practical Implications for Analysts

- Provides a comprehensive, standardized catalogue enabling verification, cleaning, transformation, and integration across variables and sites.
- Supports reproducible analysis through documented instrumentation, schedules, calibration approaches, and QA codes.
- Facilitates data reuse and sharing by detailing folder structures, file naming conventions, and location metadata, with explicit QA metadata and calibration parameters for key measurements.

## Challenges and Opportunities

- Key challenges include increasing the value of datasets by combining them with other relevant data and enabling access to underlying data used to create outputs.