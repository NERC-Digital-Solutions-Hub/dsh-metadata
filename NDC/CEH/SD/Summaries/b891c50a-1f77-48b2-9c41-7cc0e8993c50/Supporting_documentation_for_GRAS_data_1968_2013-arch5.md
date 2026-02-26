# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Grasmere 1968 to 2013

## Overview
- Long-term monitoring dataset from Grasmere, Cumbria, England, covering 1968 to 2013 for multiple aquatic variables.
- Variables include: surface temperature (TEMP), surface oxygen saturation (OXYG), Secchi depth (SECC), alkalinity (ALKA), pH, ammonium (NH4N), nitrate (NO3N), soluble reactive phosphate (PO4P), total phosphorus (TOTP), dissolved reactive silicon (SIO2), and phytoplankton chlorophyll a (TOCA).
- Data originally collected by the Freshwater Biological Association; managed by CEH and its predecessor since 1989.
- Data available for download; used in multiple recent publications.

## Sampling regime and collection methods
- Frequency: weekly to fortnightly sampling over the period, with some variables starting earlier (1968) than others.
- Sampling location: measurements taken from a boat at a marked buoy located at the deepest part of the lake; when the buoy was inaccessible, samples were taken from the shore (Flag 2).
- Water sampling: integrated from 0 to 5 meters when possible.
- Timeframe: June 1968 through end of 2013.

## Quality control and data quality
- Data are raw and have not been quality controlled or calibrated (except for double entries from 2005 onward).
- Visual checks have been performed on the data.
- Values below detection limits are indicated with a "<" in the sign_if_LT_LOD column.

## Data structure and contents
- File format: comma-separated values (CSV).
- Key columns:
  - sdate: date of measurement.
  - variable, Description: name of the measurement (e.g., TEMP, OXYG, SECC, ALKA, PH, NH4N, NO3N, PO4P, TOTP, SIO2, TOCA).
  - value, Description: measured values for each variable.
  - sign_if_LT_LOD, Description: indicates whether a value is below the detection limit (sign is "<" if applicable).
  - flag, Description: 1 = sample collected at buoy location; 2 = sample taken from shore due to buoy inaccessibility.
- Water chemistry units:
  - ALKA: µg CaCO3 per litre
  - TOCA, NH4N, NO3N, PO4P, TOTP, SIO2: µg per litre
  - TEMP: degrees Celsius
  - OXYG: % air-saturation
  - SECC: metres
  - pH: numeric pH

## Accessibility and usage notes
- Data are curated as a historical record with clear provenance: collected by FBA, then CEH and predecessors.
- The dataset has been used in peer-reviewed studies (examples include analyses of catchment productivity, long-term lake water quality trends, and biogeochemical cycling).
- Researchers should account for the raw status and the absence of full QC/calibration when integrating into analyses; plan for independent QC/normalization where needed.
- Documentation provides context for sampling methods and potential discrepancies between buoy and shore sampling occasions.

## Provenance and related publications
- Primary institutions: Freshwater Biological Association (initial collection); Centre for Ecology & Hydrology (since 1989) and predecessors.
- Recent publications using the dataset:
  - Maberly et al. (2013). Catchment productivity controls CO2 emissions from lakes. Nature Climate Change.
  - Reynolds et al. (2012). Forty years of monitoring water quality in Grasmere: effects of sewage enrichment vs hydraulic flushing on phytoplankton ecology. Freshwater Biology.
  - Wang et al. (2016). Coupling of carbon and silicon geochemical cycles in rivers and lakes. Scientific Reports.
  - Woolway et al. (2016). Lake surface temperatures in State of the Climate 2015. Bulletin of the American Meteorological Society.

## Governance considerations for Data Stewards
- Data custodians should preserve the raw data with metadata describing sampling location, depth integration, buoy vs shore sampling, and LOD indicators.
- Maintain clear versioning and provenance to support future QC and calibration work.
- Facilitate updates and disclosures of any new QC steps, calibrations, or methodological changes.
- Address potential interoperability needs due to historical sampling methodologies and occasional shore-based sampling.
- Ensure licensing and usage terms are clear when sharing and reusing the dataset, given its long-term institutional custody and multiple user communities.