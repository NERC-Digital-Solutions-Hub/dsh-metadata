# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from Derwent Water 1990 to 2013

## Purpose and scope
- Long-term, fortnightly monitoring dataset from Derwent Water, Cumbria, England.
- Covers 0 to 5 m integrated water samples from August 1990 to end of 2013.
- Variables span physical, chemical, and biological indicators relevant to freshwater environmental health.

## Variables and units
- Surface temperature (TEMP): degrees Celsius
- Surface oxygen saturation (OXYG): % air-saturation
- Secchi depth (SECC): metres
- Alkalinity (ALKA): µg CaCO3 per litre
- pH (PH): unitless
- Ammonium (NH4N): µg N per litre
- Nitrate (NO3N): µg N per litre
- Soluble reactive phosphate (PO4P): µg P per litre
- Total phosphorus (TOTP): µg P per litre
- Dissolved reactive silicon (SIO2): µg per litre
- Phytoplankton chlorophyll a (TOCA): µg per litre

## Sampling regime and collection methods
- Sampling frequency: fortnightly.
- Measurement location: on the lake at a marked buoy (deepest part); when not possible, samples from shore (Flag 2).
- Water samples are integrated from 0 to 5 m depth.
- Data provided as raw measurements (no calibration/quality control beyond visual checks for most years).

## Data quality and status
- Raw data not quality controlled or calibrated (except for some double entries from 2005 onwards).
- Visually checked; some data gaps exist (e.g., March–June 2001 due to foot-and-mouth outbreak; limited data in 2009 due to weather).

## Data structure and availability
- Format: comma-separated values (CSV) with:
  - Date: measurement date
  - Variable, Description: variable name and description
  - Value, Description: measured value
  - Sign_if_LT_LOD, Description: indicates if below detection limit (<)
  - Flag, Description: 1 = buoy location, 2 = shore sampling
- Dataset accessible for download; raw, not yet quality controlled/calibrated.

## Data considerations for analysis
- Below-detection values marked with a "<" symbol; interpret with appropriate censoring.
- Gaps and non-shore samples may affect time-series continuity; account for sampling location differences when analyzing trends.
- Requires subsequent quality control and calibration for formal policyReporting or inter-dataset comparisons.

## Recent example publications using this dataset
- The impact of climate change on the physical characteristics of the larger lakes in the English Lake District (George, Hurley & Hewitt, 2007).
- Catchment productivity controls CO2 emissions from lakes (Maberly et al., 2013).
- Fisheries on the edge in Cumbria, UK: where salmonids, cyprinids and climate change collide (Winfield et al., 2006).
- Long-term case histories of ruffe introductions to UK lakes (Winfield et al., 2007).
- Conservation of vendace in the UK (Winfield et al., 2012).
- Reappearance of vendace in Bassenthwaite Lake amidst multiple stressors (Winfield et al., 2017).
- Lake surface temperatures (Woolway et al., 2016). 

## Data stewardship and usage in monitoring
- Demonstrates a long-running, standardized data stream suitable for tracking environmental health and informing policy over time.
- Geared toward analysts who verify, quality-control, and transform data, then present outputs (reports, maps, charts) and store datasets in appropriate portals.