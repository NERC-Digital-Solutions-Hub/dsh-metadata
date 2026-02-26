# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2018)

- The study site is Ballynahone National Park, an ASSI/SAC and Ramsar site in Northern Ireland, sampled to assess NH3 emissions from local poultry installations affecting the peatland ecosystem.
- Local site operator: Ulster Wildlife Trust (UWT); analysis conducted by the Centre for Ecology and Hydrology, Edinburgh (CEH).

## Measurement Method
- Instrument: CEH ALPHA® passive samplers using a citric acid coated filter to capture NH3; protected by a white PTFE membrane.
- Deployment: Replicate samplers mounted on shelters at about 1.5 m above ground on poles; monthly exposure cycles.
- Analysis: Exposed samplers extracted into deionised water and analyzed with SEAL AA3 colorimetric assay to determine ammonia concentration.
- Calculation: Ambient air concentration derived from sampler ammonia concentration using uptake rate of 0.003241315 m3 h-1 and exposure duration.
- Data scope: Measurements collected along a transect through Ballynahone Bog; data recorded as monthly periods per site.

## Data Quality and QA/QC
- Some raw samples were incorrect or lost due to weather; such samples are flagged and not used for deposition estimates.
- Quality rules applied to final data:
  - CV rule: If coefficient of variation across replicates is >15%, replicates are evaluated; if deemed representative, data may be kept and flagged (valid data flag 103).
  - Missing samplers: Marked as invalid (-1) or -9999.00 where appropriate.
  - Duration deviations: Samplers left on longer/shorter than usual cycles are flagged.
  - Local contamination/influences: Site operator notes used to discard non-representative samples; final value is the average of remaining results.
- Final dataset is curated to include accepted values with appropriate flags.

## Dataset and Fields
- Final dataset name: UWT_Ballynahone_Bog_Data_2018.csv.
- Scope: Contains monthly NH3 concentration data per site with accompanying metadata and quality flags.
- Key fields (as described in the document):
  - Station name, unique site identifier, network_id (UWT), parameter_id (alpha_NH3_g)
  - Exposure start and end dates/times
  - Measured ammonia concentration (µg NH3 m-3)
  - Less-than flag (detection limit indicator)
  - Verification id (data verification status)
  - Unit id (24 = µg NH3 m-3)
  - Data capture percentage
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code and associated flags (data status codes, QC flags)
  - Month-Year (mm-yy)
- EMEP flags provide nuanced status and reasons (e.g., contamination, sampling period duration, detection/quantification limits, CV issues) to inform data usability and provenance.

## Site Information
- Ballynahone bog_1 to Ballynahone bog_8: eight sampling sites with identical start date (01/09/2014) and ongoing end date; each site includes:
  - Latitude and longitude coordinates
  - Height of air inlet above ground: 1.5 m
- Site metadata supports spatial analyses and data provenance across the transect.

## Data Governance, Availability, and Updates
- Data are produced under a collaboration between the UWT (operator) and CEH (analytical support); final data are documented with explicit QA/QC flags and metadata for discoverability.
- The dataset includes detailed flags, notes, and provenance to facilitate appropriate use, update, and interoperability with broader inventories (e.g., UK-AIR/EMEP contexts).
- Data are organized to allow ongoing updates through the same structure, with clear instructions on handling invalid or non-representative samples and how final site averages are determined.