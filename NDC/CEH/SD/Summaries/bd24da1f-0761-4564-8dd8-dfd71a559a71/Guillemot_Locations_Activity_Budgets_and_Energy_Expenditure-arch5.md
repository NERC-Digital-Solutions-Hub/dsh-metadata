# Activity data from common guillemots from the Isle of May during the 2005-2006 annual cycle

## Overview
- A multi-part dataset describing activity, location, and colony attendance for common guillemots (Uria aalge) from the Isle of May, Scotland.
- Coverage: 4 July 2005 – 21 June 2006; 13 individuals tracked.
- Data collected using biologging devices (GLS with time-depth recorders) and supplementary colony attendance observations.
- Includes derived daily activity budgets and environmental context (sea surface temperature).

## What the dataset contains
- Activity-derived data for each individual per day, including:
  - Inactive on water hours, diving hours, active on water hours, flight hours, colony presence hours, daily energy expenditure (DEE, kJ), and proportions of dive activity by time of day (twilight, day, night).
  - Sea surface temperature (SST) recorded by bird-borne loggers.
- Spatial data describing daily locations for each individual.
- Colony attendance data providing a daily density score at the colony site.

## Data collection and provenance
- Species and site: Common guillemots at the Isle of May National Nature Reserve, Scotland (56°11′N, 02°33′W).
- Methods:
  - Capture of chick-rearing adults; attachment of GLS-TDR devices (LT2400; 36 × 11 mm).
  - Recapture during the breeding season; loggers removed; body feathers collected for sexing (CHD I genes) under UK Home Office Licence.
  - Data recovery relied on re-captures; two sampling strategies due to memory limits.
- Sampling period and sample size:
  - 4 July 2005 to 21 June 2006; 13 individuals.
  - Two sampling regimes: 
    - 16 s depth readings for a 24 h period every 30 days (n = 9 loggers retrieved).
    - 32 s depth readings for a 24 h period every 15 days (n = 4 loggers retrieved).
- Data processing:
  - Derived daily budgets and activity categories from raw biologging data.
  - Colony attendance recorded via daily time-lapse photography (7 Oct 2005 – 20 May 2006).
  - Data processing performed by Ruth Dunn; access to Isle of May dataset granted by Scottish Natural Heritage (SNH).
- Data access and rights:
  - SNH granted access to the Isle of May dataset; research teams include Sarah Wanless, Mike Harris, and Francis Daunt.

## File structure and schema

- IoM_Guillemot_SST_TAB_DEE.csv
  - Columns (13): ID, Sex, Date (D-M-Y), Logger-SST (°C), Inactive_h (hours), Diving_h (hours), Active_h (hours), Flight_h (hours), Colony_h (hours), DEE (kJ), Twilight_diving (proportion), Day_diving (proportion), Night_diving (proportion)

- IoM_Guillemot_Locations.csv
  - Columns (4): ID, Date (D-M-Y), Long, Lat
  - Note: Two location estimates per day; data presented separately to reflect dual daily fixes

- IoM_Guillemot_ColonyAttendance.csv
  - Columns (2): Date (D-M-Y), Density (0–5; categorical mapping: 0 no individuals, 1 <10, 2 10–20, 3 20–50, 4 >50, 5 all ~100 breeding sites)

## Data quality, standards, and governance considerations
- Data quality and completeness:
  - Memory constraints required two sampling strategies, leading to potential irregular coverage across individuals and dates.
  - Locations are provided as two daily estimates; interpretation requires handling multiple rows per date for each individual.
- Metadata and units:
  - Dates in D-M-Y format; SST in °C; times in hours; DEE in kJ; dive proportions as fractions.
- Provenance and reproducibility:
  - Clear lineage from field collection to processing (names of collectors and processor; licensing stated).
  - Derived variables (daily budgets, activity proportions) documented as coming from raw biologging outputs.
- Sharing and interoperability:
  - Data are organized into three CSV files with explicit column definitions; potential need for standardizing date formats to ISO for interoperability.
- Usage considerations for data stewards:
  - Maintain provenance references (who collected, processed, and granted access).
  - Preserve per-individual and per-day linkage across the three files; handle multiple daily location entries.
  - Ensure proper citation and licensing notes accompany dataset use; acknowledge SNH and the researchers involved.
  - Consider providing machine-readable metadata (data dictionary, variable definitions, and units) to facilitate discovery and reuse.

## Implications for data stewardship and future use
- The dataset is valuable for studies of seabird energetics, movement ecology, and colony dynamics, provided metadata are preserved and access rights followed.
- To enhance discoverability and interoperability, consider adding persistent identifiers (e.g., DOIs) and a machine-readable data dictionary with versioning.
- Plan for ongoing updates or reprocessing workflows if raw data or metadata are expanded or corrected in the future.