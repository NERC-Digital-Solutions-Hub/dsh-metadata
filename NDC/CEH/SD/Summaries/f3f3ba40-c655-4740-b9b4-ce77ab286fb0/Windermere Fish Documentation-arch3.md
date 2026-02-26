# Windermere Fish Abundance 1940-2012

- Overview
  - Long-term dataset of fish abundance in Windermere (1940–2012) covering Arctic charr, pike, perch, roach, and total fish abundance from hydroacoustics.
  - Data mainly originate from Windermere North and South Basins; collected by the Freshwater Biological Association (FBA) and, since 1989, by CEH and its predecessor IFE.
  - Outputs are provided as yearly averages and are available for download as CSV files.

- Data content and structure
  - File format and scope
    - Windermere_fish_1940_2012.csv; size ~24 KB; columns include YEAR, SITE, DETERMINAND, ANNUAL_AVERAGE, UNITOFMEASUREMENT.
  - Determinands (species and measures)
    - Esox lucius (Pike); Perca fluviatilis (Perch); Rutilus rutilus (Roach); Salvelinus alpinus (Arctic charr); Total fish (hydroacoustics).
  - Measurements and units
    - CPUE-based measures for pike, perch, roach, and Arctic charr (e.g., CPUE fish per unit effort, net-days, or area-based CPUE per 100 m2 per day).
    - Hydroacoustics: night-time total fish abundance (fish ha-1) and day-time abundance of large fish (≥ about 200 mm) in the upper water column.
  - Sampling sites and location
    - Data cover Windermere North and South Basins; approximate lake-centre coordinates provided for site localisation.
  - Metadata and quality indicators
    - Columns and determinants indicate measurement type (CPUE, abundance) and unit; year-by-year averages produced from standardized protocols where applicable.

- Data collection methods and sampling design
  - Pike (Esox lucius)
    - Basins: north and south; method: standardized gill-netting.
    - Timeframe: continuous monitoring since 1944; standard method since 1982 (64 mm bar-mesh nets, 40 m x 3 m, multiple sites per basin).
    - Sampling effort: ~240 net days annually since 1990, distributed between basins; site rotation over two weeks per year.
  - Perch (Perca fluviatilis)
    - Basins: north and south; method: trapping; standardised since 1943.
    - Trap designs evolved; from 1941 tar-varnish-treated traps to standardized forms; data used to compute CPUE by year (1982–2012) per basin.
  - Roach (Rutilus rutilus)
    - Basins: north and south; method: bottom-set gill nets; sampling at multiple inshore sites.
    - Years: 1995, 2000, 2005, 2012; net designs changed over time; CPUE compiled as annual averages (per 100 m2 net per day) for small and large roach.
  - Arctic charr (Salvelinus alpinus)
    - Basins: north; method: gill nets on spawning grounds.
    - Timeframe: 1940–2012; spawning-ground sampling in October–December; CPUE calculated for November (month of peak catches).
  - Hydroacoustics (total fish abundance)
    - Basins: north and south; method: night-time hydroacoustic surveys since 1990; day-time assessments of large fish in upper water column.
    - Equipment evolution: early zig-zag single-beam (1990–2001); since 2002, split-beam systems with calibration and inter-system checks.
    - Reporting: annual means with 95% confidence limits for night-time total abundance and day-time large fish abundance.

- Quality assurance and data governance
  - Quality control
    - Biological measurements checked by multiple individuals (three-person verifications for some datasets).
    - Hydroacoustic data calibrated and inter-calibrated between systems; periodic field and lab calibrations.
  - Data provenance and collaboration
    - Data originate from Windermere North and South Basins; maintained through collaborations between FBA and CEH/IFE.
    - Document references include methodological and calibration details, underpinning transparency and reproducibility.

- Limitations and considerations for monitoring use
  - Methodological changes over time
    - Gear changes and sampling designs (e.g., trapping methods, net designs, and hydroacoustic systems) introduce comparability considerations across years.
  - Variability and data gaps
    - High intra-annual variability for roach CPUE; roach data limited to specific years (1995, 2000, 2005, 2012); some determinants have detailed year-by-year coverage, others are periodic.
  - Data granularity
    - Outputs are annual averages; spatially explicit site-level data are not provided in the CSV summary, though site-level sampling existed in raw data.
  - Metadata completeness
    - Core metadata are provided (locations, units, determinants), but researchers may need to consult original references for full methodological metadata and calibration logs.

- Implications for monitoring frameworks and policy use
  - Long-term, multi-method monitoring enables assessment of trends in fish populations related to eutrophication, climate change, and prey dynamics.
  - Standardized protocols (where applied) and explicit quality control enhance reliability for policy evaluation and decision-making.
  - Transparency of data processing (CPUE calculations, hydroacoustic analysis) supports openness and data governance aligned with monitoring frameworks.
  - Caution advised when integrating across years with methodological changes; leverage calibration and inter-system comparisons to reconcile differences.

- References and further information
  - Kipling, C. (1984); Le Cren, E. D. (1959) and (2001) on aging and sampling design.
  - Baroudy, E. & Elliott, J. M. (1993); Winfield, I. J., Fletcher, J. M. & James, J. B. (2006) on hydroacoustics and surveillance methodologies.
  - Additional species-focused studies: Winfield et al. (2008) on Arctic charr and roach/population dynamics; Le Cren (2001) on Windermere perch and pike project.