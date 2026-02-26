# Supporting information for Ammonia measurements from passive samplers at Fenn's, Whixall, Bettisfield, Wem & Cadney (2018)

## Purpose and Context
- Data originate from atmospheric ammonia monitoring with CEH ALPHA passive samplers during the Site Nitrogen Action Plan (SNAP) implementation on Fenn's Mosses, Whixall Moss, Bettisfield Moss, Wem Moss, and Cadney Mosses SAC/SSSI as part of the LIFE project.
- Local site operator duties are carried out by Natural England; analysis is conducted by CEH Lancaster with data processed by CEH Edinburgh.
- Samplers are deployed in monthly exposure cycles and aimed at informing ammonia concentration assessments for environmental management.

## Sampling and Analysis Method
- CEH ALPHA passive samplers use a citric acid–coated filter to capture NH3, protected by a white PTFE membrane, with the membrane oriented downward during exposure.
- Replicate samplers are mounted on shelters at about 1.5 m above ground to improve reliability.
- Analysis involves extracting exposed filters into deionised water and measuring ammonium colorimetrically with SEAL AA3; results are converted to average ambient NH3 concentration using a known uptake rate of 0.0028986 m3 h-1 and the exposure duration.

## Data Processing and Quality Assurance
- Raw data are quality checked with several rules:
  - CV of replicates < 15%; if >15%, replicates are reviewed; valid data are flagged as 103.
  - Missing samplers are assigned -9999.00 and flagged invalid (-1).
  - Sampler duration anomalies (long/short) are flagged when necessary.
  - Local contamination or deviations are flagged, and non-representative results may be discarded; final site data are the average of remaining valid results.
- The final dataset is named FWBWC_ammonia_measurements_2018.csv and comprises monthly measurements per site, with site names and spatial identifiers provided elsewhere in the document.

## Dataset Structure and Key Fields
- Each row represents one month’s data for a single site; columns include:
  - Site name and unique site identifier
  - Network ID
  - Parameter ID (type of measurement: alpha_NH3_g)
  - Measurement start and end dates/times (exposure window)
  - Ammonia concentration during exposure (units: µg NH3 m-3)
  - Detection/validation indicators (e.g., less-than flag for values below detection limit; verification ID; unit ID)
  - Data capture percentage
  - Validity ID (1 = valid, -1 = not valid)
  - EMEP data status code with corresponding flags
  - Month-Year of measurement (MMM-YY)
- EMEP flags provide detailed data-quality context (e.g., missing data, values below detection limits, sampling period deviations, contamination sources, CV-related flags, etc.).

## Flags, Quality Indicators, and Data Status
- Data flags indicate validity and representativeness, including:
  - 103: data considered valid after CV check
  - -1: invalid data (missing or non-representative)
  - Specific EMEP flag notes explain conditions such as contamination, near-threshold measurements, sampling period deviations, and other data quality issues
- Flagging supports downstream filtering for analysis, ensuring robust, comparable monthly NH3 concentrations.

## Site Information
- MM01, MM02, MM03:
  - Start date: 01/07/2018
  - End date: Ongoing
  - Latitude/Longitude: MM01 (52.925, -2.777), MM02 (52.932, -2.751), MM03 (52.924, -2.758)
  - Air inlet height: 1.5 m above ground

## Data Use and Metadata
- The dataset is prepared for integration into broader analyses of ammonia exposure, supports cross-site comparisons, and is designed to be discoverable with accompanying metadata and spatial identifiers.