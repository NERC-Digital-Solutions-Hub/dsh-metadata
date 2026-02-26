# Brief description of the dataset

## Dataset Overview
- Weekly water quality monitoring data for seven sites along the River Thames and fifteen major tributaries.
- Time period: March 2009 to February 2013.
- Measured parameters include phosphorus and nitrogen species, dissolved reactive silicon, water temperature, pH, Gran alkalinity, suspended solids, chlorophyll, major dissolved anions (fluoride, chloride, bromide, sulphate) and cations (sodium, potassium, calcium, magnesium, boron).
- Dissolved and total iron, manganese, zinc, and copper concentrations produced from August 2010 to February 2013.
- Accompanying daily river flow data supplied.
- Part of the Centre for Ecology & Hydrology's Thames Initiative monitoring programme.

## Sampling and Analytical Methods
- Bulk samples taken from the main flow weekly on Monday or Tuesday; subsamples filtered in the field through a 0.45 μm Whatman WCN membrane.
- In-lab storage: dark, 4°C prior to analysis.
- pH measurement: Radiometer PHM210, calibrated with pH 4, 7, 10 buffers traceable to NIST.
- Gran alkalinity: acidimetric titration to pH 4 and 3 with 0.5N H2SO4.
- Suspended solids: filtration of ~500 mL through pre-dried GF/C filter; filter dried (16 h at 80°C) and weighed.
- Chlorophyll: filtration of ~500 mL unfiltered water, extraction in 10 mL 90% acetone/water, spectrophotometric analysis after refrigeration in the dark.
- Total phosphorus (TP) and total dissolved phosphorus (TDP): digestion with acidified potassium persulphate; complex formation with ammonium molybdate; spectrophotometric measurement at 880 nm.
- Soluble reactive phosphorus (SRP): filtered sample analyzed by phosphomolybdenum blue method; analyzed within 48 h.
- Dissolved reactive silicon (DRSi): reaction with acid ammonium molybdate, reduction with tin(II) chloride; spectrophotometric quantification.
- Ammonium: indophenol-blue colorimetric method using a Seal Auto Analyser 3.
- DOC and TDN: thermal oxidation (to Dec 2010) and Elementar Vario Cube (from 2011).
- Major dissolved anions: ion chromatography (Dionex AS50).
- Total and dissolved cations: acidification followed by ICP-OES.
- All analyses (except suspended solids) run with reference Aquacheck QC standards.

## Data Format and Content
- Date/time: day/month/year; sampling time: hour:minute.
- Concentration data expressed per parameter (e.g., TP, TDP, SRP, DRSi, various ions and metals, chlorophyll, etc.).
- Flow data: mean daily average flow in cubic metres per second.
- Distinctions:
  - Total phosphorus vs dissolved phosphorus (unfiltered vs 0.45 μm filtered).
  - Dissolved vs total metal concentrations (unfiltered vs filtered samples).

## Site and Flow Data Details
- Most sites near Environment Agency gauging stations.
- Jubilee River flow data sourced from Windsor (river Thames at Windsor, downstream of Jubilee River; amalgamated flows).
- Some Thames sites: flows interpolated based on catchment areas using multiple gauging data.
- Cut and River Kennet sites have flow data from gauging stations upstream of the monitoring sites.
- Gauging stations used for each site listed in the CEHThamesInitiative_SamplingSiteLocations file.

## Data Provenance and Quality Assurance
- Analytical methods and references established in notable literature.
- Quality control using Aquacheck QC standards.

## References
- Eisenreich, Bannerman & Armstrong (1975)
- Leeks et al. (1997)
- Marker et al. (1980)
- Mullin & Riley (1955)
- Murphy & Riley (1962)
- Neal, Neal & Wickham (2000)

## Relevance for Analysts Monitoring the Environment
- Standardised, traceable methods enable time-series analysis and policy performance assessment.
- Includes both water quality and hydrological context (daily flow).
- Data are linked to CEH Thames Initiative and NRFA, facilitating integration with other environmental datasets.
- Considerations for increasing data value:
  - Potential for combining with additional datasets (e.g., ecological indicators, land-use data).
  - Emphasis on making underlying data accessible to downstream users and researchers.