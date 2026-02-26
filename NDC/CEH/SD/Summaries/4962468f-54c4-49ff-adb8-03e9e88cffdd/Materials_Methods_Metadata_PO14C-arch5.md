# Materials and methods, and metadata for Freshwater Particulate Organic Radiocarbon for Four Major UK Catchments, 2013-2014. Data taken from 'Aged riverine particulate organic carbon in four UK catchments' Adams et al, 2015 Science of the Total Environment.

## Overview
- Dataset documents freshwater particulate organic radiocarbon (14C) data for four UK catchments collected in 2013–2014.
- Data source: Adams et al. (2015) Science of the Total Environment; supplemented with methodological details and metadata.
- Includes field sampling strategy, laboratory analyses, data processing steps, and a data dictionary for downstream use.

## Field sites
- Catchments included: Ribble (NW England), Conwy (North Wales), Hampshire Avon (South England), and Dee (NE Scotland).
- Each catchment characterized by population density and hydrology (e.g., Ribble with conurbations along Calder; Avon is groundwater-dominated; Dee shows rapid upper catchment response; Ribble upper parts are flashy).
- Sampling locations: tidal-limit water samples from the four catchments; additional upstream samples for Ribble and Dee.

## River sampling and analysis
- Sample collection: 5 L water per sample using high-density polyethylene containers.
- Suspended particulate matter (SPM) isolation: repeated centrifugation (≈9600 g for 30 min) to obtain ~100 mL of SPM-water mixture.
- Organic carbon content (%OC) and SPM concentration ([SPM]) measured via two techniques:
  - Filtering a subsample on pre-weighed, pre-combusted GF/F filters to determine [SPM]/%OC.
  - Total carbon analyses with Vario EL (Ribble, Conwy, Avon) and Thermo Flash 2000 (James Hutton Institute).
- 14C analysis preparation: graphite targets produced from CO2 via iron/zinc reduction after quantitative carbon recovery in sealed quartz tubes; CO2 measured for δ13C correction.
- δ13C measurement: dual-inlet mass spectrometry (ΔV) for δ13C with precision ≈ ±0.03‰; calibrated against international standards.

## 14C data processing and calibration
- 14C dating performed as absolute percent modern carbon (pMC), with adjustments for bomb carbon when applicable.
- Conversion to iron/graphite targets and AMS analysis performed primarily at SUERC (East Kilbride) with three smaller samples at UCIAMS (University of California Irvine) for <500 μg C.
- δ13C used to correct 14C data; multiple international reference materials and standard calibrations ensured accuracy.
- Reported analytical precision: 1σ for 14C pMC values; δ13C precision per instrument calibration (δ13CVPDB‰).
- Data interpretation follows standard radiocarbon dating practice relative to AD 1950.

## Data structure and metadata (Column heading explanations)
- Column fields include: Catchment, Site, Flow, Lat, Long, Publication code, Date, d13CVPDB‰, 14C pMC, ±/1σ PMC, [SPM], %OC, etc.
- Descriptions provide units and plain-text notes for each field to facilitate interpretation and interoperability between datasets.
- Publication codes indicate the analysis lab (SUERC or UCIAMS) and stage of data processing.

## Quality control and provenance
- Size-matched process background materials and known-age standards used to check accuracy/precision.
- Cross-lab checks (SUERC vs. UCIAMS) for consistency on select samples.
- Documentation includes detailed methodology and a data dictionary to support reproducibility and data reuse.

## References
- Methodological and calibration references for radiocarbon dating and carbon analysis:
  - Boutton et al. 1983; Slota 1987; Xu et al. 2004; Stuiver & Polach 1977.
- Primary data source: Adams et al. 2015, Science of the Total Environment (Aged riverine particulate organic carbon in four UK catchments).