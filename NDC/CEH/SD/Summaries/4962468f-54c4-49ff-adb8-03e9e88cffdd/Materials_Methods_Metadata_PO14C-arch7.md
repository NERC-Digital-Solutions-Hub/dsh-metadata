# Materials and methods, and metadata for Freshwater Particulate Organic Radiocarbon for Four Major UK Catchments, 2013-2014. Data taken from 'Aged riverine particulate organic carbon in four UK catchments' Adams et al, 2015 Science of the Total Environment.

## Overview
- Presents materials, methods, and metadata for freshwater particulate organic radiocarbon (PO14C) across four major UK catchments (data from 2013–2014; see Adams et al., 2015).
- Data primarily include 14C and 13C measurements of suspended particulate matter (SPM) from river water samples, plus related sample and site metadata.
- Most radiocarbon analyses were performed at SUERC (Scotland) with three measurements at UC Irvine; results reported as absolute percent modern carbon (pMC) with 1σ precision.
- Metadata and column definitions are provided to support GIS integration and map-based data exploration.

## Field sites and spatial context (GIS relevance)
- Four catchments described:
  - Ribble (north-west England): high population density (989/km2); sub-catchments Hodder and Calder (Calder with significant urban/industrial history).
  - River Conwy (North Wales): population density ~49/km2; mountainous topography; strong river response to rainfall.
  - Hampshire Avon (south England): population density ~108/km2; groundwater-dominated due to chalk aquifers; tidal limit shows limited rainfall response.
  - River Dee (north-east Scotland): population low above tidal limit (~4/km2); upper mountainous reaches with rapid response to rainfall/snowmelt.
- Sampling design and spatial data:
  - Samples collected at tidal limits; some upstream samples in Ribble and Dee.
  - Data include latitude/longitude and site-level identifiers to enable GIS mapping and spatial analyses.
- Relevance for GIS specialists:
  - Facilitates creation of map layers showing catchment boundaries, sampling sites, hydrological regimes, and land-use contrasts (e.g., Calder industrial/mining area).
  - Supports multi-resolution data integration (catchment-scale attributes + point sample data).

## Sampling and analysis workflow
- Sample collection:
  - 5 L water samples collected from tidal limits; additional upstream samples in some catchments.
  - Suspended particulate matter (SPM) isolated via high-speed centrifugation until ~100 mL of SPM-water mixture remained.
- Carbon content determination:
  - [SPM] estimated by filtering a known volume of water, drying filters, and reweighing.
  - Total carbon measured with elemental analyzers (Vario EL or Thermo Flash 2000) at respective laboratories.
- Radiocarbon (14C) analysis:
  - Graphite targets prepared from CO2 (cryogenic separation) and reduced to iron/graphite mix for AMS.
  - δ13C measured to correct 14C data; mass spectrometry calibration to VPDB standard.
  - Most analyses performed at SUERC; three measurements at UC Irvine (UCIAMS). Standards and process blanks used to ensure accuracy.
  - Results expressed as pMC relative to 1950 AD, accounting for bomb carbon; conventional radiocarbon ages provided where applicable.
  - Analytical precision cited as 1σ.
- Data quality and reporting:
  - Use of standardized reference materials and international calibration practices.
  - Correction for δ13C applied to 14C data to improve comparability.

## Data schema and metadata (for GIS integration)
- Column heading explanations (examples):
  - Catchment: Name of study catchment; Catchment Units: plain text; Flow: qualitative condition (e.g., High/Low); Lat/Long: geographic coordinates; Date: sample collection date.
  - Site: river within catchment; d13CVPDB‰: stable carbon isotope value; 14C pMC: radiocarbon content; +/- 1σ PMC: analytical uncertainty.
  - [SPM]: Suspended particulate matter concentration (mg/L); %OC: organic carbon content (percent).
  - Publication code: unique data-analyses code; Date: sample collection date; other notes: placeholder for additional context.
- Data products and usage:
  - Enables spatial visualization of PO14C distribution across catchments.
  - Supports integration with other GIS layers (e.g., land use, hydrology, population density, topography).
- Standards and QA:
  - Metadata documents units, methods, and uncertainties; supports reproducibility and cross-study comparisons.

## References and methodological context
- Core methodological references and standard practices cited:
  - Boutton et al. 1983; Slota 1987 for preparation and calibration techniques.
  - Xu et al. 2004 for SUERC 5MV AMS capabilities.
  - Stuiver & Polach 1977 for reporting radiocarbon data.
- Data interpretation notes:
  - pMC values can exceed 100 due to bomb carbon; conventional radiocarbon ages provided where applicable.
  - 1σ precision indicates analytical uncertainty around pMC measurements.

## Notes on applications for GIS specialists
- This dataset provides spatially explicit radiocarbon and organic-carbon measurements in riverine SPM, suitable for mapping temporal and spatial trends in freshwater carbon cycling.
- The inclusion of precise site coordinates, catchment attributes, and standardized metadata supports robust GIS analyses, data fusion with ancillary layers, and transparent data provenance.