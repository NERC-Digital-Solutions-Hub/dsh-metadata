# The data included in Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv relates to an analysis of the impact changes in water availability will have on the suitability of land used in the production of these commodities in 2050.

## Aim
- Combine projections of changes in water scarcity with current extent of land use for selected commodities to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and collection methods
- Global maps of change in annual runoff (%) and water scarcity (index 1–4) derived from projections by five GCMs, obtained from Prof. N. Arnell (University of Reading). Methodology detailed in Arnell et al. (2011).
- Global maps of current pasture land area downloaded from earthstat.org.
- Global cropland maps generated from a mix of satellite-derived data and national/state/country census statistics, expressed on a global 5 arcminute grid (details in Monfreda et al., 2008; Ramankutty et al., 2008).

## Experimental design
- Desk-based study; analysis performed by overlaying spatial data in ArcGIS.
- Vulnerable land defined as pasture land that (i) experiences a decrease in annual runoff, and (ii) is in watersheds classified as water scarce in 2050.
- For each country and commodity, compute the percentage of land that meets both criteria (vulnerable share).

## Data content and structure
- Files: Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, Wheat_2050.csv.
- Values: percentage of the country’s total area for each commodity classified as vulnerable.
- Country names aligned with FAOSTAT conventions; data averaged across the five GCM models; standard deviation provided.

## Calibration steps and units
- No calibration required; all data are pre-published.
- Annual runoff: percentage change from baseline 1960–1990 to 2050.
- Water scarcity: scale 1–4 (1 = not water scarce, 4 = severely water scarce).
- Land areas expressed in hectares (ha).

## Analytical methods
- Overlay land area maps with GCM-derived projections of water scarcity and runoff in ArcGIS.
- Identify vulnerable areas where both criteria are met; compute country-level share of land that is vulnerable for each commodity.

## Quality control and data provenance
- Datasets sourced directly from data owners to ensure unmodified data are used.

## Data structure and interpretation
- Country-level estimates averaged across the five GCM models; includes standard deviation across models.
- GCM models used: CSIRO_Mk3, HADGEM, INMCM4, IPSL_CM5 (listed as IPSL_MR or IPSL_CM3 in text), and MRI-ESM_CM3 (text shows MRIOC_CM3).

## Additional information for interpretation
- References and background datasets:
  - Arnell et al. 2011; Gosling & Arnell 2016; Gosling et al. 2010.
  - Monfreda et al. 2008; Ramankutty et al. 2008.
- The study is desk-based with data combining hydrological projections and global agricultural land maps to assess country-level vulnerability.