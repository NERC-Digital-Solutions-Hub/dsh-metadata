# Supporting information for Pescott, O.L. (2016). A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data

## Overview
- Describes the supporting dataset for a survey of vascular plant occupancy in pavement (sidewalk) habitats within an urban area around Sheffield, England.
- Timeframe: field surveys conducted from 2012-06-23 to 2014-07-11; cross-sectional snapshot limited to late June and early July each year.
- Objective: capture plant species occurring in pavement-adjacent habitats to support analysis of urban flora occupancy.
- Outputs include a structured data record with sampling areas and plant observations, plus notes on data interpretation and references.

## Sampling design and scope
- Geographic basis: British National grid (OSGB 1936 EPSG:27700); target area in Sheffield with at least 25% built-up land cover per the Land Cover Map 2000 (Fuller et al. 2002).
- Spatial structuring: the area divided into four quadrants (north-east, south-east, south-west, north-west) around a central reference point (Lat 53.378493, Long -1.430239; grid reference 438000, 387000).
- Selection process:
  - Within each urban 1 km^2 cell, all four 500 x 500 m sub-cells with at least 50% built-up area were numbered.
  - A pocket calculator random number generator selected one sub-cell per 1 km^2 cell for survey; four 1 km^2 cells per quadrant were used, with 16 total sub-cells surveyed.
  - Exclusion: four 1 km^2 cells in the north-east quadrant that fell in the neighboring city of Rotherham were excluded, leaving 16 sampled sub-cells.
- Field method: within each selected 1 km^2 cell, survey of 16 selected 500 x 500 m sub-cells for 1.5 hours or until every publicly accessible street had been walked on both sides (whichever took longer).
- Habitat focus: plants recorded only if they occurred in the pavement (sidewalk) habitat or immediately adjacent features (edges of paved areas, grass strips, kerbstones, pavement furniture, utility installations, etc.). Garden escapes observed on the pavement boundary were recorded as such in the comments.

## Data collected and habitat definition
- Target habitat: pavement-side plant occupancy within urban 1 km^2 squares.
- Observations include plant occurrences rooted on the pavement or within the immediate pavement-adjacent zone, including occasional boundary-wall-originating shoots that persist in the focal habitat.
- Timing and phenology considerations: the single-year seasonal window across three years aims to minimize detection bias due to phenology; late-flowering species may be identified to genus in some cases due to timing.

## Data structure and fields
- recordedName: species or species aggregate as observed in the field.
- nameAuthor: taxonomic authority for the name where applicable.
- date: observation date (DD/MM/YYYY).
- 1kmLocation: lettered British National grid reference for the sampled 1 km square.
- 1kmQuadrant: quadrant designation for the 1 km square.
- centroidEasting / centroidNorthing: coordinates of the centroid for the sampled 500 x 500 m sub-cell.
- buffer (m): distance used to recreate the sampled area when needed.
- comment: notes related to species occurrence observations (e.g., garden escapes; surviving).

## Temporal and phenology notes
- The study is a cross-sectional snapshot limited to late June and early July across years 2012–2014.
- This constraint helps reduce phenology-related detectability differences, but may miss late-flowering taxa; future re-surveys should consider shifting phenology.

## Quality control and taxonomy
- All plant identifications were conducted by the author.
- Ambiguities in identification were resolved using:
  - Flora for Britain and Ireland (Stace 2010) for nomenclatural keys.
  - Vegetative keys (Poland and Clement 2009) when needed.
- In cases with insufficient material, specimens were recorded to genus level.

## Usage notes and interpretation
- Aims to enable data reuse and cross-study comparisons by providing:
  - Clear sampling design and random selection process.
  - Precise spatial references and a downloadable buffer to recreate surveyed areas (via ESRI Shapefile of areas).
  - A straightforward, field-derived data structure capturing species occurrences and location context.
- Related documentation and data products:
  - See Pescott (2016) Biodiversity Data Journal (in review) for the full data paper.
  - Land Cover Map 2000 (Fuller et al. 2002) is cited as the basis for the built-up area criterion.
- References for methodological and taxonomic context:
  - Fuller RM et al. 2002; Smith 2010; Stace 2010; Poland & Clement 2009; Pescott 2016 (in review).

## Additional information
- The dataset references an ESRI Shapefile of the sampled areas to aid spatial recreation.
- Provides structured data fields intended to facilitate data cleaning, integration, and the creation of data products (dashboards, pivot tables, etc.) for end users.