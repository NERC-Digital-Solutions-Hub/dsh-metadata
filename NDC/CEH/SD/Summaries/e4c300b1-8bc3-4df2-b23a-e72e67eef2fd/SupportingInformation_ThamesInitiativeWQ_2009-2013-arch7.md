# Brief description of the dataset

- Weekly water quality monitoring data for seven River Thames sites and fifteen major tributaries, March 2009 to February 2013, with daily river flow data. Includes a wide set of chemical, physical, and biological parameters and is part of the Centre for Ecology & Hydrology's Thames Initiative monitoring programme.

## Overview

- Provides long-term, spatially distributed water quality observations to support assessment of river conditions and trends.
- Data are complemented by mean daily flow data to enable hydrological context and correlation analyses.

## Spatial and Temporal Coverage

- Sites: 7 River Thames sites plus 15 major tributaries.
- Time period: March 2009 – February 2013 (weekly sampling; bulk samples collected Monday/Tuesday each week).
- Flow data: Mean daily flow (m3/s) supplied; most sites near Environment Agency gauging stations.
- Special flow notes:
  - Jubilee River site flows from Windsor (downstream of the monitoring site).
  - Hannington Wick, Wallingford, Sonning flows interpolated from catchment-area-based estimates.
  - Cut and River Kennet flows sourced from gauging stations upstream of sites.
- Site locations recorded in CEHThamesInitiative_SamplingSiteLocations file.

## Variables Measured

- Water quality parameters:
  - Phosphorus and nitrogen species; dissolved reactive silicon; water temperature; pH; Gran alkalinity; suspended solids; chlorophyll a.
  - Major dissolved anions: fluoride, chloride, bromide, sulfate; cations: sodium, potassium, calcium, magnesium, boron.
  - Dissolved and total iron, manganese, zinc, copper (from Aug 2010 to Feb 2013).
- Nutrients and related measures:
  - Total phosphorus (TP) and total dissolved phosphorus (TDP)
  - Soluble reactive phosphorus (SRP)
  - Dissolved reactive silicon (DSi)
  - Ammonium
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN)
- Major ions and metals measured in both dissolved and total forms as appropriate.
- Flow: mean daily river flow (m3/s).

## Sampling, Analytical Methods, and Quality Control

- Sampling: Bulk samples from main flow (Mon/Tue) weekly; subsamples filtered in the field (0.45 μm filter).
- Sample handling: Stored in the dark at 4°C.
- Analyses (examples):
  - pH by Radiometer pH meter with NIST-traceable buffers.
  - Gran alkalinity by acidimetric titration to pH 4 and 3.
  - Suspended solids by filtration and reweighing.
  - Chlorophyll a by filtration, acetone extraction, and spectrophotometry.
  - TP/TDP by acidified persulfate digestion and spectrophotometric measurement.
  - SRP by filtration and phosphomolybdenum blue colorimetry.
  - DSi by molybdate-based colorimetry with silicomolybdenum blue reduction.
  - Ammonium by indophenol-blue method.
  - DOC/TDN by Thermal Oxidation (until 2010) and Elementar Vario Cube (from 2011).
  - Major ions by ion chromatography.
  - Major metals by ICP-OES (unfiltered/differs by dissolved vs total).
- Quality control: Analyses performed with reference Aquacheck QC standards; standardized methods and instruments referenced.

## Data Format and Units

- Date/time format: day/month/year with sampling time in hour:minute.
- Concentration units include micrograms per liter (μg/L), milligrams per liter (mg/L), micrograms per liter for metals, micrograms P per liter for phosphorus species, chlorophyll a in μg/L, and flow in m3/s.
- Temperature in degrees Celsius; pH as a unitless measure.
- Alkalinity given in micro-equivalents per liter (μEq/L).
- Spatial and temporal alignment allows creation of time-series and map-based visualizations.

## Related Data Sources and Accessibility

- Flow data sourced from National River Flow Archive (NRFA).
- Proximity to Environment Agency gauging stations; some sites use upstream or interpolated flow data.
- Site locations available in CEHThamesInitiative_SamplingSiteLocations.

## Data Quality, Standards, and Considerations for GIS Use

- Data collected using standardized laboratory methods with QC standards; documentation includes method references.
- Some flows are interpolated or sourced from gauges upstream/ downstream, which may affect precise hydrological attribution at specific sites.
- Users should account for:
  - Missing weeks at some sites or periods.
  - Flow data source variability (direct gauge vs. interpolated).
  - Potential changes in analytical methods over time (e.g., DOC/TDN instrumentation) when performing long-term trend analyses.
- The dataset is well-suited for spatial mapping of water quality by site and temporal trend analysis, especially when combined with the site locations file and flow context.

## Potential GIS Applications

- Create spatial maps of nutrient, metal, and major ion concentrations across sites and over time.
- Analyze relationships between flow and water quality parameters.
- Develop time-series dashboards per site or per tributary.
- Integrate with other hydrological or ecological layers to assess impacts on riverine ecosystems.

## References

- Eisenreich, S. J., R. T. Bannerman & D. E. Armstrong, 1975. A simplified phosphorus analytical technique.
- Leeks, G. J. L., et al., 1997. The LOIS river monitoring network: strategy and implementation.
- Marker, A. F. H., et al., 1980. The measurement of photosynthetic pigments in freshwaters.
- Mullin, J. B. & J. P. Riley, 1955. Colorimetric determination of silicate.
- Murphy, J. & J. P. Riley, 1962. Phosphorus determination in natural waters.
- Neal, C., et al., 2000. Phosphate measurement in natural waters: silica interference.