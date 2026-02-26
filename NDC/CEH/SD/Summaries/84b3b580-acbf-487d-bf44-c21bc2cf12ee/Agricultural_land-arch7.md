# The data included in Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv relates to an analysis of the impact changes in water availability will have on the suitability of land used in the production of these commodities in 2050.

## Aim
- Combine projections of changes in water scarcity with current land use for selected commodities to identify potential country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and collection methods
- Global maps of change in annual runoff (%) and water scarcity (index 1–4) derived from five general circulation models (GCMs), provided by Prof. N. Arnell.
- Water scarcity methodology detailed in Arnell et al. (2011).
- Global maps of current pasture land from earthstat.org (open access).
- Global cropland maps created from a mix of satellite data and census statistics, on a 5 arcminute grid (details in Monfreda et al., 2008; Ramankutty et al., 2008).

## Fieldwork and laboratory instrumentation
- Desk-based study; no fieldwork or laboratory instrumentation used.

## Calibration steps and values
- No new calibration; all data are published sources.
- Annual runoff: percent change between baseline (1960–1990) and 2050.
- Water scarcity: scaled 1–4 (1 = not water scarce, 4 = severely water scarce).
- Agricultural land areas provided on a per-hectare basis.

## Analytical methods
- Overlay of land area for each commodity with GCM-based projections of water scarcity and runoff using ArcGIS.
- Vulnerable land defined where pasture land overlaps areas with (i) declining runoff and (ii) water scarcity in 2050.
- Output: country-level percentage of land that is vulnerable according to both criteria.

## Nature and units of recorded values
- Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, Wheat_2050.csv contain the percentage of total country area for each commodity classified as vulnerable.
- Country names align with FAOSTAT naming.
- Values reflect the percentage of land area, with baseline/runoff and 2050 water scarcity designations described above.

## Quality control
- Datasets sourced directly from data owners to ensure unmodified versions.

## Details of data structure
- Country-level estimates averaged across the five GCM models.
- Standard deviation provided for the values.

## Additional information for interpretation
- GCMs used: CSIRO_Mk3, HADGEM, INMCM4, IPSML_MR, MRIOC_CM3.
- Figure 1 describes the schematic overlay of hydrological model outputs with global agricultural land maps.
- References for underlying datasets include Arnell et al. (2011), Gosling et al. (2016), Gosling et al. (2010), Monfreda et al. (2008), and Ramankutty et al. (2008).