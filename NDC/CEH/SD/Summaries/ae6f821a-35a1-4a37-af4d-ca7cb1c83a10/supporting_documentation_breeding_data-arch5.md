# Supporting documentation for the bird breeding data

## Overview
- Long-running, standardized study of the great tit population at Wytham Woods; methods in use since 1947.
- During Apr–Jun, 1208 nestboxes were regularly visited to collect breeding data (nest building, first egg date, clutch size, hatch date, fledgling numbers, and breeding pair identities).
- Chicks ringed at 15 days; data entered into the Edward Grey Institute Bird Data Management Project (EBMP).
- Dataset covers breeding season 2020 and 2021; contributors: Keith McMahon, Sam Croft, Kristina Beck.

## Data collection and scope
- Nestbox-level records include species (b, g, m, c), nest state (state.code 0–6 with defined meanings), freshness of renovations, predation indicators, and nest closure dates.
- Key timing data: lay date, expected hatch date, hatch date; outcome metrics: clutch size, total eggs weighed, number of chicks, chicks ringed, dead chicks, fledglings, mean chick weight.
- Breeding pair identities (Father, Mother); can include missing data (NA) when unknown.
- Post-processing notes: Dead ringed chick IDs captured when applicable; comments field for additional information.
- Data quality notes: NAs indicate missing or not entered information.

## Data structure and metadata
- Pnum column encodes year, attempt, and nestbox identity (e.g., 20201B1 = 2020, first nest recorded in nestbox B1).
- Species codes: b = blue tit, g = great tit, m = marsh tit, c = coal tit.
- State.code meanings (0–6) range from empty nest to emptied by fieldworker; 6 marks nest emptied after fledging.
- Key fields: Lay.date, Expected.hatch.date, Hatch.date, Clutch.size, Num.chicks, Num.chicks.ringed, Num.dead.chicks, Num.fledglings, Mean.chick.weight, Father, Mother, Dead.ringed.chick.ids, Comments.
- Data quality indicators: NAs denote missing information (e.g., NA in Father = father identity not identified; NA in Comments = no comments entered).

## Data management, standards, and governance
- Data are managed within the EBMP system, consistent with long-standing standardized methods.
- Emphasizes accuracy, consistency, proper metadata, and standardized formats to support interoperability and reuse.
- Documentation of data processing may accompany the dataset to aid reuse and understanding.

## Sharing, access, and updates
- Datasets are intended to be uploaded to relevant portals and catalogued as part of data holdings.
- Ongoing data collection and potential updates imply an established process for incorporating new records and maintaining discoverability.
- Any data sharing should respect limitations (e.g., predation signs, encryption of sensitive fields) and ensure proper versioning.

## Practical notes for data stewardship
- Ensure alignment with user needs by maintaining clear, machine-readable metadata and code lists (species, state codes).
- Maintain data provenance: link data back to collectors (McMahon, Croft, Beck) and the EBMP system.
- Monitor and manage incomplete areas (e.g., missing parental identities or comments) and document reasons for gaps.
- Prepare for interoperability with other nestbox or long-term avian datasets by preserving encoding schemes (Pnum, state.code, species codes).
- Document processing steps and any transformations applied to raw data prior to sharing.

## References
- Perrins CM, McCleery RH. 1989. Laying dates and clutch size in the great tit. Wilson Bulletin: 236-253.
- Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.