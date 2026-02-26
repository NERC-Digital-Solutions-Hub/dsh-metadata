# Windermere Fish Abundance 1940-2012

## Dataset Description
- Long-term dataset describing fish abundance in Windermere (North and South basins) from 1940 to 2012.
- Includes data for Arctic charr, pike, perch, roach, and total fish abundance from hydroacoustics, plus all detectable species.
- Data originally collected by the Freshwater Biological Association (FBA) and later by CEH/IFE; hydroacoustics data gathered by CEH/IFE since 1990.
- Available to download as Windermere_fish_1940_2012.csv (CSV, 24 kb), covering yearly basin-average values.

## File Details and Structure
- File format: CSV
- Columns:
  - YEAR: Year measurements were taken
  - SITE: Windermere North basin or Windermere South basin
  - DETERMINAND: Fish species name (determinant)
  - ANNUAL_AVERAGE: Yearly mean value
  - UNITOFMEASUREMENT: Measurement unit (CPUE or equivalent)
- DETERMINAND values include:
  - Esox lucius (Pike)
  - Perca fluviatilis (Perch)
  - Rutilus rutilus (Roach)
  - Salvelinus alpinus (Arctic charr)
  - Total fish (hydroacoustics)
  - All detectable fish species (as applicable)

## Spatial and Temporal Coverage
- Spatial: Windermere North basin and Windermere South basin
- Temporal: 
  - Arctic charr: 1940–2012 (north basin site-specific spawning data)
  - Pike: 1944–present (north and south basins)
  - Perch: 1943–2012 (north and south basins)
  - Roach: 1995, 2000, 2005, 2012 (bottom-set gill-net surveys)
  - Hydroacoustics (total fish abundance): 1990–2012 (monthly sampling, both basins)

## Sampling and Measurement Methods
- Pike (Esox lucius)
  - Sampling: standardized gill nets (64 mm bar mesh, 40 m x 3 m nets) from mid-Oct to late Dec; fixed sites in each basin; two-week site visits per season.
  - Measurements: length, weight, sex; age from opercular bone; CPUE calculated per year for north and south basins.
- Perch (Perca fluviatilis)
  - Sampling: standardized trapping at sites in north and south basins (1943–2012); long-term trap designs evolved; CPUE by year calculated per site.
- Roach (Rutilus rutilus)
  - Sampling: bottom-set survey gill nets at 15 inshore sites (north and south basins); variations in net size and mesh across years (1995, 2000, 2005, 2010–present).
  - Measurements: species identification; CPUE calculated for small and large roach separately (net-1 day, or equivalent units).
- Arctic charr (Salvelinus alpinus)
  - Sampling: gill netting on spawning grounds (Low Wray Bay, North Thompson Holme) from October–December; spawning-month CPUE calculated (November) per basin.
- Hydroacoustics (Total fish from hydroacoustics)
  - Sampling: day and night hydroacoustic surveys at approximately monthly intervals from 1990 onward.
  - Technology: initial single-beam 70 kHz system (1990s) then split-beam 200 kHz system from 2002, with inter-calibration between systems.
  - Analysis: night-time abundance for the entire water column (total fish); day-time abundance of large fish (~≥200 mm) in upper 20 m; means with 95% CIs computed per year per basin.

## Data Processing and Quality Control
- Data were cleaned, standardized, and converted into annual averages per determinand and basin.
- Quality control includes measurements checked by permutations of three individuals for consistency.
- Hydroacoustic data include calibration steps and periodic field/lab calibrations as per manufacturer guidelines.

## Usage Considerations and Notes
- Units are CPUE or equivalent; species-specific definitions vary (e.g., fish per ha for hydroacoustics, net-1 day for roach, etc.). Users should align units when comparing across determinands.
- The roach dataset shows high intra-annual variation, which affected the ability to generate meaningful confidence limits for some years.
- Methodology evolved over time (e.g., trap designs, gill-net configurations, and hydroacoustic systems), which may affect comparability across periods; consider basins and sampling regime when analyzing trends.
- The dataset provides yearly basinal averages rather than site-by-site data in the downloadable file.

## Potential Data Products and Analytical Uses
- Trend analysis of CPUE for pike, perch, and Arctic charr by basin (1940/1944–2012).
- Long-term abundance assessments from hydroacoustics to complement netting data.
- Comparative analyses of spawning vs. total abundance for Arctic charr.
- Cross-species and basin comparisons to explore influences of eutrophication, climate, and prey abundance (e.g., roach dynamics).

## References and Documentation
- Data are accompanied by methodological notes and references detailing sampling regimes, age/length measurements, and prior analyses (e.g., Le Cren 2001; Kipling 1984; Baroudy et al. 1993; Winfield et al. 2006; Baroudy & Elliott 1993; Elliott & Fletcher 2001; related Hydroacoustics and Perch/Pike studies).
- Key cited works provide context on measurement techniques, calibration, and interpretation of CPUE and abundance estimates.