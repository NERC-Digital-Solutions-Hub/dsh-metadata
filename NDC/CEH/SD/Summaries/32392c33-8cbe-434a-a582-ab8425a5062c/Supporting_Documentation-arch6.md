# Water quality data - work packages 3 and 5

- Overview
  - A dataset on water quality spanning multiple sites with data for field trips, dates, times, and multiple determinands.
  - Metadata and supporting context are provided across several files, including methodology for particulates.

- Data files and what they contain
  - Water_quality_data.csv
    - Core data table with first five columns: SiteRef (unique site code; estuarine and freshwater sites), SiteName, Trip (sampling event), Date, Time.
    - Determinand values come with qualifiers (often blank; sometimes "<"). pH values were affected by instrument issues over a period; pHUncorrected contains original values; the main pH column mixes corrected and uncorrected values; some incorrect values flagged in qualifiers with an “x”.
    - Blank fields indicate missing data; zeros are actual measured values. Other columns are described in Determinand_list.csv.
  - Sampling_sites.csv
    - SiteName, SiteRef, Type (Fresh or Saline), Sampling (Spot or Continuous), Easting, Northing.
  - Determinand_list.csv
    - Metadata describing each determinand/column present in Water_quality_data.csv.
  - Particulate_matter_method.rtf
    - Methodology information for analysis of certain particulates.
  
- Key fields and their meanings
  - SiteRef: unique site identifier; BCN, TYC, DOL are estuarine; others are freshwater.
  - Trip: identifies the field sampling event; 3-digit codes indicate intermediate dates within routine trips; blank indicates autosampler or manual sampling over 1–2 days.
  - Date/Time: timestamp for when samples were collected.
  - Determinand values: numerical results with qualifiers; qualifiers indicate data quality or detection limits (e.g., <).
  - pH handling: pHUncorrected contains original values; pH column contains a mix of correct and corrected values; incorrect pH values were flagged with x in the qualifier and approximately corrected using alkalinity.
  - Missing data: indicated by blank fields; some variables were not measured for certain samples.
  - Zeros: represent measured zeros, not missing data.
  
- Spatial and sampling context
  - Sampling_sites.csv provides geographic references (Easting/Northing) and water type (Fresh vs Saline) to account for tidal influence and sampling context.
  - Sampling type (Spot vs Continuous) and tide-related water type are available for contextual analysis.

- Data quality considerations and potential pitfalls
  - Patchy data across sites and trips; long-term instrument issues affecting pH measurements.
  - Mixed pH values (corrected and uncorrected) require careful handling depending on analysis goals.
  - Intermediate dates coded within trips may require special attention when ordering samples.
  - Outputs may require joining Water_quality_data.csv with Sampling_sites.csv and Determinand_list.csv for full interpretation.

- How to use and transform for end users (Data Support perspective)
  - Data integration: join Water_quality_data.csv with Sampling_sites.csv on SiteRef to enrich with site type, sampling method, and coordinates.
  - Interpretability: refer to Determinand_list.csv to understand each determinand’s column definitions.
  - Verification and cleaning: decide on whether to use pHUncorrected, the corrected pH, or a documented correction approach; account for qualifiers and detectability notes.
  - Analysis-ready products: create dashboards or pivot tables by SiteName/SiteRef, Trip, Date, and determinand; map sites using Easting/Northing; compare freshwater vs saline sites; examine pH trends considering instrument issues.
  - Documentation: use Particulate_matter_method.rtf for particulate data interpretation and methodology considerations.