# Windermere Fish Abundance 1940-2012

- Overview
  - Long-term dataset on fish abundance in Windermere (1940–2012).
  - Includes Arctic charr, Pike, Perch, Roach, and total fish abundance from hydroacoustics.
  - Data originate from Windermere North and South Basins; provided as yearly averages.
  - Collected primarily by the Freshwater Biological Association (FBA) up to 1989, then by CEH and its predecessor IFE; hydroacoustics data collected by CEH/IFE since 1990.
  - Primary file: Windermere_fish_1940_2012.csv (CSV, 24 kb).

- Data content and structure
  - Columns in the data file:
    - YEAR: Year of measurement.
    - SITE: Windermere North basin or Windermere South basin.
    - DETERMINAND: Fish species or “Total fish (hydroacoustics)” (e.g., Esox lucius, Perca fluviatilis, Rutilus rutilus, Salvelinus alpinus, Total fish).
    - ANNUAL_AVERAGE: Mean value for the year.
    - UNITOFMEASURMENT: CPUE (catch per unit effort) in fish ha-1 or related units (for hydroacoustics data, total fish abundance).
  - DETERMINAND details:
    - Esox lucius (Pike), Perca fluviatilis (Perch), Rutilus rutilus (Roach), Salvelinus alpinus (Arctic charr), and “Total fish (hydroacoustics)”.

- Sampling design and methods by species
  - Pike (1944–present)
    - Sampling: gill netting; many changes pre-1982, standardized since 1982.
    - Standard method (since 1982): 64 mm bar mesh multifilament nets, 40 m x 3 m; 10 sites per basin; October–December; five nets in water simultaneously; rotating sites to cover lake; annual effort ~240 net days since 1990 (balanced between basins).
    - Laboratory: measure length/weight, determine sex, age by opercular bone; CPUE calculated as mean pike per net effort per year for each basin.
  - Perch (1943–2012)
    - Sampling: standardised trapping technique (1950s onward); CPUE by numbers per year (1982–2012); high intra-annual variation limited meaningful confidence limits.
    - Early traps: 300 wire traps later improved; tar-varnish to improve catches.
  - Roach (Rutilus rutilus)
    - Sampling: bottom-set survey gill nets at 15 inshore sites (split north/south basins); nets with varying mesh designs across years (1995, 2000, 2005, 2010).
    - 1995: 60 m long, 1.5 m deep; multiple mesh sizes.
    - 2000: similar length/depth with updated mesh sizes.
    - 2005/2010: Norden design (30 m x 1.5 m) with multiple mesh sizes.
    - Laboratory: all catches frozen; species identified and enumerated; CPUE calculated for small (< ~200 mm) and large (~200 mm) roach per basin per year.
  - Arctic charr (Salvelinus alpinus)
    - Sampling: monitored in the north basin (1940–2012) using gill nets (~28 m x 1.8 m) with mesh 32 mm; spawning ground locations over time.
    - Analytical: CPUE for spawning Arctic charr in November (monthly data aggregated to annual means).
  - Hydroacoustics (Total fish abundance)
    - Surveys: night and day surveys across north and south basins from 1990 onward (monthly intervals).
    - Equipment evolution:
      - 1990–2002: single-beam system (Simrad EY-M) with zig-zag coverage.
      - 2002 onward: split-beam system (BioSonics DT6000/DT-X) with inter-calibration to the prior system.
    - Analytical: night-time abundance for all detectable fish (entire water column); day-time abundance for large fish (>~200 mm) in upper 20 m; annual means with 95% CIs.

- Quality control and provenance
  - Quality control across methods:
    - Pike/roach/charr: measurements validated by multiple individuals (permutations or independent checks).
    Arctic charr and hydroacoustics: two-person checks for quality control.
  - Provenance and references:
    - Methodological notes and calibration cited from Baroudy & Elliott (1993), Winfield & Fletcher (2006), Kipling (1984), Le Cren (1959/2001), and others.
  - Data governance considerations:
    - Metadata describe site locations, sampling regimes, and year-by-year methodological changes; essential for traceability and interoperability across decades.

- Geographic and temporal coverage
  - Location: Windermere, Cumbria, Great Britain.
  - Basins: Windermere North and Windermere South.
  - Grid reference: approximately SD393960 (OS Grid), 54.360193, -2.935836 (WGS84).
  - Time span: 1940–2012, with hydroacoustics data from 1990 onward.

- Accessibility and metadata
  - Data format: CSV (Windermere_fish_1940_2012.csv).
  - Availability: data originated from Windermere North and South Basins; designed for download and reuse.
  - File size: 24 kb.
  - Documentation includes sampling design, collection methods, analytical methods, and quality control notes for each determinate.

- Governance considerations for Data Stewards
  - Ensure clear documentation of methodological shifts over time (e.g., post-1982 pike net standardization, 2002 hydroacoustic system upgrade).
  - Preserve species- and method-specific CPUE definitions to maintain comparability across years.
  - Maintain provenance links to foundational methodological papers and calibration protocols.
  - Provide explicit metadata on units, basins, and temporal windows to support interoperability and reuse.
  - Monitor data completeness and potential gaps due to changes in survey effort or method.

- End note
  - The Windermere Fish Abundance 1940-2012 dataset offers a comprehensive, multi-method, long-term view of fish populations in Windermere, suitable for trend analysis, resource management, and ecological studies, with robust QC and detailed methodological metadata to support data stewardship and reuse.