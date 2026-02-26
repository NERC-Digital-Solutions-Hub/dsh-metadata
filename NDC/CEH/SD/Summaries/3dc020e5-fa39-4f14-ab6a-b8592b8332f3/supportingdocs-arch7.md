# Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

## Overview
- Four CSV data files documenting biological (invertebrate abundances) and physical–chemical measurements from peatland ponds in the Pennine hills, northern England.
- 105 ponds across six peatlands, surveyed 2012–2014 to study colonisation, community changes (alpha/beta diversity), and associations with physico-chemical variables during peatland rewetting/restoration.
- Spatial points with extensive site metadata; pond-level time series and chrono/ natural-pond distinctions.

## What was recorded and data formats
- Biological data: invertebrate abundances per pond (mostly species-level where possible).
- Physical data: geographic data, pond morphology (dimensions, volume), altitude, aspect.
- Chemical data: dissolved ions, nutrients, pH, dissolved organic carbon, and related solutes.
- Data stored in four CSV files with structured columns (pond codes used to link datasets). Five pH values missing due to a sensor failure were imputed using a statistical relationship with [Mg].

## Study area and sampling design
- Location: peatland ponds in the Pennine hills, northern England; ponds treated as spatial points.
- Sampling regime: two-monthly visits from 04/2013 to 06/2014 (ages 4–18 months), with one interruption due to snow. On each visit, five ditches were sampled and one pond per ditch sampled randomly; small ponds often disturbed during sampling.
- Chronosequence: six peatlands selected; visits in 06/2013 and 06/2014 used different ponds to build a chronosequence (ten ponds per site).
- Naturally formed ponds: twenty across four peatlands; sampling locations chosen with landowner access.
- Total ponds: 105; natural ponds denoted with a prefix (n) in site codes.

## Study sites and pond attributes
- Sites include Moor House, Tennant Gill, Cold Fell, Yad Moss, Halton Lea, Oughtershaw Beck, and naturally formed ponds Widdybank Fell, Harwood Fell, Butterburn Flow, Geltsdale.
- For each site: location coordinates, mean altitude, restoration year, and pond age (2013/2014 where available).
- Some sites or ponds are natural (denoted with n), with incomplete age/restoration data (NA for some attributes).

## Data structure and files
- Four CSV files:
  - Chron_nat_inverts.csv (82 columns): pond code, followed by invertebrate taxa abundances per pool. Pond codes encode site and pond number (e.g., MHC06).
  - MH_inverts.csv (45 columns): pond code and taxa abundances per pool for the main chronosequence ponds.
  - Chron_natural_physical_chemical.csv (26 columns): pond code, location, sampling date, pond age, coordinates, aspect, elevation, pond dimensions (cm), pond volume (m3), temperature, dissolved oxygen, pH, and dissolved solutes (TN, TP, DOC, Al, Fe, Si, etc.).
  - MH_physical_chemical.csv (26 columns): detailed fields for the main (non-natural) ponds, with descriptive fields for pool, site, date, pond age, OS Grid Ref (and easting/northing), aspect, elevation, depth metrics (mindepth, maxdepth, meandepth), pond dimensions (longaxis, shortaxis, perimeter, volume), water temp, DO, pH, TN, TP, DOC, Al, Fe, Si, and vegetation cover.
- Column-level details include units and methodologies where applicable (e.g., GPS for coordinates, various sensors and lab instruments for chemical analyses).

## Variables and units (highlights)
- Biological: invertebrate taxa abundances per pond/pool.
- Spatial and physical: altitude (m), OS Grid Ref, easting, northing, aspect (degrees), elevation (m), pond dimensions (cm), volume (m3), depth metrics (cm), long/short axis, perimeter (cm).
- Water chemistry: temperature (°C), dissolved oxygen (mg/L), pH, total nitrogen (TN, mg/L), total phosphorus (TP, mg/L), dissolved organic carbon (DOC, mg/L), dissolved Al/Fe/Si (mg/L), vegetation cover (%).
- Temporal: sampling dates; pond age (years).

## Data quality and completeness
- Macroinvertebrate identifications verified by independent experts.
- Field sensors calibrated prior to each visit; laboratory instruments calibrated with known standards.
- Completeness: dataset described as complete; five pH values imputed due to sensor failure (documented).

## How this supports GIS work
- Pond codes enable joining across biological and physico-chemical datasets.
- Coordinate data (OS Grid Ref, easting, northing) enable accurate mapping and projection to GIS coordinate reference systems.
- Rich attribute set supports spatial analyses of biodiversity patterns relative to physico-chemical gradients, pond morphology, restoration age, and chronosequence effects.
- Enables visualization of species distributions, diversity metrics, and environmental drivers across space and time (natural vs restored ponds).

## Notes for users
- Natural ponds are denoted with a prefix (n) in pond/site codes.
- pH sensor failure occurred in month 12; five pH values are estimated via a relationship with magnesium (r = 0.81) and flagged in the dataset.
- Detailed methodological notes and full data definitions are provided in the Beadle et al. publication (in press): Landscape-scale peatland rewetting benefits aquatic invertebrate communities.

## Reference
- Beadle et al. (in press) Landscape-scale peatland rewetting benefits aquatic invertebrate communities. Biological Conservation.