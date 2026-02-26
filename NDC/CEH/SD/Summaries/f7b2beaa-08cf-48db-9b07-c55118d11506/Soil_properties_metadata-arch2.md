# Soil chemical properties from a field experiment in the Conwy Valley, North Wales, UK (20156)

- Purpose and scope
  - Documentation of soil chemical properties from a field experiment in the Conwy Valley, North Wales (20156) with metadata for Soil_properties.csv.
  - Aligns with environmental monitoring aims: standardised data collection, quality assurance, and generation of outputs (datasets, maps, charts) for assessing environmental health and policy performance over time.
  - Includes related plot location data (Plot_locations.csv) and its description (Plot_locations_metadata.rtf).

- Experimental design and sampling regime
  - Three 75 m long transects, 20 m apart, across the hillslope perpendicular to a river.
  - Along each transect, intact soil cores were extracted at 2, 12, and 75 metres.
  - Core lengths were determined by maximum soil depth or an impermeable boundary; cores collected in 1 m increments for a total of 18 cores of 1 m length (with possible 2–3 m total depth per core depending on soil profile).
  - Cores (4 cm diameter) were wrapped in thin-walled polyethylene sleeves to maintain integrity and stored at 4°C prior to analysis.
  - Field collection used a Cobra percussion hammer corer.

- Analytical methods (laboratory workflow)
  - Soil moisture content: gravimetric (24 h at 105°C).
  - Organic matter: loss-on-ignition (450°C, 16 h).
  - pH and electrical conductivity (EC): measured in a 1:2.5 soil-to-deionised water suspension.
  - Inorganic nutrients: NH4-N and NO3-N determined from 0.5 M K2SO4 extracts via colorimetric methods (Mulvaney 1996; Miranda et al. 2001).
  - Phosphorus: available P quantified with 0.5 M acetic acid extracts (ascorbic acid–molybdate blue method; Murphy and Riley 1962).
  - Carbon and nitrogen: total C (TC) and total N (TN) by TruSpec elemental analyser.
  - Dissolved fractions: dissolved organic C (DOC) and total dissolved N (TDN) in 1:5 soil-to-0.5 M K2SO4 extracts using a TOC analyzer.
  - Microbial indicators: microbial biomass C and N by chloroform fumigation (72 h incubation; k_ec = 0.45, k_en = 0.54) and PLFA analysis (96-well high-throughput method).
  - Phosphorus sorption: 1.0 g soil shaken with CaCl2 and added P concentrations (0–50 mg P L^-1) labeled with 33P; sorbed P calculated from initial minus remaining in solution; adsorption maxima estimated via Langmuir isotherms.
  - All methods reference established protocols and provide traceable details (e.g., Nair et al. 1984; Santos et al. 2011; MehdI et al. 2007; Buyer and Sasser 2012).

- Data structure and recorded values
  - Primary dataset: Soil_properties.csv with columns described in the data structure section.
  - Key column groups and units:
    - Spatial: Transect, Row
    - Depth: Depth (cm)
    - Soil properties (examples with units):
      - pH (unitless)
      - EC (µS/cm)
      - MC (% moisture content)
      - LOI (% loss on ignition)
      - TOC (mg/g)
      - TDN (mg/g)
      - Microbial_C (mg/g)
      - Microbial_N (mg/g)
      - PO4_P (mg/kg)
      - NH4_N (mg/kg)
      - NO3_N (mg/kg)
      - CtoN_ratio (unitless)
      - TC (g/kg)
      - TN (g/kg)
      - Pmax (mg/kg)
      - NH4Adsorp (mg/kg)
  - Data completeness: Empty cells indicate no data.
  - Data provenance and quality indicators: Samples analyzed in triplicate; data structure notes reference to a detailed description of each column.

- Quality control and data management
  - All samples analyzed in triplicate to ensure analytical precision.
  - Data are intended to be stored and made accessible via appropriate data portals and standardised workflows typical of environmental monitoring programs.

- Supporting materials and data access
  - Plot_locations.csv: details of plot locations.
  - Plot_locations_metadata.rtf: description of Plot_locations.csv.
  - The metadata and data structure documentation underpin reproducibility and cross-study comparability for monitoring analysts.

- Relevance for monitoring and reuse
  - Provides a standardised, QA’d dataset of soil chemical properties across defined transects and depths for temporal/environmental health assessment.
  - The well-documented methods and multiple linked datasets facilitate integration with other environmental datasets and enable broader analysis beyond a single study, addressing the challenge of increasing dataset value by combining data and enabling access to underlying data.