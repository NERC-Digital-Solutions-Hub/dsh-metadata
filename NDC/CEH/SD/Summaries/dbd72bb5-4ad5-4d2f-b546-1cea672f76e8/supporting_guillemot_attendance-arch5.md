# Data Collection

- Context and aim
  - NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
  - Isle of May, Scotland, chosen for its large, accessible population of common guillemots (model species).
  - Aim: quantify movements of immature guillemots to better understand infection risk to the breeding colony.

- Field site and sampling design
  - Four sites on the Isle of May; data collected in two periods: 25 Apr–12 May 2013 and 21 May–15 Jun 2013.
  - 69 randomly selected, individually marked birds followed with a telescope (×20–60) for 10-minute periods.
  - Locations recorded every 15 seconds; stratified sampling to balance coverage across sites and times of day.
  - Each site observed for 2 hours per day.
  - Grid overlay on site photographs to classify grid cells as breeding or pre-breeding based on observed activity; cells with surrounding breeding activity considered breeding areas.
  - If a focal bird was lost from sight, the watch continued (out of sight); if the bird flew away, the watch was terminated.
  - Preliminary data included in the dataset.
  - An index of breeder attendance per site was created by counting birds in a delimited breeding area and normalizing by the maximum count.

- Data collection specifics and workflow
  - Location data used to derive time spent in pre-breeding vs breeding areas.
  - Documentation and supporting materials include site_maps_guillemot_attendance.pdf.

- Data structure and key variables
  - Date_norm: day count from the first date of data collection.
  - Sub_colony: site where the bird was observed.
  - Time_perod: time of day (1 = dawn–10:30, 2 = 10:30–16:00, 3 = 16:00–dusk).
  - Wind_strength: ordinal scale (1 = None, 2 = Light breeze, 3 = Fair breeze, 4 = Strong, 5 = Gale force).
  - Sea condition: ordinal scale (1 = Still, 2 = Calm, 3 = Fairly choppy, 5 = Very choppy, 6 = High waves).
  - Temperature: ordinal scale (1 = Very warm, 2 = Warm, 3 = Comfortable, 4 = Cool, 5 = Very Cool, 6 = Freezing).
  - B_att_prop: proportion of breeding birds in a defined area (relative to maximum count in that area).
  - Age: age of the bird (current year minus year of ringing).
  - Ring: unique ID for each bird.
  - Sampling period: duration of the watch (mostly 10 minutes; some preliminary observations vary).
  - P_recs: number of intervals in which the bird was seen in a pre-breeding area.
  - Time interval: sampling interval (mostly 15 seconds; some preliminary observations vary).
  - B_recs: number of intervals in which the bird was seen in a breeding area.
  - Other_unknown_recs: intervals where the bird was not seen in any grid cell (e.g., flew off).
  - Other_known_recs: intervals where the bird was seen in a grid cell of unknown status.

- Data quality, provenance, and reuse considerations
  - Dataset includes preliminary data; explicit documentation of variable definitions and scoring schemes is essential for reuse.
  - Some minor inconsistencies in variable naming (e.g., Time_perod) indicate a need for standardization.
  - Provenance tied to field observations and an accompanying site map file; clear linkage between grid classifications and observed locations is important.
  - Data accessibility may benefit from detailed metadata, definitions of breeding vs pre-breeding areas, and guidance on handling incomplete observations.

- Data governance implications for Data Stewards
  - Ensure metadata completeness: clear definitions, units, and scoring for environmental variables; consistent date and time formats.
  - Implement data quality checks for variable names (e.g., correct Time_perod) and range validation for ordinal scales.
  - Maintain linkage to external materials (site_maps_guillemot_attendance.pdf) and ensure long-term access.
  - Capture data provenance and the status of preliminary data; consider versioning and documentation of any data processing steps.
  - Clarify licensing and sharing policies if the dataset is intended for public reuse.