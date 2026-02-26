# Pike Survival Data 1953-1990

## Overview
- Part of data used in Vindenes et al. (2013) American Naturalist on climate change effects in trait-based dynamics of a top predator in freshwater ecosystems.
- Survival data (binary) from capture-mark-recapture of Pike (Esox lucius) in Windermere Lake, Great Britain.
- Data collection began in 1944; this dataset focuses on survival after initial capture, including males, females, and individuals of unknown sex.

## Data Columns and Format
- Format: CSV (comma separated values); size approximately 68 KB.
- Core columns:
  - YEAR: Year of first capture of the individual fish.
  - LENGTH: Fork length at capture (cm).
  - SURVIVAL: 1 if the individual is recorded again (survived the first period after capture), 0 otherwise.
- Location: Windermere Lake, Cumbria; approximate center grid reference provided.

## Study Area & Sampling Regime
- Locale: Windermere Lake, encompassing north and south basins.
- Sampling method: Gill netting with variations pre-1982; standardized since 1982.
  - Since 1982: 64 mm bar mesh multifilament gill nets, about 40 m x 3 m, used at depths ~4–5 m.
  - Sites: 10 sites per basin (north and south) with nets set from mid-Oct to late Dec.
  - Sampling pattern: Five nets in the water at a time; sites rotated; each site fished for two weeks per season.
  - Annual effort: ~348 net days (1982–1989) split roughly evenly between basins; ~240 net days since 1990.
- Additional data: Sightings of individually-numbered tagged fish by catch-and-release anglers maintained throughout the study.

## Data Collection & Analytical Methods
- Measurements: Length (to 1 mm), weight (to 100 g), and sex determination from dissection.
- Ageing: Left opercular bone used to determine age; birth date assumed 1 April.
- Survival calculation: Combines capture data with angler sightings to derive survival metrics (as described by Haugen et al. 2007).

## Quality Control
- Measurements validated through permutations involving three individuals to ensure accuracy.

## Related Datasets & Metadata
- Metadata: Pike 1944-2002 data series.
- Related datasets:
  - Pike - Fecundity Data 1963-2002
  - Pike - Growth Data 1944-1995
  - Windermere Lake Temperature 1944-2002
- References for methodology and context available (e.g., Le Cren 2001; Winfield et al. 2008; Frost & Kipling 1959; Haugen et al. 2007).