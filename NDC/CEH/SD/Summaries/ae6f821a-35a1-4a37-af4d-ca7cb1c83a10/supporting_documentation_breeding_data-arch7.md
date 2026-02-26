# Supporting documentation for the bird breeding data

## Overview
- Regular nestbox visits (Apr–Jun) for 1208 nestboxes at the study site to record nest-building, first egg date, clutch size, hatch date, fledgling numbers and breeding pair identity.
- Great tit population studied with standardized methods since 1947.
- Chicks ringed with BTO metal rings at 15 days old.
- Data entered into the Edward Grey Institute Bird Data Management Project (EBMP) during and after the breeding season.
- Dataset covers breeding season data for 2020 and 2021, contributed by Keith McMahon, Sam Croft, and Kristina Beck.
- References for methods and site context: Perrins & McCleery (1989); Savill et al. (2011).

## Data structure and columns (key details)
- Pnum: concatenates year, attempt, and nestbox identity (example: 20201B1 = 2020, first recorded nest in nestbox B1).
- Species: coding for breeding species in the box (b = blue tit, g = great tit, m = marsh tit, c = coal tit).
- State.code: nest state (0–6; 0 = empty nest; 1–4 = nesting materials/lining; 5 = nest built over old one; 6 = nest emptied by fieldworker).
- Closed: indicates whether state.code 6 entry was recorded.
- Clear.date: date the nest was closed.
- Suspected.predation: signs of predation observed.
- Lay.date: date of first egg.
- Expected.hatch.date and Hatch.date: predicted and actual hatch dates.
- Total.egg.weight and Mean.chick.weight: weights recorded for eggs and chicks.
- Num.eggs.weighed, Clutch.size, Num.chicks, Num.chicks.ringed, Num.dead.chicks, Num.fledglings: counts related to eggs, chicks, and fledging.
- Father + Mother: identities of breeding pair.
- Dead.ringed.chick.ids: BTO ring numbers of chicks that died before fledging.
- Comments: additional information.
- NAs: missing information (e.g., NA in Father means father identity not identified; NA in Comments means no comments entered).

## Data management and provenance
- Data captured during the breeding season and entered into EBMP.
- Dataset consolidates breeding-season observations for 2020 and 2021.

## GIS and data-use implications
- Nestbox locations and nestbox IDs enable spatial mapping of breeding activity and nest states across the study site.
- Temporal data (Lay.date, Hatch.date, fledging dates) supports phenology analyses and time-series mapping.
- Species and breeding-pair information allow spatial analyses of species distribution and social structure.
- State.code and Clear.date facilitate mapping of nest occupancy and nesting progression.
- Data can be integrated with other spatial layers (e.g., habitat, land cover) by nestbox ID and year.
- Missing data (NA) and coding conventions (Pnum, State.code) should be handled during data cleaning and transformation for GIS workflows.

## References
- Perrins CM, McCleery RH. 1989. Laying dates and clutch size in the great tit. Wilson Bulletin: 236-253.
- Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological Laboratory. Oxford University Press.