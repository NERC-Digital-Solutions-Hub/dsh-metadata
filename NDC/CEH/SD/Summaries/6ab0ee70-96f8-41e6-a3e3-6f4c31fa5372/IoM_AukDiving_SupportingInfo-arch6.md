# Dive times and depths of auk (Atlantic puffin, common guillemot and razorbill) from the Isle of May outside the seabird breeding season

## Summary at a glance
- Dataset of dive times (start/end) and maximum dive depths for three auk species from the Isle of May, Scotland.
- Species and sampling windows:
  - Atlantic puffin: 19 July 2008 – 3 December 2008
  - Common guillemot: 20 July 2005 – 28 January 2006
  - Razorbill: 1 July 2008 – 24 January 2009
- Sample sizes: 12 puffins, 13 guillemots, 13 razorbills.
- Data collection used time-depth recorders (TDRs) attached to Darvic leg-rings; two TDR models were used across species.
- Output format: a single CSV file, IoM_AukDiving.csv, with seven columns describing species, sex, sampling rate, deployment ID, start/end times, and dive depth.

## Dataset scope and provenance
- Location: Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W).
- Target subjects: Atlantic puffins (Fratercula arctica), common guillemots (Uria aalge), razorbills (Alca torda).
- Data collection context: captured chick-rearing adults during the breeding season; TDRs deployed and later removed upon recapture.
- Sexing: feather samples collected for sexing using CHD I genes.
- Processing: data processed by Ruth Dunn; access supported by Scottish Natural Heritage.

## Data collection methods and instrumentation
- TDR types:
  - Puffins and razorbills: G5 TDRs (CEFAS, Lowestoft, UK).
  - Guillemots: LT2400 TDRs (Lotek Wireless, Canada).
- Deployment: attachment taken less than 5 minutes.
- Sampling strategy: designed to record over extended nonbreeding periods but constrained by device failures and memory limits.
- Original aim vs reality: intended to cover July–April; many devices failed or stopped collecting over autumn, reducing the number of contributing individuals over time.
- Recording schedules used to balance resolution and duration (memory limits) with four schemes across species, described below.

## Sampling schemes and data structure
- Guillemots: two schemes
  - 16 s sampling at 24 h periods every 30 days (n = 9 retrieved)
  - 32 s sampling at 24 h periods every 15 days (n = 4 retrieved)
- Puffins and razorbills: two schemes
  - 3 s sampling at 24 h periods every 10 days (puffins n = 6; razorbills n = 7)
  - 30 s sampling at 24 h periods every day (puffins n = 6; razorbills n = 6)
- Rationale: two sampling rates per species to balance depth-resolution with usable recording duration given memory constraints.

## Data file and column definitions
- File: IoM_AukDiving.csv
- Columns (7):
  - Species
  - Sex
  - SamplingRate (seconds)
  - DepID (unique deployment identifier per individual)
  - StartTime (start of each dive; format: Y-M-D H:M:S)
  - EndTime (end of each dive; format: Y-M-D H:M:S)
  - DiveDepth (maximum depth during the dive; meters)

## Data quality and caveats
- Data gaps due to TDR failures reduced the number of individuals contributing over time.
- Multiple sampling schemes may affect cross-species comparability and temporal coverage.
- The dataset reflects nonbreeding-season activity, with original aims broader but constrained by equipment and field conditions.
- Times are provided with explicit timestamps; no explicit time zone noted, consistent with local field timing.