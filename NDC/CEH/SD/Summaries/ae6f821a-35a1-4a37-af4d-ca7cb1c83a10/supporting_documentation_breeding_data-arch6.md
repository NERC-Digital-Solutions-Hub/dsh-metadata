# Supporting documentation for the bird breeding data

## Overview
- Long-running ecological study of great tit population at Wytham Woods; standardized methods since 1947.
- During April–June, 1208 nestboxes were regularly visited to record nest building, first egg date, clutch size, hatch date, number and condition of fledglings, and breeding pair identity.
- Chicks are ringed with BTO metal rings at 15 days old.
- Data from the breeding seasons 2020 and 2021 entered into the Edward Grey Institute (EGI) Bird data Management Project (EBMP).
- Dataset documented here collected by Keith McMahon, Sam Croft, and Kristina Beck.

## Data collection and management
- Data are collected in the field using standardized practices, then entered into EBMP.
- Focuses on breeding events and outcomes within the breeding season; includes multiple quantitative and identity fields.
- Aims to support analysis of breeding success, timing, and parental contributions.

## Dataset details
- Seasons covered: 2020 and 2021.
- Study area: Wytham Woods, Oxford (ecological research site).
- Data provenance: collected by named researchers and stored in EBMP.

## Column metadata and key field meanings
- Pnum: composite code with year, attempt, and nestbox identity (e.g., 20201B1 = 2020 season, first nest in nestbox B1).
- Species: codes for breeding species in the box (b=blue tit, g=great tit, m=marsh tit, c=coal tit).
- State.code (0–6): nest state (0=empty; 1–4 various nest materials/lining; 5=nest built over old one; 6=nest emptied by fieldworker); Close date corresponds to state.code=6.
- Closed: indicates whether a nest state 6 entry was recorded.
- Clear.date: date the nest was closed.
- Suspected.predation: signs of predation observed.
- Lay.date: date of first egg.
- Expected.hatch.date: expected hatch date.
- Hatch.date: actual hatch date.
- Total.egg.weight: weight of eggs (g).
- Num.eggs.weighed: number of eggs weighed.
- Clutch.size: total number of eggs.
- Num.chicks: number of chicks.
- Num.chicks.ringed: number of chicks ringed.
- Num.dead.chicks: number of dead chicks.
- Num.fledglings: number of chicks that fledged.
- Mean.chick.weight: mean weight of chicks (g).
- Father+ Mother: identities of breeding pair.
- Dead.ringed.chick.ids: BTO ring numbers of chicks that died pre-fledging.
- Comments: additional information.
- NAs: indicate missing information (e.g., NA in Father = father not identified; NA in Comments = no comments entered).

## Data quality, limitations, and usage notes
- Data reflect field observations from a defined breeding season window; records may contain missing values (NAs).
- Some fields require interpretation (e.g., Pnum encoding, state codes) to ensure correct data extraction and analysis.
- Standardized methods support cross-year comparisons of timing, clutch size, hatch and fledging success, and parental involvement.

## Access and provenance
- Data managed under the EBMP system at the Edward Grey Institute.
- Dataset documented here pertains to breeding-season data for 2020 and 2021, collected by named researchers.

## References
- Perrins CM, McCleery RH. 1989. Laying dates and clutch size in the great tit. Wilson Bull.:236-253.
- Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.