# Materials and methods, and metadata for Freshwater Particulate Organic Radiocarbon for Four Major UK Catchments, 2013-2014. Data taken from 'Aged riverine particulate organic carbon in four UK catchments' Adams et al, 2015 Science of the Total Environment.

## Overview
- Describes field sampling, laboratory analyses, and metadata for freshwater particulate organic radiocarbon (PO14C) across four UK catchments during 2013–2014.
- Catchments included: Ribble (NW England), Conwy (North Wales), Hampshire Avon (South England), and Dee (NE Scotland).
- Provides context on catchment characteristics that influence hydrology and sampling interpretation.

## Field sites and catchment context
- Ribble: NW England, population density ~989 persons/km²; sub-catchments Hodder and Calder; includes industrial/mining history in Calder; upper catchment shows flashy response to rainfall.
- Conwy: Major Welsh drainage; population density ~49 persons/km²; mountainous topography with high river response during storms.
- Hampshire Avon: Southern England; population density ~108 persons/km²; groundwater-dominated due to chalk aquifers; tidal limit shows limited rainfall response.
- Dee: NE Scotland; population density ~4 persons/km² above tidal limit; upper mountainous areas with rapid response to rainfall and snowmelt.

## River sampling protocol
- Water samples (5 L) collected from the tidal limit for all four catchments; additional upstream samples in Ribble and Dee.
- Suspended particulate matter (SPM) extracted by centrifugation (9600 rpm for 30 min; ~10,700 relative centrifugal force) until ~100 mL of SPM+water remained.
- SPM concentration measured as [SPM] from filtered, pre-weighed GF/F filters; total carbon analyzed with two different elemental analyzers.

## Laboratory analyses and measurements
- Carbon content: 
  - [SPM] determined by filtration and reweighing.
  - Total carbon measured with Vario EL elemental analyser (Ribble, Conwy, Avon) and with Thermo Flash 2000 elemental analyser (James Hutton Institute).
- 14C analysis preparation:
  - Graphite targets prepared from CO2 via quantitative recovery in sealed quartz tubes followed by cryogenic CO2 separation.
  - CO2 reduced to iron/graphite (Fe/Zn reduction) for AMS.
  - A subsample of CO2 converted to graphite for AMS measurement.
  - δ13C measured using dual-inlet mass spectrometry to correct 14C data to -25‰ δ13CVPDB.
- Labs and facilities:
  - Most 14C analyses conducted at SUERC AMS Laboratory (East Kilbride); three samples analyzed at UCIAMS (Keck Carbon Cycle AMS, University of California Irvine) for small sample sizes (<500 μg C).
- Standards and calibration:
  - Size-matched process blanks and age standards used to check accuracy and precision.
  - Results reported as absolute percent modern carbon (pMC) with decay-age corrections relative to AD 1950.
  - Bomb carbon possibilities recognized; analytical precision for δ13C reported as ±0.03 ‰; overall 14C analytical precision provided as 1σ.

## Data structure and metadata
- Column heading explanations for Riverine_PO14C_Raw_Data include:
  - Catchment: name of the study catchment; Site: river/site name; Flow: qualitative flow condition (e.g., High/Low).
  - Lat/Long: geographic coordinates.
  - Publication code: unique code assigned at analysis stage.
  - Date: sampling date.
  - d13CVPDB‰: stable carbon isotope composition.
  - 14C pMC: radiocarbon content (% modern carbon).
  - +/- 1σ PMC: analytical error in pMC (1σ).
  - [SPM]: suspended particulate matter concentration (mg/L).
  - %OC: organic carbon content (%).
- The dataset links sample measurements to metadata via Publication code and includes date, location, and observational notes.

## Data quality, challenges, and considerations (analyst perspective)
- Use of two different total carbon instruments requires careful inter-calibration to ensure consistency across sites.
- Cross-lab analyses (SUERC vs. UCIAMS) necessitate harmonized quality controls and transparent uncertainty propagation.
- δ13C corrections are essential for accurate 14C interpretation; precision is high (±0.03‰) but still requires careful handling.
- Data at multiple scales (tidal limits vs. upstream samples) and varying catchment demographics demand careful geographic and hydrological interpretation.
- Documentation of metadata (dates, coordinates, flow notes, and publication codes) supports reproducibility and data discoverability.
- The dataset emphasizes rigorous provenance, with explicit references to standard references and calibration materials, enabling traceability from field sample to reported pMC.