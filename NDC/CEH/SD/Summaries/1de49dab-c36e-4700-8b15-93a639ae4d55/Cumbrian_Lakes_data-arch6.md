# Cumbrian Lakes plankton and fish data, used for turning points and early warnings analysis (1940 to 2013)

- Purpose and scope
  - Dataset describing phyto- and zooplankton counts, chlorophyll concentration, and fish catch data from four Cumbrian lakes (Windermere NBAS/SBAS, Esthwaite Water, Blelham Tarn).
  - Time coverage: 1940–2013 (with varying lengths per variable; Fish data from Windermere only; phytoplankton and chlorophyll spanning broader periods).
  - Used to support turning points and early warning analysis; data accompanying Burthe et al. 2015, with authors’ contact recommended prior to reuse.

- Geographic and site details
  - Windermere North Basin (NBAS) and South Basin (SBAS)
  - Esthwaite Water (ESTH)
  - Blelham Tarn (BLEL)
  - Approximate grid references:
    - Windermere NBAS: NY383006
    - Windermere SBAS: SD382914
    - Esthwaite Water: SD358972
    - Blelham Tarn: NY366006

- Data content and formats
  - Four main CSV data files:
    - Windermere_fish_annual_catches.csv
      - Columns: date, site (NBAS/SBAS), Species (Arctic charr, perch, pike), variable (CPUE type), Catch
    - Cumbrian_Lakes_phyto_allsites.csv
      - Columns: month, year, site (BLEL, ESTH, NBAS, SBAS), taxon (genus code), value (cells/ml), counter, chamber, form
    - Cumbrian_Lakes_zoo_allsites.csv
      - Columns: month, year, site, variable (counts for Daphnia, Bosmina, total calanoids, total cyclopoids, total zooplankton filter counts), value (individuals per litre), confound.var
    - Cumbrian_Lakes_chl_allsites.csv
      - Columns: date, month, year, site, variable (TOCA), value (chlorophyll a in mg/m^3), confound.var
  - Data types and formats are CSVs with lake- and taxon-specific coding; sampling is at the deepest point of each lake.

- Sampling design and field methods
  - Frequency: weekly to biweekly sampling at deepest point of each lake.
  - Phytoplankton: water fixed with Lugol’s iodine; counted in Lund chambers; dominant species aggregated to genus level for consistency; key data from 1964–2009 (phytoplankton).
  - Chlorophyll: filtered water (GF/C), methanol extraction, spectrophotometric measurement (Talling protocol); data from 1964–2009.
  - Zooplankton: two data streams
    - Species-level counts (Windermere NBAS) 1979–2010
    – Aggregate crustacean zooplankton counts from all lakes (1964–2009)
  - Fish (Arctic charr, perch, pike)
    - Arctic charr: CPUE from anglers (1966–present) and gill-netting on spawning grounds (1940–present)
    - Perch: standardized trapping (1943–present)
    - Pike: standardized gill-netting since 1982 (1944–present)
    - Sampling effort: ~240 net days/year (since 1990), up to ~348 net days/year (1982–1989)
  - Data processing: for phytoplankton, counts aggregated to genus level to reduce analyst variability; CPUEs calculated as appropriate units per effort (e.g., fish per hour, per net per day, etc.)

- Analytical methods and time framing
  - Phytoplankton and chlorophyll data used to assess primary productivity and phenology; data linked across lakes for multi-taxa analyses.
  - Zooplankton data provide predator-prey context for lower trophic levels.
  - Fish CPUE data enable long-term population trend analyses and links to nutrient/oceanographic changes.
  - All data intended for integration into time-series analyses spanning 1940–2013 to identify turning points and potential early warning signals.

- Data provenance, rights, and usage notes
  - Original data collected by the Freshwater Biological Association (FBA); later managed by CEH and its predecessor IFE.
  - Dataset rights: Database Right/Copyright © NERC - CEH/FBA; re-use requires contacting data authors in Burthe et al. (2015) context.
  - Strong recommendation to contact data authors prior to reuse to ensure proper attribution and data handling.

- Quality, caveats, and applicability
  - Coverage varies by variable and lake; some series are longer than others (e.g., phytoplankton and chlorophyll vs. fish CPUE).
  - Methods and counting practices evolved; certain data (e.g., phytoplankton counts) were consolidated to genus level to improve consistency.
  - Users should account for changes in sampling effort and methodology over time when performing longitudinal analyses.

- Potential uses for data support and exploration
  - Construct integrated multi-taxa time series to study ecosystem responses to eutrophication, climate change, and prey availability.
  - Develop dashboards or self-serve data products combining CPUE, chlorophyll, phytoplankton, and zooplankton metrics.
  - Reproduce or extend turning points and early warning analyses across temperate lake ecosystems.

- Key references and methodological context
  - Burthe et al. (2015) and supporting methodological works cited in the dataset documentation (Lund 1949; Talling 1974, 2003; Thackeray et al. 2013; Winfield et al. 2008a, 2008b).

- Geographic and temporal metadata at a glance
  - Lakes: Windermere NBAS/SBAS, Esthwaite Water, Blelham Tarn
  - Time span: 1940–2013 (variable by data type)
  - Primary data types: phytoplankton, zooplankton, chlorophyll, fish CPUE
  - Data accessibility note: CSV exports with explicit site codes and taxon/sample metadata; usage requires author contact per dataset provenance.