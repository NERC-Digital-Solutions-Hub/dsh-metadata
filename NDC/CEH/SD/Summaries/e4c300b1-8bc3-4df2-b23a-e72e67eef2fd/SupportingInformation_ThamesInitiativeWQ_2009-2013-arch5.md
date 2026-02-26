# Brief description of the dataset

## Overview
- Weekly water quality monitoring dataset covering seven sites along the River Thames and fifteen major tributaries.
- Timeframe: March 2009 to February 2013.
- Measured parameters include: phosphorus and nitrogen species, dissolved reactive silicon, water temperature, pH, Gran alkalinity, suspended solids, chlorophyll, major dissolved anions (fluoride, chloride, bromide, sulphate) and cations (sodium, potassium, calcium, magnesium, boron); dissolved and total iron, manganese, zinc, copper (Aug 2010–Feb 2013); accompanying daily river flow data.
- Part of the Centre for Ecology & Hydrology's Thames Initiative monitoring programme.

## Data collection and measurement methods
- Bulk samples collected from the main flow weekly (Monday or Tuesday); subsamples filtered in the field (0.45 μm WCN membrane).
- In-lab handling: samples stored in the dark at 4°C before analysis.
- Measurements and instruments include:
  - pH using Radiometer PHM210 with NIST-traceable buffers.
  - Gran alkalinity by acidimetric titration to pH 4 and 3.
  - Suspended solids by filtration, drying, and weighing.
  - Chlorophyll by filtration, acetone extraction, and spectrophotometry (Marker et al. method).
  - Total phosphorus (TP) and total dissolved phosphorus (TDP) via digestion and spectrophotometric detection.
  - Soluble reactive phosphorus (SRP) by colorimetric method after filtration.
  - Dissolved reactive silicon by molybdate reduction to silicomolybdenum blue and spectrophotometry.
  - Ammonium by indophenol-blue method.
  - Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN) by thermal oxidation (199x–2010) and Elementar system (from 2011).
  - Major dissolved cations/anions by ion chromatography; cations by ICP-OES after acidification.
- Quality control standards: analyses conducted with Aquacheck QC standards (except noted).

## Data structure and format
- Date/time: day/month/year with sampling time in hour:minute.
- Parameter definitions and units provided (e.g., TP, TDP, SRP, DOC, TDN, chlorophyll a, metal concentrations, etc.).
- Flow data: mean daily flow in cubic metres per second.
- Site-specific flow context: most sites near Environment Agency gauging stations; several exceptions described (e.g., Jubilee River flow data downstream of Windsor; some sites with interpolated or upstream gauging data).
- Location metadata: accompanying CEH Thames Initiative SamplingSiteLocations file describing gauging stations used for each site.

## Data provenance and site/flow details
- Flow data sourced from the National River Flow Archive; site-specific notes:
  - Jubilee River flows from Windsor (downstream amalgamation).
  - Hannington Wick, Wallingford, Sonning flows interpolated by catchment area.
  - Cut and River Kennet sites supplied with upstream gauging data.
- The dataset is tied to the Thames Initiative monitoring programme, with site locations and gauging references documented.

## Data quality, reproducibility, and governance
- Methods and references documented for each analytical technique (e.g., Eisenreich 1975; Leeks et al. 1997; Marker et al. 1980; Mullin & Riley 1955; Murphy & Riley 1962; Neal et al. 2000).
- QA practices include use of reference standards and method-specific calibration details; SRP analyzed within 48 hours to minimize instability.
- Analytical method changes noted (DOC measurement method switched from Thermalox to Elementar in 2011), which has implications for harmonization across the time series.

## Metadata, access, and reuse considerations
- Comprehensive methodological metadata provided, enabling reproducibility and cross-site comparison.
- Dataset supports data governance needs for large-scale, long-term water quality datasets: standardized sampling, clear documentation of methods, and metadata for data discovery.
- Important governance considerations for data stewards:
  - Maintain consistency across sites and time, especially where analytical methods changed.
  - Document and manage data gaps, interim methods, and site-specific flow data peculiarities.
  - Ensure accompanying site-location and gauging data files remain linked to the core measurements for proper data discovery and reuse.

## Key references
- Eisenreich, Bannerman & Armstrong (1975)
- Leeks et al. (1997)
- Marker et al. (1980)
- Mullin & Riley (1955)
- Murphy & Riley (1962)
- Neal, Neal & Wickham (2000)