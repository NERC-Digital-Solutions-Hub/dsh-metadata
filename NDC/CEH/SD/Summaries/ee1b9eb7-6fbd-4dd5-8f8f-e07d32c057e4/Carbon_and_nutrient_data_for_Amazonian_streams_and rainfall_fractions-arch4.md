# Sampling Regime

## Overview
- Spatial focus: Western Amazonian basin, Tambopata National Reserve, Madre de Dios, Peru (approx. 12°49' S, 69°16' W).
- Temporal window: February 2011 – May 2012; multiple field campaigns (Feb–Apr 2011; Sept–Dec 2011; Mar–May 2012) for fluvial carbon data; rainfall fractions sampled Apr–May 2012.
- Data types: dissolved inorganic carbon (DIC) and its δ13C in DIC, dissolved organic carbon (DOC), particulate organic carbon (POC); rainfall fractions including rain water, throughfall, stemflow, and overland flow; supporting nutrients and major ions (Ca, Mg, K, Na, P, Si) in water.
- Purpose: capture hydrological controls on carbon concentrations/fluxes across wet and dry seasons; assess data completeness and provide a basis for synthesis with previous submissions.

## Data coverage and structure
- Streams and rivers sites: NC (New Colpita), MT (Main Trail), LT (La Torre), TP (Tambopata).
- Catchment context: NC and MT upstream areas are smaller; LT (~2000 km2) and TP (~14000 km2) contribute to broader regional hydrology.
- Data availability notes: DIC and δ13C-DIC data previously submitted for small streams (DOI: 10.5285/507a5e1f-e056-454c-8ff6-d185f3da8556) and rivers (DOI: 10.5285/02d5cea710aa-4591-938a-a41e1c5bc207); rainfall fractions data submitted here.

## Sampling design and field methods
- Fluvial sampling: three campaigns targeting varying flow conditions to understand hydrological controls on carbon.
  - DIC, δ13C-DIC, DOC, POC concentrations measured; subset of samples analyzed for nutrients.
  - MT stream dries in the dry season; no samples Sept–Nov 2011 for MT.
- Rainfall fractions sampling: throughfall collectors near TAM9 plot; stemflow sampled from eight tree species; overland flow collected along stream banks.
- Collection details:
  - DIC: pre-acidified exetainers; headspace analysis for DIC concentration and δ13C-DIC.
  - DOC: filtered water, acidified, degassed, analyzed by combustion (TOC analyzer).
  - POC: measured by loss on ignition of dried filter papers.
  - Cations (Ca, Mg): atomic absorption spectrometry (AAS).
  - Anions/solutes (K, Na): flame photometry.
  - TotP: colorimetric method via phosphomolybdate complex reduction.
  - Si: colorimetric (heteropoly blue molybdosilicate).
- Quality-control in the field: triplicate exetainers for DIC; randomised sample order; repeated standards and drift checks across runs.

## Data structure and formats
- Data files: 
  - Amazon streams C and nutrients (streams and rivers)
  - Amazon rainfall fractions C and nutrients (rainfall fractions)
- Data columns:
  - Streams and Rivers: Time, Date, Type (stream or river), Site (MT, NC, LT, TP), CollectorID, DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si.
  - Rainfall fractions: Time, Date, Type (TF, SF, OF, RW), CollectorID (TF: collector number; SF: tree name; OF: stream; RW: rain water).
  - Note: some columns may be NA when data were not analysed.
- Column counts: 14 columns for streams/rivers; 12 columns for rainfall fractions.

## Calibration and measurement specifics
- DIC: multi-point standards; triplicate measurements with different isotopic compositions; midrange standard for drift checks.
- DOC: eight-point calibration with blanks and drift checks; samples acidified and degassed prior to analysis.
- POC: calculated from loss on ignition with initial dry weight and subsequent combustion.
- Nutrients and major ions: multi-point calibrations for Ca/Mg (AAS), K/Na (flame photometry); totP and Si calibrations with blanks.
- Data provenance: methodologies aligned with standard methods and referenced literature.

## Data quality control and provenance
- Instrument performance: drift correction standards included after every ~10 samples; randomised sample order.
- Calibration checks: regular drift checks, consistency checks between begin/end calibrations, and duplicate standard analyses.
- Data flags: NA indicates not analysed or unavailable data.
- References and prior submissions:
  - American Public Health Association (1999) standard methods.
  - Waldron et al. (2014) on precision/accuracy of DIC δ13C measurements.
  - Previous data DOIs noted for DIC, DOC, POC data submissions.