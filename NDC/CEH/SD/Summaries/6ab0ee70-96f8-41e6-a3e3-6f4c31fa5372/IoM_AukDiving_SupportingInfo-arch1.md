# Dive times and depths of auk (Atlantic puffin, common guillemot and razorbill) from the Isle of May outside the seabird breeding season

## Overview
- Dataset of dive start times, dive end times, and maximum dive depths for three auk species (Atlantic puffin, common guillemot, razorbill) from the Isle of May, Scotland.
- Focus on periods outside the seabird breeding season.

## Data collection and methods
- Subjects: chick-rearing adults captured at the breeding site during the breeding season.
- Tagging: time-depth recorders (TDRs) attached to Darvic leg-rings; removal occurred when recaptured in the following breeding season.
- Devices and sampling:
  - Puffins and razorbills: G5 TDRs (31 × 8 mm) used for some deployments.
  - Guillemots: LT2400 TDRs (36 × 11 mm) used for those deployments.
  - Attachment time: < 5 minutes.
- Sexing: birds sexed using two CHD I genes from 3–5 tail feathers collected at retrieval.
- Data collection timing: intended to cover the full nonbreeding period (July–April) but data gaps occurred due to TDR failures over autumn.
- Sampling regimes (to balance depth resolution with recording duration):
  - Guillemots: depth readings every 16 s for 24 h every 30 days (n = 9 retrieved birds) and every 15 days (n = 4) at 32 s intervals.
  - Razorbills and puffins: depth readings every 3 s for 24 h every 10 days (n = 7 razorbills, n = 6 puffins) or every day (n = 6 razorbills, n = 6 puffins) at 30 s.
- Key personnel and provenance: Scottish Natural Heritage facilitated access; data collected by Sarah Wanless, Mike Harris, and Francis Daunt; data processed by Ruth Dunn.

## Data structure and content
- Dataset file: IoM_AukDiving.csv
- Columns (7):
  - Species
  - Sex
  - SamplingRate (seconds)
  - DepID (unique deployment ID per individual)
  - StartTime (dive start, format Y-M-D H:M:S)
  - EndTime (dive end, format Y-M-D H:M:S)
  - DiveDepth (maximum depth per dive, in meters)

## Timeframe and sample sizes
- Atlantic puffin: 19 July 2008 – 3 December 2008 (12 individuals)
- Common guillemot: 20 July 2005 – 28 January 2006 (13 individuals)
- Razorbill: 1 July 2008 – 24 January 2009 (13 individuals)

## Data quality, limitations, and challenges
- Some TDRs failed during autumn, reducing the number of individuals contributing data over time.
- Original aim was full nonbreeding-period coverage; practical gaps due to device failures.
- Data are limited to periods outside the seabird breeding season; nonbreeding data may be incomplete for certain individuals.
- Variation in sampling rates and device types across species, potentially affecting cross-species comparability.

## Provenance and access
- Location: Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W)
- Access and project coordination: Scottish Natural Heritage; data collection and processing by listed researchers.
- Data availability: provided as IoM_AukDiving.csv with metadata described above.