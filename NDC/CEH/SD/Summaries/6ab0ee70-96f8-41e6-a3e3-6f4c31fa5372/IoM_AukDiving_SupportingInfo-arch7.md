# Dive times and depths of auk (Atlantic puffin, common guillemot and razorbill) from the Isle of May outside the seabird breeding season

## Overview
- Dataset of dive times (start and end) and maximum depths for three auk species: Atlantic puffins (Fratercula arctica), common guillemots (Uria aalge), and razorbills (Alca torda).
- Location: Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W), outside seabird breeding season.
- Sampling periods by species:
  - Atlantic puffin: 19 July 2008 – 3 December 2008
  - Common guillemot: 20 July 2005 – 28 January 2006
  - Razorbill: 1 July 2008 – 24 January 2009
- Sample sizes: 12 puffins, 13 common guillemots, 13 razorbills.

## Data collection and methods
- Birds captured as chick-rearing adults during the breeding season; time-depth recorders (TDRs) fitted to Darvic leg-rings. 
- TDR models used: G5 TDRs for puffins and razorbills; LT2400 TDRs for common guillemots.
- Attachment time: <5 minutes; birds recaptured during the breeding season to remove TDRs.
- Data collection intended to span the nonbreeding period; some TDRs failed, causing participant numbers to decline over time.
- Sampling schemes to extend data collection:
  - Various configurations to balance resolution with study duration (e.g., 16 s, 32 s, 3 s, or 30 s readings over 24 h periods at different intervals).

## Data content and schema
- File: IoM_AukDiving.csv
- Columns: 
  - Species
  - Sex
  - SamplingRate (seconds)
  - DepID (unique deployment ID per individual)
  - StartTime (dive start; Y-M-D H:M:S)
  - EndTime (dive end; Y-M-D H:M:S)
  - DiveDepth (maximum depth per dive; meters)

## Study scope and data provenance
- Purpose: collect auk diving data during nonbreeding period; initial aim broader than achieved due to TDR failures.
- Data collection and processing:
  - Collectors: Scottish Natural Heritage provided access; data collected by Sarah Wanless, Mike Harris, and Francis Daunt; Ruth Dunn processed the data.
  - Biological sampling for sexing: feather collection (UK Home Office Licence) and CHD I gene analysis.
  
## Data quality and limitations for GIS use
- Incomplete time series due to TDR failures; data decline over autumn.
- Variation in sampling rates and deployment durations across individuals and species.
- Data are constrained to a single location, with temporal resolution determined by device settings.

## Potential GIS applications
- Visualize dive events and depth profiles by species and individual over time.
- Create time-enabled maps or heatmaps of diving activity, using StartTime/EndTime and DiveDepth.
- Use DepID to link dives to individuals; incorporate Sex and SamplingRate as attributes.
- Assess data coverage and gaps to plan inclusion Criteria in spatial analyses.