# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Purpose and context
- Monitoring ammonia (NH3) in air along a transect through Ballynahone National Park, an ammonia-sensitive peatland ecosystem.
- Aimed to assess potential NH3 deposition from local poultry livestock installations.
- Local site operator: Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.

## Sampling method and analysis
- Instrument: UKCEH ALPHA® passive samplers with citric acid coated filters and PTFE membranes; deployed at ~1.5 m height.
- Setup: Replicate samplers attached to shelters on poles; monthly exposure cycles starting at the beginning of each month.
- Processing: Exposed samplers extracted into deionised water; analyzed by SEAL AA3 (colorimetric) to determine ammonia concentration.
- Conversion: Concentrations converted to ambient air concentration using uptake rate of 0.003241315 m³ h⁻¹ and exposure duration.
- Data coverage: Some samples were incorrectly exposed or lost due to weather; such data are flagged and excluded from deposition estimates.

## Data quality assurance and flags
- Final dataset: UWT_Ballynahone_Bog_Data_2021.csv containing accepted data values with flags.
- Quality rules applied to raw data:
  - CV rule: Coefficient of variation (std dev of replicates / mean of replicates) < 15% required; otherwise replicates may be discarded or data flagged as valid if representative (flag 103).
  - Missing samplers: Marked as -9999.00 and invalid (-1).
  - Measurement duration: Flags for samples lasting longer or shorter than normal cycle due to weather/staff (duration flags).
  - Local contamination/influence: Site operator notes used to discard non-representative samples; reported data are the average of remaining results.
- Data status and flags are included per row (e.g., EMEP status, validity, and data capture).

## Data structure and contents
- Each row represents one month of data for a single site; columns include:
  - Site name and unique site identifier; network_id (BE); parameter_id (alpha_NH3_g).
  - Start and end measurement dates and times (exposure period).
  - Measured ammonia concentration (µg NH3 m⁻³); less than detection indicator (1 if below detection limit 0.03 µg m⁻³, else 0).
  - Verification id (Not verified, Preliminary verified, Verified).
  - Unit id (24 = µg NH3 m⁻³).
  - Data capture percentage; Validity_id (1 = valid, -1 = not valid).
  - EMEP flag and data status code (A-J for verification flags and other data status indicators).
  - Month-Year of measurement (mmm-yy).
- Data capture and quality indicators (e.g., CV-based validation, presence of contamination flags) accompany concentration values.

## Dataset and site information
- Final dataset name: UWT_Ballynahone_Bog_Data_2021.csv.
- Site information includes eight Ballynahone bog sites (bog_1 to bog_8) with:
  - Start date: 01/09/2014; End date: Ongoing.
  - Latitude and longitude coordinates for each site.
  - Height of air inlet above ground: 1.5 m.

## Notes on usage and provenance
- Data intended to support understanding of NH3 exposure at Ballynahone Bog and potential impacts from local livestock operations.
- Operator notes and data flags provide transparency on data quality and any exclusions.
- Data structure facilitates self-serve analyses and integration with related datasets, with clear metadata on measurement period, detection status, and quality controls.