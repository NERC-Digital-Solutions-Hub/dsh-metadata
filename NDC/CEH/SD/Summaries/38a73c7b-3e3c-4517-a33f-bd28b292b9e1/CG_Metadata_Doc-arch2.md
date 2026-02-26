# Survey of British calcareous grasslands, 1990 and 2007

- Purpose: A national, repeatable survey of calcareous grasslands in Britain to document vegetation and soil characteristics across sites representative of calcicolous ecosystems, enabling monitoring of environmental health and policy performance over time.
- Timeframe and coverage:
  - 1990 survey: 128 plots across 56 sites (1990–1993)
  - 2007 resurvey: 48 plots across 35 of the original sites (2006–2009)
  - Geographic scope: Britain

- Survey design and methods:
  - Plot layout: Standardised 12 × 12 m plots (often 12 × 12 m, some 6 × 24 m) with a 12 × 12 m grid subdivided into four 6 × 6 m blocks and further into nine 2 × 2 m units.
  - Quadrat sampling: Within each plot, 36 sub-quadrats (0.5 × 0.5 m) sampled to record vegetation frequency (presence/absence) across 36 quadrats.
  - Relocation markers: Permanent copper loop markers buried 5–15 cm to enable precise relocation (approx. 5 cm accuracy).
  - Site selection: 56 sites chosen for representativeness of calcareous grasslands, with stable management and ownership; plots placed to capture variation in aspect, altitude, climate gradient, and deposition.
  - Time to record: 3–12 hours per plot; grid setup about 45 minutes.
  - Data handling: Data managed using VESPAN II; frequency-based data used to derive constancy classes and compare with British Plant Communities (NVC) profiles.

- Vegetation data (1990 and 2007):
  - Taxa recorded: Vascular plants, bryophytes (1990 included bryophytes and macrolichens; 2007 did not), and growth form classification (grasses, other herbs, lower plants, etc.).
  - Recording approach: Qualitative presence within each of the 36 quadrats; dominant species and specific cover notes for key taxa.
  - Documentation: Vouchers for difficult taxa; detailed notes on recording issues to aid interpretation.
  - Output handling: Data prepared for machine processing with standardised forms and checked for consistency; use of MATCH and VESPAN II alignment with NVC concepts.

- Soil data:
  - 1990: In-field pH of top 10 cm (slurry method).
  - 2007: Soil sampled at each plot (top 10 cm) with five subsamples composited; samples stored at 4°C and analysed in the lab.
  - Analyses (2007): pH (water extracts), plant-available phosphorus (Olsen-P), nitrate and ammonium via extracts, base cations (Ca, Na, Mg, K) and Al, using ICP; soil organic matter by loss on ignition.
  - Sample handling: All extracts stored at 4°C; moisture-corrected values applied where appropriate.

- Data products and datasets:
  - CG_SITES.csv: Site-level information (plot IDs, site name, status, year, coordinates, NVC, soil properties, topography, management notes, etc.).
  - CG_VEG.csv: Vegetation species recorded per plot-year, with taxon identifiers, growth forms, and counts (presence/absence across 36 quadrats per plot).
  - CG_SITES.csv fields include: plot_id, site, status, year, grid references, NVC, soil pH, altitude, aspect, slope, coastal status, soil type, organic content, ammonium, nitrate, average soil depth, and notes.
  - CG_VEG.csv fields include: plot_id, year, species_rec, BRC_NUM/BRC_NAME (linked plant records), count, growth form.
  - Note: 999 indicates no data; 0/1 indicators used for binary site characteristics (e.g., coastal, scree).

- Data provenance and access:
  - Origin: 1990 DoE contract (T.C.G. Rich, E.A. Cooper, J.S. Rodwell, A.J.C. Malloch); 2007 NERC grant (multiple authors).
  - Key publications and datasets: 
    - Rich et al. (1993) on climate change and air pollution effects on British calcicolous ecosystems (Final report to UK DoE).
    - Van Den Berg et al. (2011) on nitrogen deposition effects on species composition in calcareous grasslands.
    - Rich et al. (2015) Survey of British calcareous grasslands, 1990 and 2007 (NERC Environmental Information Data Centre; DOI provided).
  - Data access: NERC Environmental Information Data Centre (EIDC) with DOI: 10.5285/38a73c7b-3e3c-4517-a33f-bd28b292b9e1.

- Strengths and intended use for monitoring:
  - Standardised, repeatable sampling designed to minimize observer bias and enable long-term environmental health assessment.
  - Frequency-based vegetation data aligned with British Plant Communities (NVC) frameworks; suitable for detecting patterns related to climate, pollution, and management.
  - Comprehensive soil measurements provide context for plant community change and nutrient dynamics.

- Limitations and caveats:
  - Cover estimates are limited; data are predominantly presence/absence within quadrats.
  - Relocation and marker loss risk (though copper loops mitigate this) and datasets unique in method, limiting direct comparability with other datasets.
  - Less comprehensive bryophyte data in 2007 compared with 1990; some taxa under-represented due to recording constraints.

- Practical relevance for analysts:
  - Enables tracking of environmental health indicators and policy performance through vegetation and soil metrics across Britain.
  - Provides a structured framework to integrate additional datasets (e.g., deposition, climate) for multi-source environmental analysis.
  - Datasets are suitable for spatial and temporal trend analyses, with explicit metadata and standardized data formats.