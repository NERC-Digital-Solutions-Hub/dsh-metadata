# Windermere Fish Abundance 1940-2012

## Overview
- Long-term dataset documenting abundance of Windermere fish species from 1940 to 2012.
- Species include Arctic charr (Salvelinus alpinus), Pike (Esox lucius), Perch (Perca fluviatilis), Roach (Rutilus rutilus), plus total fish abundance from hydroacoustics.
- Data cover Windermere North and South basins; annual averages are provided.
- Historically collected by the Freshwater Biological Association (FBA); since 1989 by CEH and its predecessor Institute of Freshwater Ecology (IFE). Hydroacoustics data collected by CEH/IFE since 1990.

## Data content and scope
- File: Windermere_fish_1940_2012.csv
- Format: CSV, 24 KB
- Columns: YEAR, SITE, DETERMINAND (species), ANNUAL_AVERAGE, UNITOFMEASUREMENT
- UNITOFMEASUREMENT values reflect:
  - CPUE (catch per unit effort) for pike, perch, roach, Arctic charr
  - CPUE expressed as fish per hectare for hydroacoustics (total fish)
- Data originate from Windermere North and South basins (sites).

## Sampling design by species

- Pike (Esox lucius)
  - Monitoring sites in north and south basins (SITE) using gill nets; continuous since 1944.
  - Standardised since 1982: 64 mm bar mesh, 40 m x 3 m nets, 4–5 m depth, Oct–Dec, 10 sites per basin.
  - Sampling cadence: weekly cycle (set, lift, re-set) with rotating sites; typical annual effort ~240 net days (since 1990).
  - In-field: measure length/weight, determine sex; age via left opercular bone.
  - Output: annual average CPUE by year (numbers of pike per unit effort) for each basin.

- Perch (Perca fluviatilis)
  - Monitoring in north and south basins via trapping (1943–2012).
  - Initial traps: ~300, tar-varnish coated; evolved trap design over time.
  - Sampling: April–June; CPUE by numbers calculated per year from single sampling sites (north/south) with high intra-annual variation.
  - Output: annual average CPUE per year for North and South basins.

- Roach (Rutilus rutilus)
  - Bottom-set survey gill nets inshore; sampling at 15 sites (split roughly 5 north, 10 south) during September.
  - Net designs changed across years (1995, 2000, 2005, 2010) with various bar mesh sizes.
  - Processing: catch frozen and later species-identified/enumerated.
  - Output: CPUE by year (numbers per 100 m2 net per day) for each basin.

- Arctic charr (Salvelinus alpinus)
  - Monitored in the north basin (1940–2012) using gill nets (~28 m long, 1.8 m deep; 32 mm mesh, with changes pre-1970s).
  - Target: spawning ground abundance; nets deployed Oct–Dec at ~2 m depth.
  - Processing: measure and release most fish; occasional mortalities retained.
  - Output: CPUE for spawning Arctic charr by November each year (numbers per net per day).

- Hydroacoustics (total fish abundance)
  - Night- and day-time hydroacoustic surveys across both basins from 1990 onward (monthly).
  - Method evolution: 1990 zig-zag single-beam (70 kHz) followed by 2002 upgrade to split-beam (200 kHz) with calibration.
  - Outputs:
    - Night-time abundance of all detectable fish in the water column (best total abundance estimate).
    - Day-time abundance of large fish (~≥200 mm) in upper ~20 m (best estimate of exploitable stock).
  - Quality: calibration performed per manufacturer guidelines; data summarized as means ± 95% CIs.

## Data structure and format
- Primary fields: YEAR, SITE, DETERMINAND, ANNUAL_AVERAGE, UNITOFMEASUREMENT.
- DETERMINAND values correspond to each species and aggregate fish metrics (e.g., "Total fish (hydroacoustics)").
- ANNUAL_AVERAGE provides the year-specific average metric for the given determininand and site.
- Outputs are provided as yearly averages across the sampling regime described above.

## Geographic scope and sampling regime
- Geographic focus: Windermere lake, Cumbria, Great Britain.
- Basins: Windermere North and Windermere South.
- Sampling seasons/timing vary by species (e.g., pike autumn nets; perch early-year traps; roach September nets; Arctic charr spawning-season focus in November).

## Analytical methods and intended outputs
- CPUE metrics used to quantify abundance for pike, perch, roach, and Arctic charr (with units specified above).
- Hydroacoustic data used to estimate total fish abundance and exploitable-size fish abundance.
- Data presented as annual averages with accompanying 95% confidence limits for several species and total fish metrics.

## Data quality control and provenance
- Quality control includes cross-checks of measurements by multiple individuals (e.g., permutations of three), and replication by two individuals for hydroacoustic calibration checks.
- Data origin and references documented (e.g., Le Cren, 1959/2001; Kipling, 1984; Baroudy and Elliott, 1993; Winfield et al., 2006; Kipling 1984; Fletcher et al. references).
- Data management and metadata practices align with CEH/IFE data standards; historical records maintained and datasets made available with descriptive metadata.

## Related references and context
- Key methodological references and related publications cited for pike, perch, roach, and Arctic charr methodologies and hydroacoustic approaches.
- Dataset intended to support analyses of long-term fish population trends and responses to environmental drivers within Windermere.