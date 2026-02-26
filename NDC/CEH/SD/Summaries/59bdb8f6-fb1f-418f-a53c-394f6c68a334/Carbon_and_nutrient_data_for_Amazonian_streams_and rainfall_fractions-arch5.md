# Sampling Regime

## Overview
- Data collected from two small streams (MT, NC) and two rivers (LT, TP) plus rainfall fractions in the Western Amazonian basin, Tambopata National Reserve, Peru, during Feb 2011–May 2012.
- Targeted dissolved inorganic carbon (DIC) and its δ13C-DIC isotopic composition, dissolved organic carbon (DOC), and particulate organic carbon (POC); rainfall fractions analyzed for DOC, POC, and selected DIC/δ13C-DIC.
- MT is seasonally active; NC flows during the dry season as well. Catchment scales are provided for context.

## Datasets and Data Points
- DIC, δ13C-DIC, DOC, POC data with site-specific counts (NC, MT, LT, TP) summarized in Table 1; rainfall fractions data summarized in Table 2.
- Prior data deposits exist for:
  - DIC in small streams (DOI 10.5285/507a5e1f-e056-454c-8ff6-d185f3da8556)
  - DIC in rivers (DOI 10.5285/02d5cea7-10aa-4591-938a-a41e1c5bc207)
- Rainfall fractions data were collected/applied in 2012 and include throughfall, stemflow, overland flow, and rain water.

## Sampling Campaigns and Sites
- Three field campaigns: Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012.
- MT dries up during the dry season, so Sept–Nov 2011 sampling for MT was not possible.
- Sampling targeted varying flow conditions to understand hydrological controls on carbon concentrations and fluxes.

## Measurement Methods
- DIC and δ13C-DIC: headspace method on Thermo-Fisher GasBench/Delta V Plus.
- DOC: filtered water, acidified to pH ~3.9, degassed, analyzed by TOC combustion (Thermalox TOC 2020).
- POC: quantified by loss on ignition (LOI) after drying and combustion.
- Major nutrients:
  - Ca, Mg by Atomic Absorption Spectrometry (AAS).
  - K, Na by flame photometry.
  TOT-P and Si by colorimetric methods (phosphomolybdate/ascorbic acid and heteropoly blue, respectively).
- Rainfall fractions: throughfall, stemflow (eight sampled trees), overland flow, and rain water.

## Sample Handling and Quality Control
- DIC samples: triplicate exetainers; drift corrections using standards; randomised sample order.
- DOC: eight-point calibration with drift checks; blanks included.
- Cations and Si/TotP: calibration and drift checks; repeated standard analyses to ensure instrument stability.
- Documentation notes data points not analyzed (NA) and includes references to prior data submissions.

## Data Structure and File Formats
- CSV files named Amazon streams C and nutrients, and Amazon rainfall fractions C and nutrients.
- Streams/rivers file: 14 columns; Rainfall fractions file: 12 columns.
- Key fields include Time (HH:MM:SS), Date (dd/mm/yyyy), Type (stream or river; TF SF OF R for rainwater), Site (MT, NC, LT, TP or EI for rain), CollectorID, and concentrations for DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si.
- NA indicates data not analyzed. Units are consistent with standard methods (mg/L, μg/L, ‰, etc.) as detailed in the tables.

## Data Availability, Provenance, and Documentation
- Detailed methodological descriptions for sample collection, storage, and analysis are provided, including instrument-specific calibration, drift corrections, and QA procedures.
- Data provenance is reinforced by references to methodological literature (Waldron et al. 2014; American Public Health Association 1999) and linked DOIs for previous data submissions.
- Extensive metadata accompany the dataset to support discoverability and reuse, with explicit notes on sample limitations (e.g., MT not sampled during certain periods) and data completeness (NA entries).

## Reuse Considerations and Limitations
- Data cover both stream and rainfall fraction components with seasonally varying coverage; some samples are missing due to hydrological conditions (e.g., MT drying period).
- Data are suitable for hydro-biogeochemical analyses of carbon and nutrient cycling in tropical rainforest basins, provided citations to the original DOIs and method references are observed.

## References
- American Public Health Association (1999). Standard methods for the examination of water & wastewater.
- Waldron, S., et al. (2014). Quantifying precision and accuracy of measurements of dissolved inorganic carbon stable isotopic composition using continuous-flow isotope-ratio mass spectrometry. Rapid Communications in Mass Spectrometry.