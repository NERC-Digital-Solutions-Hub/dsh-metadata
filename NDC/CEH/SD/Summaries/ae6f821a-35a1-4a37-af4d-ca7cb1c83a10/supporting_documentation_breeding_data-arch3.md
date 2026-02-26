# Supporting documentation for the bird breeding data

- Overview of the data collection
  - All 1208 nestboxes at the study site were visited regularly in April–June to record nest building, first egg date, number of eggs, hatch date, number of fledglings, and the identity of the breeding pair.
  - The great tit population at Wytham Woods has been studied with standardized methods since 1947.
  - Chicks are ringed with a BTO metal leg ring at 15 days old.
  - Data collected during and at the end of the breeding season are entered into the Edward Grey Institute (EGI) Bird data Management Project application (EBMP).
  - Dataset covers breeding seasons 2020 and 2021, created by Keith McMahon, Sam Croft, and Kristina Beck.

- Dataset structure and column descriptions
  - Pnum: encodes year, attempt, and nestbox identity (e.g., '20201B1' = 2020, first recorded nest in B1).
  - Species: codes for breeding species in the box (b = blue tit, g = great tit, m = marsh tit, c = coal tit).
  - State.code: nest state 0–6 (0 = empty; 1–4 = partial nest materials; 5 = nest built over an old one; 6 = nest emptied by a fieldworker).
  - Closed: whether state.code 6 was entered; Clear.date: date the nest was closed.
  - Suspected.predation: signs of predation.
  - Lay.date: date of first egg; Expected.hatch.date; Hatch.date.
  - Totals and measurements: Total.egg.weight (grams); Num.eggs.weighed; Clutch.size; Num.chicks; Num.chicks.ringed; Num.dead.chicks; Num.fledglings; Mean.chick.weight.
  - Parent identities: Father+ Mother; Dead.ringed.chick.ids (ring IDs of chicks that died before fledging); Comments (additional information).
  - NAs: meanings include missing father identity or missing comments.

- Data management and provenance
  - Data are entered into EBMP during/after the breeding season, enabling standardized management and sharing.
  - Metadata availability and completeness may vary; some fields may require interpretation or transformation for use in analyses.
  - Data originate from field observations and are linked to original dataset sources.

- Quality, governance and usage considerations
  - Strengths for monitoring frameworks: standardized long-running methodology, explicit field definitions, and traceable data lineage via EBMP.
  - Potential barriers: incomplete metadata, data access considerations, and the need to transform formats for some analyses.
  - The dataset supports monitoring of breeding phenology, clutch size, chick survival, and growth metrics, and contributes to long-term evaluations of the Wytham Woods great tit population.

- Context and references
  - Wytham Woods described as Oxfordshire’s ecological laboratory.
  - Foundational references: Perrins and McCleery (1989) on laying dates and clutch size; Savill et al. (2011) on Wytham Woods as an ecological laboratory.