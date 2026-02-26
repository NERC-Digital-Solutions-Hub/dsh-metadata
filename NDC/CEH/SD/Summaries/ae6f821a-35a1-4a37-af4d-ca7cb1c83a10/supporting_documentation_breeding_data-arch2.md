# Supporting documentation for the bird breeding data

## Aim and scope
- Document provides details for the bird breeding dataset collected at the study site.
- Regular visits (April–June) to 1208 nestboxes to record nest-building, first egg date, total eggs, hatch date, fledgling counts, and breeding pair identity.
- Great tit population studied with standardized methods since 1947.
- Data are collected and entered into the Edward Grey Institute (EGI) Bird Data Management Project application (EBMP).
- Dataset covers breeding seasons 2020 and 2021, contributed by Keith McMahon, Sam Croft, and Kristina Beck.

## Data collection protocol
- Nestbox visits conducted during the breeding season to collect comprehensive breeding data.
- All chicks ringed with a BTO metal leg ring at 15 days old.
- Fieldwork outputs are recorded in EBMP, ensuring consistency with long-term monitoring practices.

## Data structure and coding
- Pnum: composite field encoding year, breeding attempt, and nestbox identity (e.g., '20201B1' = 2020 season, first nest in box B1).
- Species codes: b = blue tit, g = great tit, m = marsh tit, c = coal tit.
- State.code: nest state (0–6) with meanings:
  - 0 = empty nest
  - 1–4 = nest material and lining stages
  - 5 = nest built over an old one
  - 6 = nest emptied by a fieldworker or fledging
- Closed: indicates whether state.code=6 was recorded for a nest.
- Clear.date: date when the nest was closed.
- Suspected.predation: signs of predation recorded.
- Lay.date, Expected.hatch.date, Hatch.date: key timing metrics.
- Clutch.size, Total.egg.weight, Num.eggs.weighed, Num.chicks, Num.chicks.ringed, Num.dead.chicks, Num.fledglings, Mean.chick.weight: various quantitative measures.
- Father+ Mother: identities of breeding pair.
- Dead.ringed.chick.ids: ring IDs of chicks that died before fledging.
- Comments: additional notes; NA indicates missing data.
- NA handling: NA entries denote missing or not recorded data.

## Dataset content and variables
- Data captured per nestbox per breeding attempt, including:
  - Nest state progression and final outcome
  - Timing data (lay, hatch, fledging)
  - Reproductive metrics (clutch size, egg/chick weights, numbers weighed)
  - Parental identities and fledgling outcomes
  - Ringing status and mortality information
  - Additional observational notes

## Provenance and context
- Long-running ecological monitoring lineage demonstrated by references:
  - Perrins CM, McCleery RH. 1989. Laying dates and clutch size in the great tit.
  - Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory.
- Site: Wytham Woods; purpose aligned with environmental monitoring and ecological research.

## Data management and accessibility
- Data collected for monitoring and quality assurance are entered into EBMP.
- Datasets are stored and uploaded to appropriate data portals, enabling standardised access and sharing.

## Potential uses for environmental monitoring and policy assessment
- Facilitates assessment of long-term breeding performance and population dynamics (timing, clutch size, fledgling success).
- Supports standardised reporting and comparison across years and studies.
- Enables integration with other datasets to enhance environmental health analyses and policy evaluations.