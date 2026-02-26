# Wetland life project, species table for larval and adult mosquitos at various wetland sites, samples from April to October 2017 and 2018

## Overview
- Dataset from the Wetland Life project detailing mosquito diversity and abundance in English wetlands.
- Covers larval and adult mosquitoes across 12 UK wetland sites with samples collected from April 2017 to September 2018.
- Data intended to support tools and analyses for assessing wetland suitability for mosquitoes, with related publications and project outputs.

## Data collection and methods
- Collection sites and methods:
  - 12 wetland sites sampled.
  - Adults: two Mosquito Magnet traps per site deployed continuously for four days and four nights every fortnight from early April to late October.
  - Larvae: water samples collected from target water bodies in May, July, and September.
- Sampling details:
  - Larval sampling: approx. 1 L of surface water per site; about 200 mL collected per dip using a standard white container (immersed five times); larvae captured with a pipette and stored in 75% ethanol.
  - Adult sampling: traps attract mosquitoes via CO2 (propane combustion) and heat, supplemented with octenol lure.
- Coverage:
  - On average, about 9 samples per site across the study period.
- Data captured:
  - Counts by life stage (larval or adult) and mosquito species, aggregated by site and date.

## Data variables and structure
- Data type: total counts by life stage, species, site, and year/month.
- File structure: CSV with columns for date/year, site, site latitude/longitude (degrees, minutes, seconds for Excel compatibility), followed by a species table with a column for every species found in the study.
- Location data: geocoordinates stored in DMS format to ensure proper loading into analysis tools like Excel.

## Quality control and limitations
- Identification: adults and larvae identified using published keys; secondary verification within the research team.
- Consistency and bias:
  - Sampling methods adapted to site topography; no guarantee of a totally consistent sampling effort across all sites.
  - Absolute population density estimates are approximate due to potential variability in effort and trap effectiveness.
- Data suitability notes:
  - Data provide evidence on relative species distribution across sites rather than precise abundance comparisons without accounting for effort differences.

## Outputs, publications, and provenance
- Publications relating to the study include:
  - Mosquito diversity and abundance in English wetlands (Parasites & Vectors, 2022, submitted at the time).
  - Mosquito magnet traps for monitoring host-seeking Simulium (2018).
  - Wetland mosquito survey handbook: assessing suitability of British wetlands for mosquitoes (Natural Resources Institute, 2020).
  - The wonder of wetlands: interdisciplinary investigations on the multiple values of English wetlands (2022).
  - Mosquito Magnet traps as a potential means of monitoring blackflies (2021).
- Project outputs referenced online as part of the Wetland Life outputs.

## Implications for data strategy and governance (Data Leaders)
- Utility:
  - Provides a longitudinal, geolocated dataset enabling cross-site comparisons and modeling of mosquito distribution and abundance.
  - Supports development of data products for wetland suitability assessments and vector surveillance.
- Data management considerations:
  - Metadata embedded in the dataset (date, site, precise coordinates; species counts) supports discoverability and re-use.
  - Clear documentation of collection methods and quality caveats aids interpretation and integration with other data sources.
- Gaps and challenges to address:
  - Scattered data collection across sites and years may require harmonization when integrating with other datasets.
  - Verification of sampling effort consistency is important for robust trend and density analyses.
  - Access and reuse depend on availability of related project outputs and publications; ensure clear data licensing and access pathways.