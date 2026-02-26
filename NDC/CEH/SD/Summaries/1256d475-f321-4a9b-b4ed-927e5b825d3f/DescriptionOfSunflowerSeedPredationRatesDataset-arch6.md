# Sunflower seed predation rates in Biodiversity and Ecosystem Function in Tropical Agriculture (BEFTA) plots, Sumatra, Indonesia

## Overview
- Study location: three estates in Riau Province, Sumatra, Indonesia (Ujung Tanjung, Kandista, Libo) owned by Pt Ivo Mas Tunggal.
- Experimental setup: 18 plots established in 2013 as part of the BEFTA project investigating vegetation management and granivory.
- Stand types: mature stands at Ujung Tanjung and Kandista; Libo replanted in 2014.
- Sampling: granivory measured once in 2014 (mature) and five times across 2016–2017 (mature and replanted).

## Experimental design and data collection
- Granivory assay: ten shelled sunflower seeds placed on a 15 cm paper disc, covered by a polystyrene plate ~10 cm above soil.
- Treatments (per replicate): 
  - remain_cage_grease (cage + grease)
  - remain_cage (cage only)
  - remain_open_grease (grease only)
  - remain_open (open)
- Setup: traps are metal grids (approx. 35 x 20 x 14 cm); four treatments applied at each of three sampling positions per plot, field exposure for ~24 hours.
- Sampling positions: edges of the 50 x 50 m plot at 45°, 165°, and 285° from compass north.
- Response variable: seeds remaining out of ten (decimal values possible when half seeds are present).

## Data structure and storage
- Data format: three separate CSV files (thin format; one observation per line):
  - SunflowerSeedPredationRates_2014.csv (mature stands)
  - SunflowerSeedPredationRates_2016_2017.csv (mature stands)
  - SunflowerSeedPredationRates_replants.csv (replanted stands)
- Key columns (example):
  - Estate_abbrev (KNDE, UTNE, LIBE)
  - Plot_no (e.g., C01, C10, D28)
  - Triplet (plot sets of three; aids point identification)
  - Treatment (reduced/normal/enhanced since Feb 2014)
  - Period (discrete sampling periods)
  - Position (sampling compass heading)
  - Date_set / Time_set (seed placement)
  - Date_coll / Time_coll (seeds remaining recorded)
  - seedstreat (remain_cage, remain_open, remain_cage_grease, remain_open_grease)
  - seedsremaining (numeric; out of ten)
  - dayrain (24-hour rainfall at nearest weather station)
  - allnotes (observations and data-entry notes)
  - SAFE_distance (numeric; only in SunflowerSeedPredationRates_2016_2017.csv; may indicate data to exclude)

## Quality control and provenance
- Data checks: basic validation for impossible values (e.g., more seeds remaining than possible).
- Data entry verification: 50% of entries cross-checked against original field sheets; error rate <1%; corrections logged with data provenance preserved.
- Funding and scope: project funded under NE/P00458X/1.
- Data scope: two BEFTA core data files (2016–2017) and replanted plots; coordinates and field notes included in the dataset.

## Variables, units, and notes
- Seeds remaining: numeric, representing how many seeds remained from ten after the exposure period (decimals possible due to half-seeds).
- Dayrain: numeric value of rainfall (mm) during the 24-hour interval from 8am to 8am.
- Time/date fields: recorded to allow precise temporal alignment of seed placement and assessment.
- SAFE_distance: only in the 2016–2017 mature dataset; data may be unsuitable for analysis and should be treated with caution or excluded.

## Cautions and limitations
- SAFE_distance data may not be suitable for use; interpret with caution for 2016–2017 dataset.
- Exclosure and ant-poison related notes apply to the 2016–2017 period and may affect interpretation of predation rates.
- Data are provided in thin format; users may need to reconstruct plot-level or triplet-level aggregations as required.

## Access and reuse
- Files available:
  - SunflowerSeedPredationRates_2014.csv
  - SunflowerSeedPredationRates_2016_2017.csv
  - SunflowerSeedPredationRates_replants.csv
- Usage: suitable for analyses of granivory/predation rates across estates, stand types, treatments, and sampling periods; allows self-serve exploration and creation of data products (dashboards, summaries) to support end-user interpretation.