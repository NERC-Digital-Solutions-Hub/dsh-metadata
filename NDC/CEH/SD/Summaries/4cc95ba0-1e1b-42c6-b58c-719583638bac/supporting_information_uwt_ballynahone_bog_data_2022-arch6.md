# Ammonia measurements from passive samplers at Ballynahone Bog field site, Northern Ireland, 2022

## Purpose and context
- Data collected along a transect through Ballynahone National Park (an ASSI/SAC and Ramsar site) to assess potential NH3 impacts on a sensitive peatland ecosystem.
- Local operator: Ulster Wildlife Trust (UWT); analysis conducted by UK Centre for Ecology and Hydrology Edinburgh (UKCEH).
- Motivation: investigate whether Ballynahone Bog is affected by NH3 emissions from nearby poultry livestock installations.
- Sampling design: monthly passive measurements using UKCEH ALPHA® samplers along the transect; samplers exposed at roughly 1.5 m above ground.

## Methods and data processing
- Sampler type: CEH ALPHA® passive samplers with citric acid coated filter and PTFE membrane; membrane oriented downward during exposure.
- Deployment: replicate samplers attached to a shelter on a post, at ~1.5 m height; each site has multiple replicates for robust estimation.
- Analysis workflow: exposed samplers extracted into deionised water; analyzed with SEAL AA3 colorimetric method to determine ammonia concentration.
- Calculation: ambient NH3 concentration derived from sampler concentration using a known uptake rate (0.0038422 m3 h-1) and the exposure duration.
- Data quality controls: identified and flagged questionable samples (e.g., incorrectly exposed, weather-related losses); data flagged accordingly.
- Final dataset: UWT_Ballynahone_Bog_Data_2022.csv, with one row per month per site; columns include site name, start/end dates, ammonia concentration (µg NH3 m-3), and a data flag.

## Data content and structure
- Measurements: monthly average NH3 concentrations for each site along the transect.
- Data fields include: site name, network_id, parameter_id (alpha_NH3_g), exposure start/end dates and times, measured NH3 concentration, less-than flag (detection limit), verification status, unit_id (µg NH3 m-3), data capture percentage, validity flag, and EMEP code.
- Dataset flags and status: multiple indicators used to communicate data quality and provenance (e.g., validity, data capture, verification, and EMEP-related flags).
- EMEP flags reference: standardized codes (e.g., indicating contamination, sampling period variations, detection limit issues) to support cross-system data interpretation.

## Quality, flags, and caveats
- Coefficient of variation (CV) < 15% across replicates is a criterion for validity; if CV > 15%, data are evaluated for potential discard or kept with notes; valid measurements receive a 103 flag when appropriate.
- Missing samplers: indicated by -9999.00 and marked invalid (-1).
- Duration anomalies: samplers left on too long or too short are flagged.
- Local contamination or influences: notes guide discarding non-representative samples; final site value is the average of remaining valid results.
- Some data were not suitable for deposition estimation due to incorrect exposure or weather-related losses; these are flagged and excluded from the final deposition dataset.
- Data conclusions are based on accepted data values after QA/QC and are presented with appropriate flags and metadata.

## Site information
- Ballynahone bog_1 to Ballynahone bog_8:
  - Start date: 01/09/2014; End date: ongoing.
  - Coordinates (approximate):
    - bog_1: 54.82223827, -6.67860685
    - bog_2: 54.82303694, -6.67686906
    - bog_3: 54.82331637, -6.67530382
    - bog_4: 54.82396942, -6.67339952
    - bog_5: 54.82446239, -6.67000651
    - bog_6: 54.82514962, -6.67946104
    - bog_7: 54.82165647, -6.67468906
    - bog_8: 54.81616100, -6.65596700
  - Height of air inlet above ground: 1.5 m for all sites.

## Data product and access notes
- Primary data product: UWT_Ballynahone_Bog_Data_2022.csv (accepted data values with appropriate flags).
- Units: micrograms of NH3 per cubic meter of air (µg NH3 m-3).
- Data provenance: measurements collected by UWT, analyzed by UKCEH Edinburgh; dataset includes detailed metadata on sampling dates, site identifiers, and quality flags.
- Intended use: supports assessment of ammonia exposure across the transect and informing potential management or policy considerations; compatible with standard QA/QC and EMEP flag interpretations for broader data integration.