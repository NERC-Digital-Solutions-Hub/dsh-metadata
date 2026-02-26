# Land Ocean Carbon Transfer (LOCATE) Monthly river sampling dataset

- Multidisciplinary NERC project involving National Oceanography Centre, British Geological Survey, Centre for Ecology and Hydrology, Plymouth Marine Laboratory, with several universities and the Environment Agency
- Aim: improve understanding of carbon flow from land into the ocean, focusing on rivers (companion dataset covers estuaries)

## Aims, scope and outputs
- Provides information on geographical and seasonal variation in carbon fluxes from land to rivers
- 2017 field campaign: 41 rivers across England, Scotland and Wales; sampling Jan–Dec 2017 with additional samples in Nov 2016
- Rivers chosen to reflect different land-use types
- Data intended to support modelling efforts and integration with environmental datasets (EA data for modelling datasets)

## Sampling design and regime
- Monthly sampling at a fixed site on each river; most sites sampled within a 2–3 day window each month
- Dorset Stour had a delayed start (sampled from April 2017)
- Sampling coordination led by Andy Tye (BGS)
- After an initial test, most sites moved to HMS sites to facilitate data integration

## Field sampling procedures
- Field processing: most sample filtering/separation done in the field; POC filtered in lab on return
- Samples kept in the dark in cool boxes or freezers during transport
- In-field measurements: salinity, conductivity (SEC), and temperature where possible; weather and river conditions recorded; photos taken upstream and downstream
- Sample collection depth: ~0–30 cm mid-channel; representative of main river body
- Vessel rinsing, handling, and contamination prevention practices followed (gloves, triplicate rinses)
- Sample types and handling:
  - Particulates (POC, PON, 13C, 15N): two 1 L bottles for return to lab
  - Nutrients, DOM, alkalinity, pH: specified bottle types and rinsing protocols
  - Temperature, conductivity, salinity: field measurements with appropriate equipment
- Transport: samples moved to institutes for filtering and lab analyses; cool box or freezer used for transport

## Field blanks and quality control in the field
- Field blanks implemented for each batch of filters (not at every site)
- Process: Milli-Q water blanks prepared and tested
- Responsible groups perform blanks for their analyses:
  - BGS for fluorescence blanks
  - CEH Lancaster for nutrients
  - NOC for POC
- Blank procedures include unfiltered and filtered Milli-Q water end-points for respective analyses

## Laboratory analyses, instrumentation and methods
- Nutrients, pH, and alkalinity: detailed instrumentation (NH4-N, NO3-N, NPOC, PO4-P, TDC, TN, TP, pH, alkalinity) with specified UKAS ISO 17025-aligned methods and detection limits
- Isotopes and carbon/nitrogen analysis: crossflow with Flash EA 1112 Elemental Analyzer linked to DeltaPlus XP IRMS; δ13C and δ15N normalized to USGS reference materials
- Calibration and reference materials: USGS40/USGS41a; long-term QC with dried milled topsoil standard
- Fluorescence and absorbance: Varian Cary Eclipse (fluorescence) and Varian Cary 60 (absorbance) with standard blanks and quinine sulphate calibrations
- Fluorescence data processed with PARAFAC modelling (MATLAB DOMFluor v1.7)
- Absorbance scanned 200–800 nm; absorbance units in cm-1; Raman units used for fluorescence after correction
- QA: blanks and standards run with each batch; instrument sensitivity checked daily

## Isotope and carbon/nitrogen data processing
- Isotopic and elemental concentrations reported as weight percentages and isotope ratios
- Calibration scales aligned to international references; results are traceable to standard reference materials
- QA metrics include long-term precision for carbon, nitrogen and isotope standards

## River and catchment context
- Land cover and catchment-context data applied to each river:
  - CEH Land Cover Map 2015 and associated variables (arable land, woodlands, grasslands, freshwater areas, urban areas, etc.)
  - Peat soil presence and area
  - Catchment area, mean altitude, and other geographical descriptors
  - Base Flow Index (BFI) and carbonate rock fraction
  - Standardised rainfall data (NRFA indicators)
- Data integration metadata includes:
  - River_code, Date, Trip_number, Sampling_time_GMT, River_sample_ID
  - Environmental conditions (weather, sampler_comments, flow and level)
  - Instrumentation readings (temperature, conductivity, salinity)
  - chemical concentrations (NH4-N, NO3-N, NPOC, PO4-P, TDC, TN, TP, pH, alkalinity)
  - DOM and POC/PON measurements, δ13C/δ15N where applicable
  - PARAFAC component loadings and fluorescence indices
  - Absorbance data (abs254, abs340)
  - Various sample-quality and methodology flags

## Companion dataset and data accessibility
- LOCATE produces a companion estuarine dataset for the land-to-ocean carbon transfer project
- The dataset emphasizes standardized formats and interoperability to support policy and environmental monitoring over time

## Relevance and challenges for environmental monitoring
- Demonstrates standardized, multi-parameter monitoring of riverine carbon fluxes across regions and seasons
- Challenges addressed include integrating multiple data streams and improving data reuse by linking to broader environmental datasets
- Designed to support transparent assessment of carbon transfer dynamics and inform monitoring and policy performance over time