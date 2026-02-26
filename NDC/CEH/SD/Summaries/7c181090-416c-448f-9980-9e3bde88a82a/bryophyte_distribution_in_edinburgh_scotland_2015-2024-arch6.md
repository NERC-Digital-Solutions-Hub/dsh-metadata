# Bryophytes in an Urban Environment

## Overview
- Data set from the Botanical Society of Scotland's Urban Flora Project (UFP), initiated in 2015.
- Documents distribution of bryophytes (mosses, liverworts, hornworts) in the City of Edinburgh.
- Records species presence/absence and associated habitat across 1x1 km units to understand factors shaping urban species distribution and richness.
- Some data predates the UFP; reflects survey aims to understand urban bryophyte dynamics.

## Spatial coverage
- 138 monads (1x1 km squares) defined by the Ordnance Survey National Grid.
- Survey area largely within the A720 Edinburgh city ring road, extending southwest to the Water of Leith (Currie, Balerno), north to Cramond Island, and east to Joppa.

## Experimental design / data collection
- Route chosen per monad to maximize ecological diversity in public spaces and waste ground; steep/private areas largely excluded.
- Each monad surveyed at least once; repeat visits to particularly species-rich monads.
- 272 bryophyte species recorded as present or absent across the 138 monads.
- Species names aligned with the UK Species Inventory for standardisation.

## Data files and structure
- Species_by_monad.csv: records species presence (1) or absence (0) in each monad; includes Ordnance Survey grid references for monads.
- Species_location_habitat_date.csv: expanded dataset with species location, habitat context, and date; includes site name, original and 4-figure OS grid references, decimal latitude/longitude, habitat code, secondary habitat notes, and date recorded.
- Habitat codes (Table 3) map to broad habitat categories (agricultural, building/structures, crags/quarries, derelict/waste ground, gardens/parks/grounds, heath/moor, inland water, marine/coastal, roads/paths/pavement, woodland/hedgerow) with subcategories.

## Quality control
- All recorders were experienced bryologists who consulted others for species identity confirmation.
- Species locations verified against maps to ensure accuracy.

## Temporal scope and provenance
- Some data precede the UFP era; overall survey activity documented within the UFP framework.
- Cited in Bryophytes in an Urban Environment (Chamberlain & Wilson); full reference pending.

## Usage and applications
- Enables analysis of urban bryophyte patterns by monad and habitat context.
- Supports data products such as dashboards, pivot tables, and maps to enable self-service exploration.
- Can be combined with other urban habitat data to study drivers of species richness and distribution in cities.
- Suitable for informing urban biodiversity policy and public-facing data releases.