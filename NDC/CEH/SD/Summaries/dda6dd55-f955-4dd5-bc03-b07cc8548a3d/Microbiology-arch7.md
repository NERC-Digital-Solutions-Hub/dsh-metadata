# Procedure for enumeration, isolation, preservation and identification of E. coli isolates NERC project NE/N019555/1

## Overview
- Describes a step-by-step workflow to enumerate, isolate, preserve, and confirm E. coli isolates that are resistant to third-generation cephalosporins or carbapenems from fecal, soil, water, wastewater, and related samples.
- Includes media preparation, sample processing, culture conditions, isolation procedures, and confirmatory testing (API 20E).

## Materials and media
- Buffers and reagents: PBS (1 L), cefotaxime, meropenem
- Agar media: CHROMagar ESBL, CHROMagar KPC, MacConkey, TBX
- Preservation: Tryptone soy broth with 30% glycerol, LifeGuard Soil Preservation solution
- Identification: API 20E kit
- Ancillary: filter papers, sterile petri dishes, cryovials, media bottles, inoculation loop
- Equipment: refrigerator (2-8 °C), freezer (-20 °C, -80 °C), autoclave, water bath (40-100 °C), incubator (36 ± 2 °C), shaker

## Preparation of media and stock solutions
- Prepare 1 L of 10× PBS, then dilute to 1× PBS. Autoclave 121 °C for 15 min.
- Prepare 1 L CHROMagar ESBL and 1 L CHROMagar KPC plates with corresponding supplements, ensuring fresh supplement solutions (used the same day) and proper protection from light; plates usable for short-term storage.
- Prepare TBX medium, MacConkey with antibiotic supplements (cefotaxime or meropenem), including cefotaxime (2 mg/mL) and meropenem (10 mg/mL) stock solutions for selective media.
- Prepare appropriate dilutions and inoculation materials for sample types.

## Sample types and processing
- Fecal (human/poultry), solid waste, and soil
  - Suspend 1–5 g in 9–45 mL sterile PBS, vortex 1 min, settle 15 min.
  - Make 1 mL suspension, perform serial dilutions in PBS.
  - Inoculate 0.1 mL onto CHROMagar ESBL, CHROMagar KPC, and TBX plates by spread plating.
  - Incubate at 37 °C for 18–24 h.
  - Identify typical E. coli colonies (dark pink to reddish) and subculture at least 3 isolated colonies onto MacConkey with cefotaxime or meropenem as appropriate.
  - Prepare a culture sweep from MacConkey plates, suspend in TSB with 30% glycerol, store at -80 °C.
- Water supplies (tap/tubewell)
  - Filter 2×100 mL through 0.22 µm membranes onto mTEC plates (cefotaixme 1 mg/L; meropenem 0.5 mg/L).
  - Incubate 37 °C for 2 h, then 44 °C for 18 h.
  - If >200 CFU, perform additional dilutions and repeat.
  - Count reddish-purple/magenta E. coli colonies, subculture at least three colonies onto MacConkey with the same antibiotics, store the sweep at -80 °C.
- Waste water
  - Take 20 mL and make 9-fold dilutions; filter through membranes onto mTEC plates with antibiotics as above.
  - Incubate as above, count colonies, subculture as above, store at -80 °C.

## Confirmation and identification of E. coli
- API 20E confirmation
  - Perform oxidase test; E. coli is oxidase-negative.
  - Prepare a fresh bacterial suspension from a colony on MacConkey; inoculate API-20E strip wells (including CIT, VP, GEL; add mineral oil to ADH, LDC, ODC, H2S, URE).
  - Incubate at 36 ± 2 °C for 18–24 h.
  - Read results using the API-20E reading table; if fewer than 3 positive tests after initial incubation, incubate an additional 24 ± 2 h.
  - For first-time reagent use, follow preparation steps for reagents; interpret reactions (e.g., TDA, VP, NIT tests) per kit instructions.
  - Identify organism using APIweb; if unidentifiable, perform additional tests (Nitrate Reduction test, MacConkey growth) as needed.
- Isolate testing rule
  - Test one E. coli isolate from each sample; if presumptive E. coli is negative by API20E, test a second isolate from that sample for confirmation.

## Data and results handling
- Outputs include:
  - Colony counts and morphological notes on selective plates.
  - Isolates stored at -80 °C, with associated sample IDs and plate metadata.
  - API-20E identification results and any supplementary tests for confirmation.
- Documentation should capture sample type, processing steps, incubation conditions, and results to support downstream data analysis and GIS mapping.

## Quality, safety, and notes
- Freshness and timing of supplement preparations are critical; use reconstituted supplement solutions the same day.
- Plates should be protected from light and dehydration; prepared media plates usable for limited storage.
- Follow strict labeling (sample ID, date, agar type) and consistent data recording for integration with spatial datasets.
- Procedures emphasize starting with a single E. coli confirmation per sample, with a plan for re-testing when necessary to confirm identity.

## GIS and data integration considerations
- Link each isolate to precise sampling location (coordinates), sample type, date/time, and processing steps to enable spatial analysis of ESBL/KPC prevalence.
- Maintain standardized metadata for interoperability across datasets and mapping applications.
- Ensure traceability from initial sample to final identification to support temporal and geographic trend analyses.