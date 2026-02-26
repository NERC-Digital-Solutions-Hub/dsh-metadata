# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2021

## Executive overview
- Purpose: assess potential NH3 emissions impact on Ballynahone Bog peatland; transect sampling across Ballynahone National Park (ASSI/SAC and Ramsar site) managed by Ulster Wildlife Trust (UWT).
- Data providers: local site operator duties by UWT; analysis by UK Centre for Ecology and Hydrology Edinburgh (UKCEH).
- Timeframe and method: monthly exposure of UKCEH ALPHA® passive samplers in 2021; replicate samplers used for reliability.
- Output: final dataset UWT_Ballynahone_Bog_Data_2021.csv with ammonia concentrations (µg NH3 m-3) and quality/flagging information; site metadata included.

## Data collection scope
- Transect across Ballynahone Bog within Ballynahone National Park (ASSI/SAC, Ramsar).
- Eight sampling sites: Ballynahone bog_1 through bog_8.
- Start dates for sites: 01/09/2014; ongoing data collection.
- Sampler height: ~1.5 meters above ground.
- Monthly measurement cycle: each sampler exposed for one month.

## Methodology
- Instrument: CEH ALPHA® passive samplers with citric acid-coated filters; PTFE membrane protects the filter.
- Deployment: replicate samplers mounted on shelters on poles; exposed with membrane facing downward.
- Analysis workflow: exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 (colorimetric method).
- Concentration conversion: results converted to ambient air concentration using the uptake rate of 0.003241315 m3 hr-1 and exposure duration.
- Data quality considerations: some samples were invalid due to incorrect exposure or weather; flagged accordingly.

## Data quality and validation
- Quality rules applied to 2021 data:
  - CV rule: coefficient of variation across replicates must be <15%; otherwise evaluation/discarding applied; valid measurements flagged as 103.
  - Missing samplers: coded as -9999.00 and marked invalid (-1).
  - Duration deviations: sampling durations longer/shorter than normal are flagged.
  - Local contamination/influences: notes used to discard non-representative samples; final values are averages of remaining replicates.
- Output flags: final dataset includes data status codes (Validity_id: 1 = valid, -1 = not valid; Data capture percentage; verification status).
- EMEP data status: embedded EMEP flags describe data capture, validity, and reasonings (e.g., detection limits, sampling period, contamination, etc.).
- Notes: some data were excluded from deposition estimation due to weather or other issues; remaining data are retained with appropriate flags.

## Dataset structure and contents
- File name: UWT_Ballynahone_Bog_Data_2021.csv (final accepted data values with flags).
- Core structure: one row per site per month with fields including:
  - Site name, unique site identifier, network_id (BE)
  - Parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times
  - Measurement (ammonia concentration; units: µg NH3 m-3)
  - Less-than flag (below detection limit indicator)
  - Verification id (Not verified / Preliminary verified / Verified)
  - Unit id (24 = µg NH3 m-3)
  - Data capture (%)
  - Validity_id (1 = valid, -1 = not valid)
  - EMEP code (data status and flags)
  - Month-Year (mm-yy)
- Data notes: concentrations are averages over the exposure period; some entries flagged or excluded based on quality rules.

## Site information
- Ballynahone bog_1 to bog_8:
  - Start date: 01/09/2014; End date: Ongoing
  - Coordinates:
    - bog_1: 54.82223827, -6.67860685
    - bog_2: 54.82303694, -6.67686906
    - bog_3: 54.82331637, -6.67530382
    - bog_4: 54.82396942, -6.67339952
    - bog_5: 54.82446239, -6.67000651
    - bog_6: 54.82514962, -6.67946104
    - bog_7: 54.82165647, -6.67468906
    - bog_8: 54.81616104, -6.65596700
  - Height of air inlet above ground: 1.5 m
- These sites comprise the measurement transect within Ballynahone Bog.

## Data governance, accessibility, and stewardship
- Responsible parties: Ulster Wildlife Trust (data collection and site operations) and UKCEH Edinburgh (data analysis and methodology).
- Data management emphasis: clear metadata, standardized quality flags, and documented data capture and validity criteria to support reuse and integration with wider data ecosystems.
- Reuse considerations: users should heed validity and data capture flags; consider replication, sampling period consistency, and potential local contamination when interpreting results.