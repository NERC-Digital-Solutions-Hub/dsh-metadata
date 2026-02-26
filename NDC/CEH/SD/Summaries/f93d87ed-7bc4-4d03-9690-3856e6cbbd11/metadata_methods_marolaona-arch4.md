# Metadata and methods for the dataset: Hydrometric data and stable isotope data for streamflow and rainfall in the Marolaona catchment, Madagascar, 2015-2016

## Overview
- Dataset from the 31.7 ha Marolaona catchment in the Ankeniheny Zahamena Corridor, Madagascar (18.970°S, 48.422°E) covering 2015–2016.
- Combines hydrometric measurements (rainfall, streamflow, perched groundwater, soil moisture) and stable isotope data (δ18O, δ2H, deuterium excess) to study rainfall–runoff and hydrological processes.
- Data collected at two rainfall gauges, two weirs, ten perched groundwater wells, and multiple soil moisture sensors across three hillslopes; isotope samples gathered from streamflow and overland flow, plus rainfall samples during the wet season.
- Data provided at 5-minute intervals; missing data indicated as NaN. Background methods and study context described in Zwartendijk et al. (2020, 2023).

## Data collection and study setup
- Hydrometric measurements include:
  - Rainfall and streamflow at two locations; perched water table levels at 10 locations; soil moisture at 3 locations (depths 5, 15, 30 cm).
  - Data period: February 3, 2015 to March 3, 2016.
- Rainfall measurements:
  - Two tipping-bucket gauges (Rain Collector II) with HOBO loggers; resolutions 0.2 mm per tip; installed ~1.2 m above soil.
  - Downstream gauge coordinates: ~18.9678°S, 48.4258°E; Upstream gauge: ~18.971°S, 48.4212°E.
  - Upstream data gap: July 1–August 17, 2015 due to battery failure.
- Streamflow:
  - Weirs at catchment outlet (31.7 ha) and upper catchment (7.11 ha); water levels recorded at 5-minute intervals.
  - Periods of sensor failure limit data to two windows: 2015-02-15 to 2015-05-13 (87 days) and 2015-12-12 to 2016-03-03 (82 days).
  - Rating curves developed using salt-dilution-slug-injection method for lower weir; upper weir uses truncated-triangular sharp-crested weir equations (validated with bucket measurements).
- Soil moisture and perched groundwater:
  - Soil moisture measured with Decagon sensors at 5 cm, 15 cm, and 30 cm depths at TF2, EUC, TSF plots.
  - Perched groundwater monitored with fully screened wells at multiple sites (TF1, TF2, EUC, TSF) with minutes-to-5-minute averaging.
- Data storage:
  - All measurements summarized as 5-minute averages (or equivalent), with detailed sensor descriptions and installation notes included in the dataset metadata.

## Datasets and file structure
- HydrometricData_Marolaona.csv:
  - Contents described in Table 1 (DateTime, rainfall at downstream/upstream, streamflow at downstream/upstream weirs, perched water tables, soil moisture and temperature at multiple depths/sites, etc.).
  - Timeframe: 2015-02-03 to 2016-03-03; data reported at 5-minute intervals; missing data as NaN.
- IsotopeData_Marolaona.csv:
  - Contents described in Table 2 (Location, Water_type: rainfall/streamflow/plot runoff, DateTime, Delta18O, Delta2H, DEx).
  - Samples collected from streamflow (upstream of weirs) and overland flow (TF2, EUC, TSF); rainfall samples collected daily during the wet season and per-event via sequential sampler.
- Isotope analyses performed with a cavity ring-down spectroscope (L2130-i CRDS) at the University of Freiburg; delta notation relative to Vienna Standard Mean Ocean Water; stated precision: ±0.16‰ for δ18O and ±0.6‰ for δ2H.
- Data provenance and methodology aligned with Zwartendijk et al. (2020, 2023) and supported by broader references listed in the document.

## Data quality, limitations, and governance
- Data gaps noted due to equipment failures:
  - Upstream rainfall data gap: 2015-07-01 to 2015-08-17.
  - Stream level data limited to two periods due to sensor failures (87 days and 82 days).
- Data are provided with explicit measurement units, depths, and sensor types to support interoperability and reuse.
- Metadata includes detailed column descriptions (Table 1 for HydrometricData and Table 2 for IsotopeData) and notes on perched-water-depth references (mm above low-permeability layer).

## Relevance for data strategy and reuse
- Demonstrates end-to-end data collection and integration across hydrometric and isotopic datasets for a tropical catchment, enabling analysis of rainfall–runoff responses and watershed processes.
- Provides a well-documented, governance-friendly data asset with clear lineage to prior research, enabling collaboration and cross-partner use.
- Facilitates scalable data management: structured CSV files, explicit metadata, traceable methods, and explicit indications of data quality and gaps.

## References
- Zwartendijk, B.W., van Meerveld, H.J., Ghimire, C.P., Ravelona, M., Lahitiana, J., Bruijnzeel, L.A. (2020). Soil water- and overland flow dynamics in a tropical catchment subject to long-term slash-and-burn agriculture. Journal of Hydrology, 582, 124287.
- Zwartendijk, B.W., van Meerveld, H.J., Teuling, A.J., Ghimire, C.P., Bruijnzeel, L.A. (2023). Rainfall-Runoff Responses and Hillslope Moisture Thresholds for an Upland Tropical Catchment in Eastern Madagascar Subject to Long-Term Slash-and-Burn Practices. Hydrological Processes, 36.