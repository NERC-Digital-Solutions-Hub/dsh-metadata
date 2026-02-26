# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- Study of natural enemies of crop pests in winter-sown oilseed rape (Brassica napus L.) and how they relate to local plant diversity and landscape characteristics.
- Data collected in 2013–2014 across the Wessex region, southern England, within the broader Wessex BESS project (NERC funding).
- Dataset designed to be used with other Wessex BESS WP4 datasets to examine ecosystem interactions and pest control dynamics.

## Data collection and methods
- Field surveys conducted in 12 fields per year (across 2014 and 2015 sampling windows).
- Local plant diversity assessed with quadrats in field margins and cropped areas; hedges recorded.
- Landscape context derived from GIS within 0.5–3 km buffers around collection points, using multiple spatial datasets.
- Natural enemies sampled with:
  - Suction sampling for canopy parasitoids (1 m² area, 7 seconds per sample, 3 sampling points per transect).
  - Pitfall traps for ground-dwelling enemies (Carabidae, Staphylinidae, etc.).
  - Water traps to assess pest larvae dropping from the canopy (subset of fields).
- Pest larvae identified: Meligethes spp., Ceutorhynchus spp., Dasineura spp.
- Temporal windows: suction and canopy sampling in late June–July 2013 and late May–June 2014; pitfall and water-trap sampling aligned with these periods.

## Landscape and habitat metrics
- GIS-based characterization of landscape within multiple radii (0.5–3 km) around each field, including:
  - Grassland types: species-rich, restoring, improved, semi-natural habitats, and arable areas.
  - Presence of hedges and grassland restoration projects.
- Local habitat measurements near transects included:
  - Field edge length, hedge proportion, field margin proportion and width.
  - Margin plant diversity via quadrats; in-crop plant diversity at several points into the field.
- Additional metrics describe spatial patterns of habitat patches and their spatial relationships (areas and distances for grasslands, semi-natural habitats, restored grasslands, and species-rich grasslands).

## Variables and data structure
- Datasets and files (linkable via a common key):
  - NERCPestNatEnSpeciesList.csv: taxonomic details and species coding; includes a SpeciesCode to link to other datasets.
  - NERCPitfall.csv: pitfall trap counts by species (and other columns) with SampleCode, SurveyDate, and transect information.
  - NERCSuctionSample.csv: suction sample counts by species with PointCode linking to landscape data.
  - NERCWaterTrap.csv: counts of pest larvae and parasitoid interactions collected via water traps.
  - NERCNatEnLandscapeSurvey.csv: landscape and field-level context data (transect, farm, field IDs, year, habitat and plant-diversity metrics, and numerous derived variables).
- Key data features:
  - Species and higher-taxon counts; optional gender metadata for Hymenoptera in the species list.
  - Linkable identifiers: SpeciesCode ties together suction, pitfall, and water-trap data across files.
  - Production of derived landscape metrics at multiple radii and for various habitat categories.

## Temporal and spatial scope
- Field surveys conducted in 12 fields per year, during 2013–2014 field campaigns in the Wessex region.
- Field coordinates provided for precise spatial context (southern England arable and semi-natural landscapes).
- Can be integrated with other WP4 datasets within the Wessex BESS program for broader analyses.

## Data quality and ethics
- Adherence to predefined field and lab protocols; data entered in MS Access with QA checks for anomalies.
- Training provided to data collectors to ensure protocol consistency.
- Research ethics approval obtained from the CLES Penryn Research Ethics Committee (2014/622).

## File linkage and usage notes
- Data can be combined across datasets using the provided linking keys (e.g., SpeciesCode, SampleCode, PointCode).
- Missing data notes indicate some pitfalls were knocked over in the field and other minor gaps; field 3.1 occasionally had sampling limitations due to crop failure.
- Provisions for data usage include the ability to analyze relationships between natural enemies, local plant diversity, and landscape structure, and to compare across years and field contexts.

## Potential uses for data support
- Build self-serve dashboards and reports on natural enemy communities and pest larvae counts by habitat type and landscape context.
- Create integrated analyses with WP4 datasets to explore drivers of biological control in oilseed rape.
- Promote data sharing and reuse by providing transparent metadata, linking identifiers, and documenting data quality and sampling design.