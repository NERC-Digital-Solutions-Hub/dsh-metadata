# Plant community surveys and sampling design

## Overview
- Study conducted in 1983 on Jebel, Tunisia, examining plant species distribution and abundance through 78 quadrats.
- Sampling aimed to cover all vegetated areas (except inaccessible areas) and to include all community types from Fay (1980), with broad but non-random site dispersion.
- Nested quadrat design used to capture multiple spatial scales and accumulate data on both herbaceous and woody components.

## Sampling design and data collection
- Quadrat hierarchy: 2 x 2 m, 5 x 5 m, 7.07 x 7.07 m, 10 x 10 m, and 14 x 14 m (nested design).
- Within the 2 x 2 m quadrat: estimate cover-abundance for herbaceous species.
- Within the 10 x 10 m quadrat: estimate cover-abundance for woody species.
- At each site, central stake located by random placement within quadrat; on average three nested quadrats per site; field work conducted 8–10 hours per day.
- For species not identified in the field, specimens were collected and pressed for herbarium verification (Tunis or British Museum). Some taxonomic groups likely under-recorded due to late flowering.

## Species identification and taxonomy
- Post-field taxonomic work updated to reflect changes in nomenclature (Euro-Med PlantBase and MedChecklist).
- Final taxonomy anchored to a Tunisian flora catalogue and a national park flora compiled since the study.
- Difficult identifications led to combining certain closely related species pairs.

## Functional grouping
- Separate analyses for woody and herbaceous communities.
- Species classified into taxonomic and functional groups expected to respond differently to grazing: Poaceae, Legumes, Geophytes, Forbs (annual/perennial), shrubs/trees; Forbs group includes ferns, cacti, club mosses, and some mosses.
- Annual vs. perennial distinction not made due to single-season survey.

## Grazing intensity assessment
- Grazing assessed at each 10 x 10 m quadrat center by ranking browsing on principal woody species.
- Four grazing levels: unbrowsed, lightly browsed, moderately to heavily browsed, severely clipped.
- Herbivore activity indicators noted qualitatively (e.g., hair on trunks, droppings), but not quantified.
- Distribution across 78 sites: 71% unbrowsed, 12.8% lightly browsed, 16.7% moderately to heavily browsed; heavily grazed sites common at low altitude with rock outcrops.

## Abiotic environmental variables
- Variables measured at quadrat centers to separate grazing effects from environment:
  - Altitude (barometric altimeter)
  - Slope (inclinometer)
  - Aspect (compass, as a proxy for solar insolation)
  - Rock outcropping/rock cover percentage

## Olea europaea as a proxy for anthropogenic activity
- Olea europaea density used as an indicator of anthropogenic influence (grazing and woodcutting impact) due to shading effects on herbaceous flora.
- Counts of Olea stems >4 cm in DBH at 1.5 m height and at 30 cm height (for 69 sites; not collected for the first 9 sites).
- Density quantified by size classes (0–5 cm, 6–10 cm, 11–15 cm, 16–20 cm, >20 cm circumference) and converted to equivalent stem radius/area per site.

## Data structure and availability
- Data provided as three flatbed CSV files:
  - woody_comm.csv: counts of woody plants at each of 78 sites
  - herb_comm.csv: counts of herbaceous plants at each of 78 sites
  - spatial_env.csv: environmental variables at each of 78 sites
- Column headers are documented in a supplementary file (Metadata_for_Tunisia plants.rtf).

## Data quality, limitations, and usage notes
- Taxonomy and nomenclature changes since the original study may affect data interpretation; updates rely on PlantBase, MedChecklist, and Tunisian flora sources.
- Non-random sampling and potential under-recording of certain taxa due to seasonal timing (late flowering) and identification challenges.
- Some data gaps: Olea measurements missing for the first 9 sites; 69 sites with Olea data.
- Potential users are requested to contact the authors before re-use of the data for new studies.

## References (context for methodology)
- Cited works cover sampling design, grazing effects, Mediterranean vegetation, and taxonomic references used for species identification and functional grouping.