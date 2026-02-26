# The data included in Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv: Analysis of the impact changes in water availability on the suitability of land used in the production of these commodities in 2050

## Aim
- Combine projections of changes in water scarcity with current land-use extents for selected commodities to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and maps
- Global maps of changes in annual runoff (%) and water scarcity (1 = not water scarce to 4 = severely water scarce) derived from five general circulation models (GCMs); projections provided by Prof. N. Arnell.
- Current pasture land area obtained from Earthdata/Earthstat.
- Global cropland maps produced from satellite data plus census data (Modfreda et al. 2008; Ramankutty et al. 2008).

## Experimental design
- Desk-based study overlaying projected hydrological changes with current land-use extents to assess vulnerabilities at the country level for pasture land used for specified commodities.

## Collection methods
- Runoff and water-scarcity maps are long-term projections (1960–1990 baseline vs. 2050) from five GCMs.
- Land-use maps (pasture and croplands) are global, gridded data sets on a 5 arcminute grid.
- Datasets are used in combination to identify vulnerable areas.

## Calibration steps and values
- No new calibration; all data originate from published sources.
- Runoff change: percentage change from baseline (1960–1990) to 2050.
- Water scarcity: 1–4 scale (1 = not water scarce, 4 = severely water scarce).
- Agricultural land areas expressed in hectares (ha).

## Analytical methods
- Overlay the spatial outputs in ArcGIS for each commodity with GCM-specific water-scarcity projections.
- Define vulnerable pasture land where both criteria are met: (i) runoff is declining, and (ii) watershed is water scarce in 2050.
- For each country and commodity, compute the percentage of total land that is vulnerable.

## Nature and units of recorded values
- For each country and commodity, the files Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, and Wheat_2050.csv report the percentage of total land used for the commodity that is vulnerable.
- Country names follow FAOSTAT formatting.
- Data are averages across the five GCM models; standard deviation provided to reflect inter-model variability.

## Quality control
- Datasets sourced directly from data owners to ensure unmodified originals.

## Details of data structure
- Country-level estimates averaged across the 5 GCM models.
- Standard deviations accompany mean vulnerability percentages.

## Models used and additional information
- GCM ensemble models: CSIRO_Mk3, HADGEM, INMCM4, IPSL_CM5? (listed as IPSML_MR in the text), and MRIOC_CM3.
- References for underlying datasets and methodology provided (Arnell et al. 2011; Gosling et al. 2016; Monfreda et al. 2008; Ramankutty et al. 2008).