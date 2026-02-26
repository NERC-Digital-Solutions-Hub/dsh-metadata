# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Esthwaite Water 1945 to 2013

## Purpose and scope
- Long-term monitoring dataset for Esthwaite Water (Cumbria, England) covering surface temperature, surface oxygen, Secchi depth, water alkalinity, pH, and key nutrients and phytoplankton chlorophyll a from 1945–2013 (some variables earlier or later).
- Sampling frequency ranges from weekly to fortnightly; samples are integrated from 0 to 5 m when possible.
- Data collected by Freshwater Biological Association originally, then CEH and predecessors since 1989.
- Measurements are provided in consistent units and include a mixture of physical, chemical, and biological indicators.

## Variables and units
- Surface temperature (TEMP): degrees Celsius
- Surface oxygen saturation (OXYG): % air-saturation
- Secchi depth (SECC): metres
- Alkalinity (ALKA): µg CaCO3 per litre
- pH (PH)
- Ammonium (NH4N): µg N per litre
- Nitrate (NO3N): µg N per litre
- Soluble reactive phosphate (PO4P): µg P per litre
- Total phosphorus (TOTP): µg P per litre
- Dissolved reactive silicon (SIO2): µg per litre
- Phytoplankton chlorophyll a (TOCA): µg per litre

## Data structure and accessibility
- Data provided as comma-separated values (CSV) with columns: sdate (measurement date), variable, value, sign_if_LT_LOD (below detection limit indicator), flag (sampling location: buoy=1, shore=2).
- Variables are represented by two fields: variable name and value; sign_if_LT_LOD indicates detection-limit status.
- Data from 1945–2013; initial data are raw and uncalibrated, with limited QC.

## Quality, metadata, and caveats
- Data are raw (not quality controlled or calibrated) except for double entries from 2005 onward, and have only visual quality checks.
- Metadata gaps exist; interpretation of detection limits and sampling location relies on the accompanying flag and sign fields.
- When buoy access was not possible, samples were taken from shore (Flag 2), affecting spatial representativeness and integration consistency.

## Data governance, sharing, and stewardship
- Underlying data are shared outputs used in published research, but full public sharing of all metadata and calibration steps may present barriers.
- Original data custodians include the Freshwater Biological Association and CEH; clear provenance is provided.
- Emphasis on documenting data governance, ensuring openness of data and methods, and maintaining standards for storage, sharing, and updates.

## Relevance for Monitoring Frameworks
- Demonstrates a long-term, multi-parameter lake monitoring dataset with physical, chemical, and biological indicators suitable for trend analysis and policy evaluation.
- Highlights practical issues in monitoring data governance: raw data status, need for QC, metadata completeness, and sharing constraints.
- Shows integration of diverse data types (in situ measurements, water chemistry, nutrient and chlorophyll indicators) and the importance of consistent sampling depth and location (buoy vs shore).

## Lessons and recommendations for framework development
- Establish robust QC/QA workflows to calibrate and validate historical and future measurements.
- Prioritize comprehensive metadata capture (sampling method, depth, location, detection limits, QC steps) to reduce barriers to data reuse.
- Implement clear data governance: open data sharing, versioning, and provenance tracking from collection to publication.
- Standardize units and provide clear documentation for variable definitions to enable cross-dataset integration.
- Plan for handling spatial inconsistencies (e.g., buoy vs shore samples) in analysis and reporting.
- Leverage existing usage in publications to validate indicators and to demonstrate the dataset’s utility for understanding nutrient dynamics, phytoplankton responses, and climate-related changes.