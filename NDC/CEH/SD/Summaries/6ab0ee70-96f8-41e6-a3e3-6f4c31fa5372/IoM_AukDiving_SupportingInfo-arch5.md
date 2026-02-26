# Dive times and depths of auk (Atlantic puffin, common guillemot and razorbill) from the Isle of May outside the seabird breeding season

## Overview
- Dataset of dive times (start and end) and maximum depths for three auk species from the Isle of May National Nature Reserve, Scotland, outside the seabird breeding season.
- Species: Atlantic puffin (Fratercula arctica), common guillemot (Uria aalge), razorbill (Alca torda).
- Time periods: Puffins 19 Jul 2008–3 Dec 2008; Guillemots 20 Jul 2005–28 Jan 2006; Razorbills 1 Jul 2008–24 Jan 2009.
- Sample sizes: 12 puffins, 13 guillemots, 13 razorbills.

## Data collection and provenance
- Method: captured chick-rearing adults at the breeding site and fitted time-depth recorders (TDRs) to Darvic leg-rings; attachment under 5 minutes.
- TDR models: Puffins and razorbills used G5 TDRs (31 × 8 mm); guillemots used LT2400 TDRs (36 × 11 mm).
- Biological sampling: 3–5 body feathers collected for sexing via CHD I genes under UK Home Office Licence; birds recaptured during the following breeding season to remove TDRs.
- Data processing: Ruth Dunn; access coordination by Scottish Natural Heritage; data collection led by Sarah Wanless, Mike Harris, and Francis Daunt.

## Sampling design and data scope
- Original aim aimed to cover the entire nonbreeding period (July–April), but data loss due to TDR failures reduced representativeness.
- Extended recording strategies included four sampling schemes to balance resolution and duration:
  - Scheme 1: depth every 16 s for 24 h every 30 days (guillemots, n=9);
  - Scheme 2: depth every 32 s for 24 h every 15 days (guillemots, n=4);
  - Scheme 3: depth every 3 s for 24 h every 10 days (razorbills n=7; puffins n=6);
  - Scheme 4: depth every 30 s for 24 h every day (razorbills n=6; puffins n=6).
- Two sampling rates were used per species to balance data resolution with the limited memory of the devices.

## Data structure and file format
- File: IoM_AukDiving.csv (one CSV file).
- Columns:
  - Species
  - Sex
  - SamplingRate (seconds)
  - DepID (unique deployment ID per individual)
  - StartTime (YYYY-MM-DD HH:MM:SS)
  - EndTime (YYYY-MM-DD HH:MM:SS)
  - DiveDepth (maximum depth per dive in meters)

## Data quality, limitations, and governance
- Data gaps due to TDR failures led to an incomplete picture of nonbreeding-period diving behavior.
- Variability in sampling rates and the memory constraints of TDRs affected data density and comparability across individuals and species.
- Provenance is well documented: device type, deployment IDs, timing, and depth readings are traceable; male/female assignment via genetic sexing is noted.
- Licensing and ethical approvals are in place (UK Home Office Licence for feather sampling; access by Scottish Natural Heritage).

## Access, sharing, and sustainability
- Data collection and processing involve named researchers and institutions; provenance and attribution are explicit.
- The dataset is organized for sharing as a single CSV with clear metadata in the column definitions, supporting reuse and reproducibility.
- For future use, accompanying metadata should include device type, exact sampling scheme per individual, and any data quality flags or exclusions to facilitate discovery and proper interpretation.