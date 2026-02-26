# Supporting information for Ammonia measurements from passive samplers at Ballynahone Bog field site (2014 - 2017)

- Objective and site context
  - Measurements collected along a transect of Ballynahone National Park, an ASSI/SAC and Ramsar site in Northern Ireland.
  - Managed by Ulster Wildlife Trust (UWT); concern that local poultry installations may affect ammonia (NH3) levels in this peatland ecosystem.
  - Field operations by UWT; analysis performed by the Centre for Ecology and Hydrology Edinburgh (CEH).

- Sampling design and measurement method
  - Instrument: CEH ALPHA® passive samplers using citric acid coated filters to capture NH3, protected by a white PTFE membrane.
  - Deployment: replicates of samplers mounted at ~1.5 m height on shelters, along a bog transect; exposed in monthly cycles.
  - Analysis: samplers extracted into deionised water; AMFIA (Ammonia Flow Injection Analysis) used to determine NH3 concentration via conductivity.
  - Calibration: concentrations converted to average air concentrations using sampler uptake rate 0.003241315 m3 h-1 and exposure duration.
  - Data coverage: intended to be monthly; some samples were invalid due to weather, misexposure, or other issues (flagged in data).

- Data quality control and flagging
  - Quality rules applied to raw data:
    - Coefficient of variation (CV) of replicates: CV < 15% advised; if >15%, data are evaluated; valid data may be flagged as 103.
    - Missing samplers: coded as -9999.00 and invalid (-1).
    - Abnormal exposure duration: longer/shorter than usual monthly cycle flagged.
    - Local contamination or influences: notes used to discard non-representative samples; final value is the average of remaining results.
  - Final dataset: UWT_Ballynahone_Bog_Data_Sep_2014-Dec_2017.csv, including accepted values with appropriate flags.
  - Data status indicators and flags (including EMEP codes) accompany each entry, describing data capture percentage, validity, verification status, detection limit status, and specific data issues (e.g., contamination, sampling period deviations, low CV, etc.).

- Dataset structure and content
  - Each row corresponds to one month of data for a single site.
  - Key fields:
    - Site name; network_id (UWT); parameter_id (alpha_NH3_g)
    - Measurement period: start and end dates and times
    - Ammonia concentration: value in µg NH3 m-3
    - Detection/qualifier flags: less than detection limit, verification status, data capture percentage, validity flag, EMEP status
    - Month-Year label (MMM-YY)
  - Data capture and quality status are recorded via EMEP flags and site-specific notes.

- Data and site information
  - Site list and coordinates (start_date 01/09/2014; ongoing at time of reporting):
    - Ballynahone bog_1 to Ballynahone bog_8 with precise latitude/longitude (approx. 54.82–54.83 N, -6.67 to -6.65 W) and 1.5 m air-inlet height.
  - Data coverage spans 2014 through 2017 (with ongoing status at last update).

- Practical use and accessibility
  - Data are prepared to be discoverable via portals with metadata; dataset describes measurement periods, site identifiers, and quality flags to support reliable interpretation.
  - The study was conducted to monitor potential ammonia deposition/air concentrations along the bog transect, informing local management and broader ammonia exposure assessments.

- Additional notes
  - Figures referenced (e.g., sampler design and deployment) are described but not included in the text.
  - Data quality and interpretation rely on replication, proper exposure timing, and careful consideration of flagged observations (e.g., contamination, sampling period deviations, detection-limit considerations).