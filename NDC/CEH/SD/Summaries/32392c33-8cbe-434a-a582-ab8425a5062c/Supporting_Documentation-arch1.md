# Water quality data - work packages 3 and 5

- The dataset comprises water quality observations relevant to work packages 3 and 5, stored primarily in Water_quality_data.csv, with supporting metadata in Sampling_sites.csv, Determinand_list.csv, and methodology guidance in Particulate_matter_method.rtf.

## Data files and structure

- Water_quality_data.csv
  - Contains a single main data file with measurements and metadata.
  - First five columns:
    - SiteRef: Unique site code (e.g., BCN, TYC, DOL are estuarine; others are freshwater).
    - SiteName: Unique site name.
    - Trip: Identifies the field trip during which samples were collected; can indicate autosampler or manual collection; intermediate dates use a 3-digit code.
    - Date: Sampling date.
    - Time: Sampling time.
  - Remaining columns: Determinands (measured variables) with qualifiers; details are described in Determinand_list.csv.
  - Notes on data quality:
    - Some pH values were incorrect due to instrument failure over a period; original pH values are in pHUncorrected.
    - For incorrect pH values, qualifiers show the issue; approximately corrected values exist using alkalinity data.
    - The pH column mixes correct and corrected values.
    - Blank fields indicate missing data; zeros are actual measured values.

- Sampling_sites.csv
  - SiteName: Unique site name.
  - SiteRef: Unique site code.
  - Type: Fresh or Saline (freshwater vs tidal/saline conditions).
  - Sampling: Spot or Continuous sampling.
  - Easting and Northing: National Grid coordinates for each site.

- Determinand_list.csv
  - Provides details about each determinand (the measured variables) referenced in Water_quality_data.csv (mapping, units, descriptions).

- Particulate_matter_method.rtf
  - Methodology information for the analysis of certain particulates.

## Key considerations for analysis

- Data scope and structure
  - Combines site-level metadata with numerous determinands per sample.
  - Spatial distinction: estuarine (e.g., BCN, TYC, DOL) vs freshwater sites.
  - Temporal structure defined by Trip and Date/Time; intermediate samples have coded trip identifiers.

- Data quality and processing
  - pH measurements include uncorrected and corrected values; instrument failure affected a period.
  - Qualifiers indicate data quality flags; some determinations may be missing or zero-valued.
  - Corrected pH values rely on alkalinity-based adjustments; users should reference pHUncorrected for original readings.
  - Missing data are represented as blanks; interpreters should consult Determinand_list.csv for which variables were measured at each sample.

- Metadata and reproducibility
  - Determinand_list.csv provides essential context for interpreting each determinand’s unit and meaning.
  - Site coordinates enable spatial analyses and mapping.
  - Particulate matter methodology is documented separately in the provided RTF.

- Practical data integration
  - Join Water_quality_data.csv with Sampling_sites.csv on SiteRef to enrich site metadata.
  - Use Determinand_list.csv to interpret each measured variable and units.
  - Consider tide-related saline classifications (Type) when analyzing freshwater vs estuarine dynamics.

## Potential limitations

- Limited data at certain scales or local levels may affect fine-grained analyses.
- pH corrections introduce a layer of processing; cross-check with pHUncorrected when assessing raw measurements.
- Not all determinands may be present for every sample; data gaps are possible due to measurement scope or instrument status.
- Access to complete metadata and method details is essential to ensure accurate interpretation and reproducibility.