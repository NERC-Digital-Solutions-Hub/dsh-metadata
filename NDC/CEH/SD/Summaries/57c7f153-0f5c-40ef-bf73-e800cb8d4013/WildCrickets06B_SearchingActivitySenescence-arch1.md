# WildCrickets06B_SearchingActivitySenescence Description of content

- A dataset describing the duration of observation periods for individual male adult crickets, with activity categorized as short or long.
- Short vs. long classification is defined by a 77-minute threshold:
  - Short duration: 1 (≤ 77 minutes)
  - Long duration: 0 ( > 77 minutes)
- Key fields:
  - Year: calendar year associated with the observation period
  - Year alive: the year when the cricket was alive
  - ID: unique identifier for each cricket
  - Temp: ambient temperature during the observation period in degrees Celsius
  - Age: age of the cricket in days at the time of sampling
  - Short: binary indicator (1 = short period, 0 = not short)
- Each row represents one observation period per individual cricket, with the duration categorized accordingly.