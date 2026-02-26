# NERC Soil Biodiversity Thematic Programme

## Overview
- The NERC Soil Biodiversity Thematic Programme (established 1999) studied a large field experiment at Sourhope, Macaulay/Hutton Institute farm in the Scottish Borders (grid NT8545019630), focusing on aboveground biomass, species composition, and soil biota functions.
- Aimed to understand soil biodiversity and the roles of soil organisms in ecological processes.
- Funded 24 projects on soil structure, soil processes (carbon and nitrogen cycles), micro-fauna and flora, meso- and macro-fauna.
- Data described here pertain to treatment details and can be used with other experimental datasets from the site as explanatory variables.

## Data asset and dataset
- Dataset: P2109_VIEW_SOIL_TREATMENTS.csv detailing treatments applied to Sourhope soil plots from 1999–2001, with additional data for 2001–2004.
- Purpose: support analysis of treatments as explanatory variables in conjunction with other site datasets.
- Reference: Scott et al., 2003 (SOURHOPE FIELD DATA HANDBOOK 2003). Available via EIDC catalogue.

## Dataset structure and key fields
- Columns:
  - TREATMENT_DATE
  - BLOCK (1–5)
  - MAIN_PLOT (A–F)
  - SUB_PLOT
  - CELL_X (grid X)
  - CELL_Y (grid Y)
  - TREATMENT_TYPE
  - DOSAGE
- Notes: See Scott et al., 2003 for plot layout and coding.

## Site-level treatments (vegetation management)
- Vegetation cutting (Cut 1–5) with specific windows:
  - Cut 1: 1999 (1–9 Jun), 2000 (8–12 May), 2001 (5–18 May, with asterisk), 2002 (20–27 May)
  - Cut 2: 1999 (29 Jun–5 Jul), 2000 (5–9 Jun), 2001 (4–8 Jun), 2002 (17–26 Jun)
  - Cut 3: 1999 (26–29 Jul), 2000 (3–7 Jul), 2001 (3–18 Jul, with asterisk), 2002 (15–19 Jul)
  - Cut 4: 1999 (23–26 Aug), 2000 (31 Jul–4 Aug), 2001 (6–14 Aug), 2002 (19–26 Aug)
  - Cut 5: 1999 (21–25 Sep), 2000 (28–31 Aug), 2001 (4–11 Sep), 2002 (24 Sep–1 Oct)
- Note: (*) indicates periods where mower was unavailable due to mechanical breakdown.

## Plot-level treatments
- 1. Control 1 — No treatment
- 2. Control 2 — No treatment
- 3. Nitrogen — Applied as NH4NO3 (ICI NITRAM granular fertilizer; Total N 34%, Ammonical N 17.2%, Nitric N 17.3%)
  - Annual rate: 24 g m-2 (5.76 kg per plot; 240 kg ha-1)
  - Applied in two doses
  - Yearly timing:
    - 1999: Spring (2–3 Apr) and Late Summer (28–29 Sep)
    - 2000: Spring (17–18 Apr) and Late Spring (16 May)
    - 2001: Spring (11–12 Apr) and Late Spring (23–25 May)
    - 2002: Spring (8–9 Apr) and Late Spring (1–2 May)
- 4. Lime — Applied as CaCO3 (powdered lime; 39.4% Calcium; ASH insoluble in HC 0.5%)
  - Annual rate: 600 g m-2 (144 kg plot-1; 6000 kg ha-1)
  - Applied in one dose
  - Yearly timing: Spring (varied dates per year)
    - 1999: 7–20 May
    - 2000: 5–10 May
    - 2001: 17–26 Apr
    - 2002: 10–17 Apr
- 5. Nitrogen and Lime — Combined N & L treatments as above
- 6. Insecticide — Dursban 4 OPA insecticide (ex Dow Chemicals)
  - Rate: 0.15 ml m-2 (36 ml in 10 L plot-1; 1.5 L ha-1)
  - Annual rate: 7.5 L ha-1
  - Applied after each mowing when weather permitted
  - Yearly applications:
    - 1999: 16 Jul, 6 Aug, 3 Sept, 30 Sept
    - 2000: 15 May, 14 Jun, 18 Jul, 11 Aug, 1 Sept
    - 2001: May timing skipped; 12 Jun, 21 Jul, 16 Aug, 13 Sept
    - 2002: 28 May, 27 Jun, 25 Jul, 27 Aug, 3 Oct

## Data provenance, scope, and usage notes
- Data subject to quality assurance but not warranted by NERC for accuracy or fitness for any particular use.
- NERC disclaimers: no liability for accuracy or reliability; data provided without guarantee of suitability for user purposes.
- The dataset can be integrated with other experimental datasets from Sourhope for explanatory analyses in GIS contexts.

## GIS considerations and usage
- Spatial framework: grid-based cell coordinates (CELL_X, CELL_Y) enabling mapping of treatment impacts at plot-level resolution.
- Useful for visualizing spatial patterns of treatments (e.g., nitrogen, lime, insecticide) and vegetation-cut regimes across the Sourhope site.
- Aligns with other site datasets to model relationships between soil biodiversity, treatment regimes, and ecological processes.