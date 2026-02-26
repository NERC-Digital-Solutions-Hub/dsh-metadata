# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

## Objective and context
- A transect of ammonia measurements through Ballynahone National Park (ASSI/SAC, Ramsar site) in Northern Ireland.
- Initiated due to concern that Ballynahone Bog could be adversely affected by NH3 emissions from nearby poultry livestock installations.
- Local site operator: Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology (UKCEH) Edinburgh.

## Data collection and method
- Instrument: UKCEH ALPHA® passive samplers with citric acid-coated filters to capture NH3; PTFE membrane protects the filter; membrane oriented downward during exposure.
- Deployment: Replicate samplers mounted on shelters at ~1.5 m above ground; monthly exposure cycles.
- Processing: Exposed samplers extracted into deionised water; NH3 concentration determined by SEAL AA3 colorimetric analysis; results converted to average air concentration using a known uptake rate (0.0038422 m3 h-1) and exposure duration.
- Coverage: Data collected along a transect across Ballynahone Bog; site identifiers and spatial data provided.

## Data quality, QC and flags
- Final dataset: UWT_Ballynahone_Bog_Data_2022.csv with accepted values and appropriate flags.
- Quality rules applied:
  - CV of replicates < 15% to deem data valid; otherwise replicates reviewed and may be discarded; valid data flagged as 103.
  - Missing samplers assigned -9999.00 and invalid (-1).
  - Sampler duration longer or shorter than the standard monthly cycle flagged.
  - Local contamination or deviations noted; affected samples discarded as appropriate; final site data is the average of remaining results.
- Data status and flags are aligned with EMEP data flags and verification codes (including verification status and data capture indicators).

## Dataset contents and structure
- Each row represents one month of data for a single site; columns include:
  - Site name, unique site identifier, network_id (BE)
  - Parameter_id (alpha_NH3_g)
  - Measurement start/end dates and times (exposure window)
  - Ammonia concentration (µg NH3 m-3)
  - Data flags, detection status, validity, EMEP status, and related metadata
  - Month of measurement
- Data units: µg NH3 m-3 (average concentration for the exposure period)
- Summary metadata: dataset contains site names and spatial identifiers (latitude/longitude, sampling height)

## Site information and locations
- Ballynahone bog_1 to Ballynahone bog_8
  - Start date: 01/09/2014; End date: Ongoing
  - Latitude/Longitude and 1.5 m air inlet height for each site
  - Example coordinates:
    - bog_1: 54.82223827, -6.67860685
    - bog_2: 54.82303694, -6.67686906
    - bog_3: 54.82331637, -6.67530382
    - bog_4: 54.82396942, -6.67339952
    - bog_5: 54.82446239, -6.67000651
    - bog_6: 54.82514962, -6.67946104
    - bog_7: 54.82165647, -6.67468906
    - bog_8: 54.816161, -6.655967
- All sites share a uniform sampling height (1.5 m) and are part of the Ballynahone Bog transect.