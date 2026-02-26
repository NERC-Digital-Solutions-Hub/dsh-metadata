# Bryophytes in an Urban Environment, a case study from Edinburgh

## Overview
- Part of the Botanical Society of Scotland's Urban Flora Project (UFP), initiated in 2015.
- Dataset on the distribution of bryophytes (mosses, liverworts and hornworts) in the City of Edinburgh.
- Records species presence/absence and associated habitat per 1x1 km monad; includes some data predating UFP.
- Aimed at understanding factors underlying species distribution and species richness in urban environments.

## Spatial Coverage
- 138 monads (1x1 km squares) defined by the Ordnance Survey National Grid.
- Survey area mainly within the A720 Edinburgh ring road; extended southwest along the Water of Leith to Currie and Balerno; north to Cramond Island; east to Joppa.

## Experimental Design and Data Collection
- A route through each monad was chosen to maximize ecological diversity in public spaces and waste ground; steep ground largely excluded; few private gardens surveyed.
- Each monad surveyed at least once; repeat visits to particularly species-rich monads.
- 272 bryophyte species recorded as present/absent across 138 monads.
- Some older data included for precipitous locations on unstable crags and steep ground.
- Species names follow the UK Species Inventory.

## Data Files and Structure
- (i) Species_by_monad.csv
- (ii) Species_location_habitat_date.csv

Data elements:
- Species_by_monad.csv
  - For each monad: species name, presence (1) or absence (0); OS grid reference for the monad.
  - Includes taxon abbreviation and standardized species naming.
- Species_location_habitat_date.csv
  - Expanded data: species name, taxon group (Moss, liverwort, hornwort), site name, original OS grid reference, 4-figure grid ref (1x1 km resolution), latitude, longitude, habitat code, any secondary habitat notes, and date recorded.
- Habitat codes (Table 3) provide detailed subcategories for each major habitat type.

Quality control:
- All recorders were highly experienced bryologists; identity confirmed via consultation when needed.
- Species locations validated by map checks.

## Habitat Coding (Table 3)
- Broad categories and subcategories include:
  - Agricultural (fields, fallow, grassland, other crops)
  - Building and walls (gravestones/monuments, other structures)
  - Crags and quarries (natural crags, quarries)
  - Derelict and waste ground (coal bings, derelict buildings, waste dumps)
  - Gardens, parks and grounds (allotments, carparks, churchyards, parks, schools)
  - Heath, moor and grassland (heath/moor habitats)
  - Inland water and wetlands (bog, canal, ditch, fen, lakes, marsh, rivers)
  - Marine and coastal (beach, cliffs, coastal path, marina, saltmarsh)
  - Roads, paths and pavement (footpaths, pavements, railways)
  - Woodland, scrub and hedgerow (conifer/deciduous woodland, hedgerows, tree lines)
- Each major category contains subcategories to capture habitat specificity.

## Data Provenance and Usage
- Data cited in: Chamberlain, DF, and Wilson, J. Bryophytes in an Urban Environment, a case study from Edinburgh. Plant Ecology and Diversity. Full reference pending.
- Dataset supports analysis of urban bryophyte distribution and factors influencing species richness, suitable for monitoring environmental health and urban biodiversity over time.