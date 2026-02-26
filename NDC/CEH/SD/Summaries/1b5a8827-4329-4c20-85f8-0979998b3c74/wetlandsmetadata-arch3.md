# Wetland life project, species table for larval and adult mosquitos at various wetland sites, samples from April to October 2017 and 2018

## Purpose and scope
- Provides a dataset of mosquito diversity and abundance across 12 UK wetland sites, including both larval and adult life stages.
- Aimed at informing a prediction tool for wetland suitability for mosquitoes and supporting monitoring decisions.

## Study design and sampling methods
- 12 wetland sites in the UK were sampled.
- Adults: two Mosquito Magnet traps per site, operated continuously for four days and four nights every fortnight from early April to mid/late October.
  - Traps mimic host animals by burning propane to release CO2 and heat and are baited with octenol.
- Larvae: one larval survey per target water body in May, July, and September.
  - Water sampling: ~1 L surface water collected (approximately 200 mL transferred to a standard white container), stored in 75% ethanol.
- Sampling adjusted to site topography; not guaranteed to be a totally consistent sampling effort across sites.

## Data collected and structure
- Data are total counts by life stage, mosquito species, site, and year/month.
- Data file structure (CSV):
  - Columns for date/year, site, site latitude and longitude (degrees, minutes, seconds format for proper loading into Excel).
  - A subsequent species table with a column for every species found in the study.

## Quality control and limitations
- Species identification conducted using published keys, with secondary verification within the team.
- Methods were adjusted to suit site topography; the dataset provides evidence of relative species distribution per site.
- Limitations:
  - No guarantee of fully consistent sampling effort across sites.
  - Estimates of absolute population density are approximate.

## Data governance and sharing considerations
- Metadata is included to support reproducibility (e.g., precise coordinates, sampling dates, life stages).
- Public sharing of underlying datasets can be a barrier in some monitoring contexts; transparency is achieved through detailed metadata and standardized structure.

## Outputs and dissemination
- Publications relating to the study:
  - Mosquito diversity and abundance in English wetlands — empirical evidence to guide a prediction tool for wetland suitability for mosquitoes (Parasites & Vectors, 2022, submitted)
  - Mosquito magnet traps for monitoring host-seeking Simulium (2018 abstract)
  - Wetland mosquito survey handbook: assessing suitability of British wetlands for mosquitoes (2020)
  - The wonder of wetlands: interdisciplinary investigations on the multiple values of English wetlands (2022)
  - Mosquito Magnet traps as a potential means of monitoring blackflies (2021)
- Project outputs linked via Wetland Life project materials (e.g., outputs page).

## Relevance for monitoring frameworks
- Demonstrates integration of targeted field collections (larval and adult) across multiple sites to inform resilience and risk assessments.
- Provides a structured, interoperable data format (CSV with explicit coordinates and per-species columns) suitable for dashboards, reporting, and indicator development.
- Highlights practical challenges in monitoring data governance, data quality, and comparability over time, informing future standardization and metadata requirements.

## Publications and related outputs
- Medlock et al., Mosquito diversity and abundance in English wetlands (Parasites & Vectors, 2022, submitted)
- Cheke et al., Mosquito magnet traps for monitoring host-seeking Simulium (2018 abstract)
- Hawkes et al., Wetland mosquito survey handbook (Natural Resources Institute, 2020)
- Hawkes et al., The wonder of wetlands (2022)
- López-Peña et al., Mosquito Magnet traps for blackflies (Medical and Veterinary Entomology, 2021)