# Windermere Fish Abundance 1940-2012

## Overview
- Long-term dataset on fish abundance in Windermere (Arctic charr, Pike, Perch, Roach; plus total fish via hydroacoustics).
- Data range: 1940–2012; includes both North and South Basins of Windermere.
- Data sources: Freshwater Biological Association (FBA) originally; CEH and its predecessor IFE since 1989; hydroacoustics data collected by CEH/IFE since 1990.
- Format: yearly averages available in a downloadable CSV (Windermere_fish_1940_2012.csv; ~24 KB).

## Data Format and Content
- File: Windermere_fish_1940_2012.csv
- Columns: YEAR, SITE, DETERMINAND (fish species), ANNUAL_AVERAGE (mean for year), UNITOFMEASUREMENT (CPUE or fish ha-1 for hydroacoustics data)
- DETERMINAND options:
  - Esox lucius (Pike) – CPUE (numbers per unit effort)
  - Perca fluviatilis (Perch) – CPUE
  - Rutilus rutilus (Roach) – CPUE (small vs large analyzed)
  - Salvelinus alpinus (Arctic charr) – CPUE
  - Total fish (hydroacoustics) – fish per hectare
  - All detectable fish species (hydroacoustics)
- Spatial scope: Windermere North basin and Windermere South basin
- Location reference: Windermere lake, Cumbria, UK; grid coordinates provided

## Sampling Regimes by Species
- Pike (Esox lucius)
  - Basins: North and South
  - Method: gill netting; standardized since 1982 using 64 mm bar mesh nets
  - Layout: 5 nets, 10 sites per basin; seasonal sampling Oct–Dec
  - Effort: ~348 net days (1982–1989); ~240 net days annually (since 1990), balanced between basins
- Perch (Perca fluviatilis)
  - Basins: North and South
  - Method: trapping; standardized from 1943 onward
  - Timing: April–June; long-term trapping history
- Roach (Rutilus rutilus)
  - Basins: North and South
  - Method: bottom-set survey gill nets; varying designs over years (1995, 2000, 2005, 2010s)
  - Sampling: 15 inshore sites (split between basins)
- Arctic charr (Salvelinus alpinus)
  - Basin: North
  - Method: gill netting on spawning grounds (Low Wray Bay 1939–1973; North Thompson Holme 1975–2012)
  - Timing: spawning period monitoring; data focused on November CPUE
- Hydroacoustics (Total fish abundance)
  - Basins: North and South
  - Method: annual night-time hydroacoustic surveys (1990–present); initial zig-zag design, later split-beam system (from 2002)
  - Calibration: periodic calibration per manufacturer instructions
  - Outputs: night-time abundance of all detectable fish (entire water column) and day-time abundance of large fish (>~200 mm) in upper 20 m

## Analytical Methods
- Pike, Perch, Roach, Arctic charr
  - CPUE calculations per year and basin
  - Units: CPUE = Catch per unit effort (numbers per net/day or per 100 m2 net day, depending on species)
  - Arctic charr CPUE calculated for spawning months (November)
- Hydroacoustics
  - Outputs: mean night-time abundance across entire water column; mean day-time abundance of large fish in upper 20 m
  - Confidence intervals: 95% CIs provided for annual means
- Data handling
  - All catches identified to species, measured (size/weight as applicable), examined for quality
  - Data stored as annual averages for download

## Quality Control
- Measurements cross-checked by multiple individuals (three for most data)
- Hydroacoustic calibration and validation by two individuals
- References to methodological standards and key validation studies provided

## Data Accessibility and Provenance
- Origin: FBA data collection (1940–1989) transferred to CEH/IFE (from 1989 onward)
- Hydroacoustics data collected by CEH/IFE (since 1990)
- Data downloadable from Windermere Basins (North and South)
- Location and site details documented (grid references and coordinates)

## Data Quality and Considerations
- Perch data: high intra-annual variation; limited confidence interval interpretability for annual CPUE
- Long-term consistency achieved via standardized methods (1982 onward for pike; ongoing standardized traps for perch; Nordic/Norden net designs for roach)
- Calibration and method changes noted, especially for hydroacoustics (1990 start; 2002 split-beam update)

## Outputs and Applications
- Enables assessment of environmental health and policy performance over time
- Supports analyses of trends related to eutrophication, climate change, and prey abundance (e.g., roach effects on Arctic charr)
- Useful for cross-basin comparisons and long-term monitoring programs

## Related Publications and References
- Key methodological and result references cited for pike, perch, Arctic charr, and hydroacoustic work, including Le Cren (2001), Frost & Kipling (1959), Kipling (1984), Baroudy & Elliott (1993), Winfield et al. (2006), and related Fish Biology/Environmental Biology of Fishes papers (2008).