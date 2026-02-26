# The provenance trial environment

## Overview
- Describes the La Petite Charnie provenance trial, established by INRA (French National Institute for Agricultural Research).
- Involves ~200,000 trees spanning 103 provenances of Quercus petraea and 9 provenances of Quercus robur.
- Site characteristics: mean elevation ~140 m, Atlantic temperate wet climate, red sandstone/shist/clay substratum, surrounded by mature oak forest and other deciduous species.
- Proxi­mate goal is to study provenance performance and herbivory across the natural range of the species.

## Experimental design and geography
- Within each soil zone, each provenance is represented by 2–3 plots, with replicates totaling 24 trees per plot (4 columns × 6 trees; 1.75 m within-column, 3 m between columns).
- Plots from 8 different randomly selected provenances are grouped into blocks; block positions are randomized within soil zones to enable separation of plot, block, soil-zone, and provenance effects.
- A subset of provenances was studied, so the block effect was not considered; plot positions within soil zones treated as random.
- Each sampled provenance is planted in multiple replicate plots across five soil zones, yielding 200 study plots containing 4,800 trees in total.

## Data collection: Herbivore survey
- Focuses on cynipid gall wasps with broad Western Palaearctic distributions.
- Gall abundance surveyed across 20 provenances during 2008–2009 (four surveys: spring and autumn generations each year).
- For each of the 200 plots, galls were sampled from 12 of 24 trees (two internal rows of six trees per plot) using a pole pruner (~4 m reach).
- From each surveyed tree, 10 twigs (last two years’ growth) were sampled; galls identified in-field by species and generation.
- Four survey generations per year (two yearly generations, spring and autumn) were recorded for each twig.

## Data structure and fields
- Data captured as counts (Nature and Units: Counts).
- Key identifiers and design fields include: ID, Record ID, ProvCode, ParcelleID, SoilZone, YearGen (generation and survey year), TreeNo, ShootNo, ShootID.
- Gall-count fields for asexual generations (e.g., AfecAsex, AglanAsex, AsolAsex, NalbAsex, NantAsex, NqbAsex, NnAsex, CdivAsex, CqfAsex) and sexual generations (e.g., AtestSex, NalbSex, NantSex, NnSex, NqbSex).
- Provisional interpretation: counts are provided per gall species and generation for each surveyed shoot on each tree.

## Quality Control
- One-to-one training of data collectors to ensure consistency.
- Double checking of data for outliers during transcription.

## GIS and data-use considerations
- The design supports spatial analysis by plot, soil zone, provenance, and year/generation, enabling mapping of gall abundance across the landscape and across provenance groups.
- Data can be linked to plot-level geography (soil zones and ParcelleID) to explore spatial patterns of herbivory and provenance performance.
- Considerations for GIS work include ensuring consistent data standards, handling large/complex datasets (4,800 trees, multiple generations, many gall taxa), and integrating with additional environmental layers (soil, elevation, climate) to contextualize provenance responses.