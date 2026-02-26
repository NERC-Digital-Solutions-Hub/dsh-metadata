# Brief description of the dataset

## Overview
- Weekly water quality monitoring data from seven sites along the River Thames and fifteen major tributaries (UK).
- Timeframe: March 2009 to February 2013.
- Measured parameters include phosphorus species (TP, TDP, SRP), nitrogen species (TDN, NH4), dissolved reactive silicon, water temperature, pH, Gran alkalinity, suspended solids, chlorophyll a, major dissolved anions (F, Cl, Br, nitrite, nitrate, sulfate) and cations (Na, K, Ca, Mg, B), plus dissolved and total metals (Fe, Mn, Zn, Cu) from Aug 2010 to Feb 2013.
- Daily mean river flow data accompany the quality data.
- Part of the Centre for Ecology & Hydrology's Thames Initiative monitoring programme.

## Monitoring and analytical information
- Sampling protocol:
  - Bulk samples collected from the main flow on Mondays or Tuesdays each week.
  - Subsamples filtered in the field through a 0.45 μm membrane filter.
  - Samples stored in the dark at 4°C before analysis.
- Analytical methods (selected highlights):
  - pH measured with a Radiometer PHM210; calibrated with pH buffers (4, 7, 10).
  - Gran alkalinity determined by acidimetric titration (pH 4 and 3).
  - Suspended solids: filter, dry, and reweigh.
  - Chlorophyll a: filtration, acetone extraction, and spectrophotometric quantification.
  - Total phosphorus (TP) and total dissolved phosphorus (TDP): persulfate digestion with molybdenum blue colorimetry.
  - Soluble reactive phosphorus (SRP): filtration and Murphy–Riley method.
  - Dissolved reactive silicon (DSi): molybdate reaction followed by reduction and spectrophotometry.
  - Ammonium: indophenol-blue colorimetric method.
  - DOC and TDN: thermal oxidation (Thermalox) until 2010, then Elementar Vario Cube.
  - Major dissolved anions: ion chromatography.
  - Total and dissolved cations: ICP-OES after acidification.
- Quality control:
  - All analyses conducted with reference Aquacheck QC standards.

## Data format and variables
- Date/time format: day/month/year; sampling time in hour:minute.
- Key variables and units (examples):
  - TP, TDP, SRP: micrograms P per liter (μg P/L)
  - Ammonium: milligrams NH4+ per liter (mg/L)
  - DSi: milligrams Si per liter (mg/L)
  - Chlorophyll a: micrograms per liter (μg/L)
  - Major dissolved anions/cations: milligrams per liter (mg/L) (e.g., F, Cl, Br, NO2, NO3, SO4, Na, K, Ca, Mg, B)
  - Dissolved metal concentrations: micrograms per liter (μg/L) for Fe, Mn, Zn, Cu
  - Total metals: same units, from unfiltered samples
  - Flow data: mean daily flow in cubic metres per second (m3/s)
- Note: Total phosphorus equals dissolved plus acid-extractable particulate phosphorus in unfiltered samples.

## Site context and data sourcing
- Flow data originate from the National River Flow Archive.
- Special cases:
  - Jubilee River: flow data from Windsor (downstream amalgamation with Thames).
  - Thames sites at Hannington Wick, Wallingford, Sonning: flows interpolated from catchment-area data.
  - Cut and River Kennet sites: flows from gauging stations upstream.
- Site locations and sampling details are documented in the CEHThamesInitiative_SamplingSiteLocations file.

## Uses and potential workflows
- Suitable for time-series analysis of nutrient and metal dynamics across multiple sites and in relation to river flow.
- Can support data integration projects, dashboards, or self-serve exploration for water quality monitoring.
- Data quality and harmonization facilitated by standardized sampling/analytical methods and QC standards.

## References (methods and background)
- Eisenreich, Bannerman & Armstrong (1975)
- Leeks et al. (1997)
- Marker et al. (1980)
- Mullin & Riley (1955)
- Murphy & Riley (1962)
- Neal, Neal & Wickham (2000)