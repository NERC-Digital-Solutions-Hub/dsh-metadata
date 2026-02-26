# Supporting documentation for the bird breeding data

## Overview
- Regular visits (April–June) to 1208 nestboxes at the study site to record breeding events.
- Long-running study of the great tit at Wytham Woods using standardized methods since 1947.
- Data entered into the Edward Grey Institute (EGI) Bird data Management Project application (EBMP) during and after the breeding season.
- Dataset covers breeding seasons 2020 and 2021, contributed by Keith McMahon, Sam Croft, and Kristina Beck.

## Data collection scope and events
- Recorded events per nestbox: nest building, date of first egg, total eggs, hatch date, number and condition of fledglings, and identity of the breeding pair.
- Chicks are ringed with a BTO metal leg ring at 15 days old.
- Information captured/during the season and at season end includes a comprehensive set of metrics related to breeding success and timing.

## Data schema and metadata (key columns)
- Pnum: encodes year, attempt, and nestbox identity (e.g., 20201B1 for 2020, first recording in nestbox B1).
- Species: code for breeding species (b=blue tit, g=great tit, m=marsh tit, c=coal tit).
- State.code: nest state (0–6) with meanings from empty to fledged/closed; Closed indicates state.code=6 entry.
- Date fields: Lay.date, Expected.hatch.date, Hatch.date, Clear.date.
- Suspected.predation: signs of predation.
- Clutch metrics: Total.egg.weight, Num.eggs.weighed, Clutch.size, Num.chicks, Num.chicks.ringed, Num.dead.chicks, Num.fledglings, Mean.chick.weight.
- Parental IDs: Father+Mother (breeding pair identities); Dead.ringed.chick.ids (ring numbers of chicks that died pre-fledge).
- Comments: supplementary information.
- NA handling: NA in fields like Father or Comments indicates missing data.
  
## Data management and provenance
- Data managed within EBMP, ensuring standardized entry for breeding-season data.
- Clear documentation of column definitions to support data discovery, interpretation, and reuse.
  
## Access, usage, and references
- Dataset derived from long-running, standardized field methods; supports longitudinal analyses of breeding timing and success.
- Foundational references for the study background: Perrins & McCleery (1989) and Savill et al. (2011).