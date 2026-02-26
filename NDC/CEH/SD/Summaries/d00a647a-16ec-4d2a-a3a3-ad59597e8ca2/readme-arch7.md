# Identifying priorities, targets, and actions for the long-term social and ecological management of invasive alien species

## Overview
- Aims to identify priorities, targets, and actions for the long-term management of invasive alien species (IAS) using expert-elicited impact data.
- Involves GIS-relevant, map-ready data to understand spatial distribution of IAS impacts across countries and study areas.

## Data and Methods
- Participants: Seventeen experts across seven case studies.
- Approach: Independent completion of Impact Score Spreadsheets guided by CONTAIN-ImpactScoringInstructions.pdf; two scoring rounds followed by a facilitated workshop in San Carlos de Bariloche, Argentina (Dec 2019).
- Outputs: Final agreed impact scores in Unique-Impact.csv.
- Evaluation: Preliminary assessment of methods shared with collaborators in Latin America via ImpactBrief-CONTAIN English and ImpactBrief-CONTAIN Español.
- Purpose within GIS: Produce structured, comparable impact data suitable for map-based visualisations of spatial patterns and cross-country comparisons.

## Data Files and Content
- Compiled-Impact.csv
  - Contains expert-elicited impacts; each row is one impact outcome listed by an expert.
  - Key columns (summary): Impact.outcome, Impact.mechanism, Maximum.impact..EICAT.classification.level., Level.of.confidence, Type, Country, References and supporting information.
- Unique-Impact.csv
  - Deduplicated version (one impact outcome per species-country).
  - Key columns (summary): Impact.outcome, Impact.mechanim, Maximum.impact..EICAT.classification.level., Level.of.confidence, Species.or.asset.impacted, Direction.of.the.impact, Area (km2), Species, Type, Country.
- CONTAIN-ImpactScoringInstructions.pdf
  - Instructions, lists, and guidance used by experts to complete the scoring.
- ImpactBrief-CONTAIN(English).pdf and ImpactBrief-CONTAIN(Español).pdf
  - Brief documents circulated to stakeholders describing procedures, examples, and questions.

## How to Use in GIS
- Data structure: tabular impact data linked at least by country, species, impact outcome, and area (km2) for spatial analysis.
- Visualization options:
  - Map impacts by country or study area.
  - Colour-code by EICAT classification level and/or direction of impact.
  - Show spatial extent using the Area field and country boundaries.
- Potential analyses:
  - Identify hotspots of high-impact outcomes.
  - Compare impact types and mechanisms across regions.
  - Inform policy targets and conservation planning with spatially explicit priorities.

## Access and Contact
- Source: Freely available data from García-Díaz, P., et al., on long-term IAS management.
- Contact: Pablo García-Díaz, School of Biological Sciences, University of Aberdeen (pablo.garciadiaz@abdn.ac.uk; permanent email: herpeto@hotmail.com).
- Date context: Data last modified 18/08/2021; submission 20/08/2021.

## Notes and Considerations for GIS Practitioners
- Data are aggregated at country and study-area scales with explicit area measurements, suitable for regional mapping but not necessarily high-resolution local mapping without further geospatial augmentation.
- The dataset emphasizes expert-elicited impacts and EICAT classifications, which can enhance thematic mapping of risk levels and mechanisms.
- When integrating with other GIS layers, align country boundaries and consider potential resolution limits of the Area field for precise spatial analyses.