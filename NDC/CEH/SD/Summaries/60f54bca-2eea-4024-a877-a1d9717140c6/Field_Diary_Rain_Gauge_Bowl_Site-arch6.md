# Bowl tipping bucket rain gauge

- A 0.2 mm tipping bucket rain gauge located in the bowl study area at Tyn-ybryn, above ground level. Installed on 6 April 2005. Originally known as RG3.
- Also referred to by date-stamped maintenance logs and data quality notes across 2005–2009.

## Data Quality and Issues

- Some data flagged as suspect (e.g., sheep may have damaged the tiny tag; protective trench dug).
- Periodic issues with the gauge being blocked/unblocked; calibration and rebalancing events recorded.
- Time stamp issues noted at multiple points (overlaps, GMT/BST changes, time drift between downloads); attempts to adjust data to align timestamps with actual times.
- Specific observations:
  - Feb 2005 onward: snow, wind, or other conditions causing dodgy readings.
  - Calibration windows and tips to ignore during certain times (e.g., between 13:30–14:30, calibrations checks).
  - 31/10/08: potential time stamp mismatch; data adjusted to follow on after the last record of the previous download.
- Data download and quality checks: several entries note successful reinstallation or verification that the gauge is working after adjustments.

## Maintenance and Adjustments

- Protective and structural interventions:
  - Sheep protection measures implemented (trench; later wooden stand due to pedestal collapse).
  - Wooden stand installed to address erosion and uneven base.
- Technical maintenance:
  - Rebalanced tipping bucket and calibration of tips.
  - Battery changes, seal and desiccant replacement on tinytag.
  - Periodic checks of wiring and data logger; note of a disconnected or damaged cable (needs replacement).
- Operational notes:
  - Some readings explicitly ignored during calibration checks.
  - Data labeled as “rain gauge download checked” and “working after re-installation.”

## Data Processing and Provenance

- Records indicate ongoing efforts to verify and clean data before analysis (e.g., adjusting time stamps, ignoring anomalous tips, re-installation confirmations).
- Acknowledges potential data gaps or questionable periods due to natural conditions (snow, wind) and environmental damage, with explicit attempts to separate reliable data from problematic intervals.

## Recommendations for Data Support

- Maintain a comprehensive metadata log linking each data segment to its corresponding maintenance event, calibration, or environmental disruption.
- Implement automated checks to flag time stamp inconsistencies and to annotate periods where data should be treated with caution (e.g., post-calibration windows, during repairs, or after sensor damage).
- Ensure clear documentation of when and why data are ignored or adjusted to support reproducibility and re-use.
- Consider adding a data quality flag for each reading (e.g., clean, suspect, corrected) and a predictable schema for timestamp normalization across GMT/BST transitions.