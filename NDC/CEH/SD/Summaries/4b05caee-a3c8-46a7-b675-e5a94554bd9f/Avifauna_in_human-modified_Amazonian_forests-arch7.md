# Supporting information for Avifauna occurrence data from a longitudinal experiment in human-modified Amazonian forests affected by the 2015-16 El Niño drought and associated fires

## Overview
- Longitudinal dataset documenting bird occurrence across 36 forest plots in the Brazilian Amazon.
- Plots span a disturbance gradient: undisturbed, logged, logged-and-burned, and secondary forests.
- Surveys conducted before and after the 2015-16 El Niño-associated fires: 2010-11 (pre-fire) and 2016 (about 12 months post-fire).
- Data stored in ECOFOR_AFIRE_RAS_birds.csv, including species observations, methods, and plot-level details.
- Purpose: quantify how human disturbance and climate-induced stressors affect tropical forest bird communities.

## Study region
- Location: Santarém/Belterra/Mojuí dos Campos municipalities, Pará state, Northeastern Brazilian Amazon.
- Key regional characteristics: mean annual temperature ~25°C; mean annual rainfall ~1920 mm.
- Primary forest canopy typically 30–40 m tall (emergents up to ~50 m).

## Experimental design and sampling regime
- 36 primary forest plots categorized by disturbance history:
  - Undisturbed (N=10)
  - Logged (N=10)
  - Logged-and-burned (N=10)
  - Secondary forests (N=6)
- Sampling within each plot at identical locations across both survey periods.
- Two bird surveys per plot using fixed-location point counts:
  - Three sampling points per plot (0, 150, 300 m)
  - Two repetitions of 15-minute counts per point (total 75 m width)
- Timing: surveys conducted from dawn to 09:30 on days without persistent rain or strong winds.
- Permits obtained from landowners and authorities; surveys conducted under Brazilian law and approvals.

## Data collection methods
- Observations include all bird species seen or heard; records included auditory and/or visual detections.
- Data collected using solid-state recorders; repetitions rotated among catchments and plots to reduce bias.
- Field personnel and observers listed for data provenance.
- Data entries capture sampling period (CAMP_1 or CAMP_2), plot code, sampling point, date, time, observer, taxonomic family, binomial name, and observation type (Auditory/Visual).

## Data structure and fields (ECOFOR_AFIRE_RAS_birds.csv)
- Fieldwork period: CAMP_1 = 2010-11 (pre-El Niño); CAMP_2 = 2016 (post-El Niño).
- Plot identifier: Plot (plot code/name).
- Sampling point: Point within the plot.
- Temporal data: Date and Time of bird record.
- Personnel: Observer (e.g., A. Lees, J. Barlow, T. Gardner, etc.).
- Taxonomy and observation: Family, Binomial (genus and species), Auditory, Visual flags.

## Plot coordinates and geography
- Plot-level geographic coordinates provided in Table 2.
- Coordinates include:
  - UTM_X and UTM_Y in Universal Transverse Mercator (UTM) zone 21M
  - Municipality attribution for each plot
- Example coverage includes plots in Santarém, Belterra, and Mojuí dos Campos, with varied UTM coordinates corresponding to each plot.

## Data access and licensing
- Primary dataset and supporting information available via the DOI link:
  https://doi.org/10.5285/4b05caee-a3c8-46a7-b675-e5a94554bd9f
- Licensing and terms of use described on the data access page.
- Data provenance and citation:
  Lees, A.; Moura, N.; Franca, F.M.; Ferreira, J.N.; Gardner, T.; Berenguer, E.; Chesini, L.; Andertti, C.; Barlow, J. (2018). Avifauna occurrence data from a longitudinal experiment in human-modified Amazonian forests affected by the 2015-16 El Niño drought and associated fires. NERC Environmental Information Data Centre.

## How this GIS-focused data can be used
- Build map-based data products showing spatial distribution of bird occurrence across disturbance classes and time periods.
- Integrate plot coordinates (UTM X/Y) with other spatial layers (land-use change, fire scars, canopy disturbance) for multi-layer analyses.
- Enable temporal comparisons of species presence/absence and abundance pre- vs post-fire within the 36 plots.
- Link to habitat and disturbance attributes to support biodiversity and conservation planning in the Amazon.

## Supporting references
- PIACENTINI, V. et al. Annotated checklist of the birds of Brazil (2015) for taxonomic context.