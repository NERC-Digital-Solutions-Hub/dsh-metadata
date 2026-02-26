# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Blelham Tarn 1945 to 2013.

## Overview
- Long-term monitoring dataset from Blelham Tarn, Cumbria, England, covering surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.
- Timeframe for the available data: 1945–2013 (with some variables starting earlier); data were collected since 1945 and subsequently by CEH and its predecessor Institute of Freshwater Ecology since 1989.
- Initial data collection by the Freshwater Biological Association; current stewardship by CEH.
- Data are provided with specific units per variable (e.g., TEMP in °C, OXYG in % air-saturation, SECC in m, ALKA in µg CaCO3 per litre, pH, nutrient concentrations in µg per litre, TOCA in µg per litre).

## Sampling regime and collection methods
- Sampling frequency: weekly to fortnightly.
- Depth integration: water samples integrated from 0 to 5 m.
- Measurement location: from a boat at a marked buoy in the deepest part of the lake; if the buoy was inaccessible, samples were taken from the shore (Flag 2).
- Timeframe for data collection: April 1945 to end of 2013.
- Variables collected include surface temperature, surface oxygen saturation, Secchi depth, alkalinity, pH, ammonium, nitrate, soluble reactive phosphate, total phosphorus, dissolved reactive silicon, and phytoplankton chlorophyll a.

## Quality control
- The dataset comprises raw data that have not been quality controlled or calibrated (except for double entries from 2005 onwards).
- Visual checks have been performed.
- Notable gap: data missing between March and July 2001 due to an outbreak of foot-and-mouth disease restricting lake access.

## Data structure
- Delivered as a comma-separated values (CSV) file with columns including:
  - sdate: Date of measurement.
  - variable, Description: Name and description of each variable (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - value, Description: Measured values for each variable.
  - sign_if_LT_LOD, Description: Indicator if a value is below detection limit (a < sign).
  - flag, Description: Indicates sampling location (1 = buoy; 2 = shore when buoy sampling was not possible).

## Recent usage and publications
- The dataset has been used in multiple studies, illustrating its value for understanding lake chemistry, phytoplankton dynamics, and related processes. Examples include:
  - Bernhardt, Elliott & Jones (2008) on phytoplankton responses to changing lake conditions.
  - Feuchtmayr et al. (2012) on spring phytoplankton phenology across lakes in the same region.
  - Foley et al. (2012) on long-term oxygen depletion related to climate change and eutrophication.
  - Maberly et al. (2013) on catchment productivity and CO2 emissions from lakes.
  - Wang et al. (2016) and Woolway et al. (2016) on lake carbon and climate-related topics.

## Relevance for monitoring frameworks (alignment with the Authors of Monitoring Frameworks archetype)
- Demonstrates the value of long-term, multi-parameter environmental health monitoring for policy scrutinies and future decision-making.
- Highlights practical data governance considerations:
  - Availability of raw data with minimal processing, underscoring the need for quality assurance and calibration in monitored datasets.
  - Inclusion of explicit metadata-like fields (e.g., sampling location flag, detection-limit indicator) to support data provenance and usability.
  - Documentation of sampling regime details (frequency, depth integration, sampling location) essential for consistent interpretation and cross-dataset integration.
- Illustrates common data challenges for monitoring frameworks:
  - Data gaps due to external events (e.g., disease outbreaks) and the impact on trend analysis.
  - Occurrence of missing or below-detection-limit data requiring clear handling and communication.
  - Potential data accessibility barriers tied to data sharing and metadata completeness, reinforcing the need for transparent data governance and open data standards.
- Provides a concrete example of structuring and disseminating environmental health data (CSV with explicit variable descriptions and flags), supporting standardized reporting, stakeholder communication, and evidence-based policy development.