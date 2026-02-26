# Supporting documentation for the bird breeding data

## Overview
- Study site: Wytham Woods; focus on the great tit population.
- Long-running, standardized research since 1947 (Perrins and McCleery 1989; Savill et al. 2011).
- During April–June, 1208 nestboxes were visited to record nest-building, lay date, clutch size, hatch date, fledgling counts, and breeding pair identities.
- Chicks are ringed with BTO metal rings at 15 days old.
- Data collected each breeding season are entered into the Edward Grey Institute (EGI) Bird Data Management Project application (EBMP).
- Dataset covers breeding seasons 2020 and 2021, contributed by Keith McMahon, Sam Croft, and Kristina Beck.

## Data collection and scope
- Regular visits of 1208 nestboxes during the breeding season to collect comprehensive breeding metrics.
- Data capture includes timing, quantity, outcomes, and parental identities for each breeding attempt.
- Nest outcomes tracked through to fledging or nest clearance by field staff.

## Data management and entry
- All data entered into EBMP (EGI Bird Data Management Project) during and after the breeding season.
- The dataset provides structured, codified information suitable for analysis and linking with historical data.

## Variables and coding (key columns)
- Pnum: encodes year, attempt, and nestbox identity (e.g., 20201B1 = 2020, first nest in nestbox B1).
- Species codes: b = blue tit, g = great tit, m = marsh tit, c = coal tit.
- State.code: nest state (0–6) with 0 = empty nest, 1–4 = various nest materials/lining, 5 = nest built over an old one, 6 = nest emptied by fieldworker.
- Closed: indicates whether state.code 6 was entered.
- Clear.date: date the nest was closed.
- Suspected.predation: signs of predation.
- Lay.date: date of first egg.
- Expected.hatch.date, Hatch.date: predicted and actual hatch dates.
- Clutch.size: number of eggs.
- Total.egg.weight: weight of eggs in grams.
- Num.eggs.weighed: number of eggs weighed.
- Num.chicks: number of chicks present.
- Num.chicks.ringed: number of chicks ringed.
- Num.dead.chicks: number of dead chicks.
- Num.fledglings: number of chicks that fledged.
- Mean.chick.weight: average weight of chicks.
- Father, Mother: identities of breeding pair.
- Dead.ringed.chick.ids: BTO ring numbers of chicks that died before fledging.
- Comments: any additional information.
- NAs: indicate missing information (e.g., NA for Father means father identity was not identified; NA in Comments means no entry).

## Data quality and notes
- Data reflect careful, standardized field methods and longitudinal study practices.
- Encoding schemes (Pnum, state codes, species codes) facilitate integration with older datasets and cross-season analyses.
- Missing data explicitly labeled as NAs, enabling transparent data cleaning and imputation planning.

## Usage context and references
- The dataset is part of a long-term ecological data collection program at Wytham Woods, contributing to understanding breeding phenology, clutch size, survival, and related dynamics.
- Foundational references: Perrins CM, McCleery RH. 1989; Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.