# Historic Standardised Streamflow Index (SSI) using Tweedie distribution with standard period 1961-2010 for 303 UK catchments (1891-2015)

- The SSI is a drought index based on the cumulative probability of monthly mean streamflow for a catchment, calculated for accumulation periods of 1, 3, 6, 9, 12, 18 and 24 months. Values are end-month based, transformed to a Normal distribution (mean 0, SD 1), and truncated at +/-5 to handle extremes.
- Standard period for distribution fitting is 1961-2010 to align with SPI-based drought indicators in the Historic Droughts project.
- The dataset covers 1891 to 2015 and is stored in CSV format, with one file per catchment (305 files for 303 UK catchments) and includes six accumulation periods.

## Project context

- Part of the Historic Droughts project (2014–2018; £1.5m) funded by UK Research Councils.
- Aims to develop a cross-disciplinary understanding of UK droughts to improve drought management tools.
- Involves eight institutions: British Geological Survey, Centre for Ecology & Hydrology, Cranfield University, University of Exeter, HR Wallingford, Lancaster University, the Met Office, and the University of Oxford.
- Seeks to link hydrometeorological data with social, regulatory, and economic factors to understand drivers, impacts, and responses to droughts since the 19th century.

## Dataset details

- SSI data are derived from the Historic Reconstructions of Daily River Flow for 303 UK Catchments (1891-2015); includes modelled daily flows, with some naturalised calibrations, totaling 305 series.
- SSI calculated for seven accumulation periods (1, 3, 6, 9, 12, 18, 24 months) and assigned to the end-month of the period.
- Calibration and catchment selection follow Smith et al. (2018); catchments include near-natural benchmarks and some with artificial influences.
- Data quality notes: uses modelled reconstructions; evaluation includes NSE (Nash-Sutcliffe Efficiency) and other metrics; users should ensure data suitability for their purpose.

## Data & methods

- Calculation process:
  - Monthly mean flows aggregated from daily reconstructions; SSI computed from the cumulative probability of monthly flows for each accumulation period.
  - Tweedie distribution fitted to each time series (1, 3, 6, 9, 12, 18, 24 months) to derive SSI.
  - Data transformed to normal scores (mean 0, SD 1); units are removed.
  - SSI values beyond |5| are truncated to this limit.
- Data sources and consistency:
  - Based on the best-performing model run from the ensemble of daily streamflow data (Smith et al., 2018).
  - Consistent standardization with SPI data produced in the project (1961-2010 period).
- Temporal considerations:
  - For accumulation periods >12 months, overlapping data cause autocorrelation; SSI indicates relative rarity within the same series, but underlying independence assumptions for frequency analysis are violated.

## Calculation notes and caveats

- The standard period (1961-2010) was chosen because it was the longest available data window at the time and to ensure comparability with SPI-based indicators.
- When interpreting SSI, more negative values indicate rarer, drier conditions (lower-than-average flows), while more positive values indicate wetter conditions.
- There are known missing data issues:
  - -999 codes indicate missing values; start-month gaps vary by accumulation period (e.g., 1-month, 3-month, etc.).
  - Two catchments (31023 West Glen at Easton Wood and 39017 Rey at Grendon Underwood) have substantial missing data due to Tweedie fitting issues across multiple months.
  - Additional sporadic missing values (Table A1) exist across several catchments and accumulation periods.
- Acknowledges potential autocorrelation in SSI series for long accumulation periods due to overlapping data.

## Data format and access

- File naming: HD_SSI-CatchID-189101-201511.csv (one file per catchment), containing the six accumulation periods, with column headings representing the accumulation period lengths (1, 3, 6, 9, 12, 18, 24).
- Data values are normal scores (mean 0, SD 1) and range from -5 to +5.
- Missing data are coded as -999.
- HD_SSI_CatchInfo.csv accompanies the SSI data, listing catchments with:
  - Catchment ID, name, area (km2), nested flag, UK Benchmark Network flag, and NRFA station page URL.
- Access notes: catchment information links point to the NRFA pages; dataset is associated with the Historic Droughts project (grant NE/L01016X/1).

## Inventory and integration

- The Historic Droughts Inventory provides:
  - Hydro-meteorological timelines of rainfall, river flows, and groundwater as drought indicators (extended back to the 19th century via modelling and data rescue).
  - References to past droughts from 19th century to present (newspapers, legislation, agricultural media, oral histories) to contextualise drivers, impacts, and responses.
- The SSI dataset can be used in multi-sectoral drought assessments and integrated with other inventories to support policy planning and water resource management.

## Usage and applications for Analysts Monitoring the Environment

- Enables consistent, comparable assessment of hydrological drought severity across multiple UK catchments and time scales.
- Supports monitoring of environmental health and policy performance over long historical periods.
- Can be combined with other datasets (e.g., socio-economic, regulatory data) to analyse drivers of droughts and effectiveness of management responses.
- Datasets are stored and prepared for publication, with metadata to facilitate reuse and transparency for policy makers and regulators.

## Acknowledgements and references

- Outcome of the Historic Droughts Project (grant number: NE/L01016X/1).
- Key references include Barker et al. (2016), Svensson et al. (2017), Tanguy et al. (2015, 2017), Vicente-Serrano et al. (2012), and Smith et al. (2018, in prep).