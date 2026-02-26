# Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv

## Aim
- Combine projections of changes in water scarcity with current land use for selected commodities to identify potential country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and collection methods
- Global maps of change in annual runoff (%) and water scarcity (index 1–4; 1 = not water scarce, 4 = severely water scarce) derived from five general circulation models (GCMs); data provided by Prof. N. Arnell, University of Reading (Arnell et al. 2011).
- Global pasture land area maps downloaded from earthstat.org (open access).
- Global cropland maps created from a mix of satellite-derived data and census statistics (country/state/national) on a 5 arcminute grid; details in Monfreda et al. 2008 and Ramankutty et al. 2008.

## Experimental design
- Desk-based study integrating projections of water scarcity with current land-use extents to assess country-level vulnerabilities of pasture land to water scarcity in 2050.

## Calibration, units, and data preparation
- No new calibration; all data are from published sources (section 2).
- Annual runoff: percentage change between baseline (1960–1990) and 2050.
- Water scarcity: scaled 1–4, with 1 = not water scarce, 4 = severely water scarce.
- Agricultural land areas are provided on a hectare (ha) basis.
- Outputs expressed as maps and country-level statistics.

## Analytical methods
- Overlay global maps in ArcGIS to combine land use with hydrological projections.
- Vulnerable pasture land is defined by two criteria at each location: (i) runoff percentage is declining, and (ii) the watershed is classified as water scarce in 2050.
- For each country and commodity, compute the percentage of total land that is vulnerable.

## Nature and units of recorded values
- Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, and Wheat_2050.csv report the percentage of a country’s total land area used for that commodity classified as vulnerable.
- Country names follow FAOSTAT conventions.
- Outputs include standard deviation across the five GCMs.

## Quality control
- Datasets sourced directly from data owners to ensure no modified versions are used.
- Data represent country-level estimates averaged across the five GCMs.

## Details of data structure
- Aggregated by country; values reflect averages over 5 GCMs.
- Standard deviation provided to indicate cross-model uncertainty.

## Data sources and model details
- GCMs used: CSIRO Mk3, Hadley Centre HADGEM, INMCM4, IPSL CM5 (notation in text: IPSML_MR), and MRIOC_CM3.
- References and underlying data sources:
  - Arnell N.W., van Vuuren D.P., Isaac M. (2011). The implications of climate policy for the impacts of climate change on global water resources. Global Environmental Change, 21, 592–603.
  - Gosling N., Arnell N.W. (2016). Global assessment of the impact of climate change on water scarcity. Climatic Change, 134, 371–385.
  - Gosling S.N., et al. (2010). Global hydrology modelling and uncertainty: running multiple ensembles with a campus grid. Philosophical Transactions of the Royal Society A.
  - Monfreda C., Ramankutty N., Foley J.A. (2008). Farming the Plant: Part 2—Geographic distribution of crop areas, yields, etc. Global Biogeochemical Cycles, 22, GB1022.
  - Ramankutty N., et al. (2008). Farming the Plant: 1—Geographic distribution of global agricultural lands in 2000. Global Biogeochemical Cycles, GB1003.