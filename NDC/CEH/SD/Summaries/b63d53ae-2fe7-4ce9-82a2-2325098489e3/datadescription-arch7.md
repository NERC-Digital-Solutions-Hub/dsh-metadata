# EIDC dataset: Tritrophic phenology and associated data from 44 sites in Scotland, 2014-2021

- Overview
  - A multi-year, 44-site dataset from Scotland (2014–2021) documenting tree phenology, caterpillar activity, and blue tit breeding data.
  - Data collected at woodland sites near major roads (M90 and A9), with nestboxes and temperature loggers.
  - 2020 fieldwork impacted by COVID-19, causing partial data collection ( southern sites visited more regularly; some measures missing).
  - Data are organized into seven CSV files, linked by site and year; site_details provides spatial context (MeanLat, MeanLong, MeanElev).

- Spatial scope and sampling design
  - Initially 30 woodland sites; expanded to 44 across Edinburgh to Dornoch.
  - Eight nestboxes per site common by 2017; visits every 2 days from early spring to early summer.
  - Temperature measured by two loggers per site at ~1.5 m height; hourly air temperatures (mid-Feb to mid-Jun).

- Data types and files
  - site_details: site codes, names, average latitude/longitude, average elevation.
  - temperatures: hourly temperature data per site and year; columns X46–X163 for hourly measurements; NA where data missing.
  - Tree_Phenology: per-tree records including year, site, TreeID, taxon, budburst and leaf phenophases (fbb, cbb, flf, clf) as ordinal days.
  - Branch_Beating: per-branch caterpillar sampling data including year, site, treeID, taxon, date, weather, caterpillar counts, mass, notes, and mass uncertainty.
  - Bird_Phenology: nestbox-level blue tit phenology and breeding activity (egg dates, hatching, incubation, clutch size, fledging, etc.) with special handling for clutch_swap_treatment.
  - Nestlings: nestling measurements across visits (mass, wing, ringed status, age).
  - Adults: adult bird metrics (ring, year, site, box, age, sex, wing, mass, date/time, ringer).

- Data structure and integration
  - The same site/year codes enable merging across files.
  - Spatial analyses can rely on site_details for mapping site locations and elevations.
  - Temporal analyses can leverage temperatures, tree phenology, caterpillar activity, and bird breeding data in parallel.

- GIS-focused considerations and use cases
  - Create map-based visuals of phenology timing (budburst, leaf-out) and caterpillar peaks across sites.
  - Overlay microclimate data (hourly temperatures) with phenological events.
  - Explore spatial patterns in blue tit breeding timing and success in relation to habitat and temperature gradients.
  - Combine with elevation and distance to roads to assess environmental drivers.

- Data quality, limitations, and notes
  - Some years have incomplete measurements due to field conditions and COVID-19.
  - Taxonomic resolution varies (species vs. genus in some trees).
  - Caterpillar masses recorded as <0.02 g when below scale threshold; certain entries include notes for reliability.
  - Clutch_swap_treatment requires careful analysis handling or exclusion as appropriate.

- References (illustrative context)
  - Macphie et al. 2020; Shutt et al. 2018; Shutt et al. 2019a; Shutt et al. 2019b.