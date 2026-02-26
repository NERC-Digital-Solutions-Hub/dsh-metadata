# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Overview
- Study evaluates how added leaf litter influences suspended organic matter (SOM) stocks in Welsh upland rivers.
- Experimental design: before-after-control-impact (BACI) with upstream reference zones and downstream experimental zones within each stream.
- Timeframe: before period (T1) Nov 2012–early Jan 2013; after period (T2) Jan–Mar 2013 (leaf litter added throughout T2). Additional leaf litter (630 kg wet weight per stream) added on 12 Feb 2013 and 5 Mar 2013 after two storm events.
- Purpose aligned with monitoring aims to identify environmental health measures and inform management decisions about organic matter inputs to streams.

## Experimental design and sampling regime
- Each stream divided into:
  - Upstream reference zone (control)
  - Downstream experimental zone (manipulated)
- Zones are similar in length and habitat; a 20–50 m gap maintained to ensure independence.
- Replication: multiple streams with replicates within each stream (A–F replicate codes mentioned for SOM data).
- Sampling occasions: conducted at the end of before period and during after period, with measurements taken at the lower end of each reach.

## Leaf litter manipulation
- Experimental zone received added leaf litter to simulate natural senescence and abscission in wooded catchments.
- Leaf litter types: oak, birch, and alder; delivered via one tonne bags and vegetable nets to maintain minimum wet weight.
- Additional litter added mid-period after storm events to sustain elevated inputs.

## Data collected: suspended organic matter (SOM)
- SOM defined as suspended particles >10 µm and <1 mm.
- Sampling method: 100 L of stream water filtered through a stacked pair of 10 µm and 1 mm filters at the downstream end of each reach.
- Sampling frequency and timing aligned with BACI design (before vs after manipulation).

## Analytical methods and processing
- SOM samples frozen shortly after collection; freeze-dried and weighed to the nearest 0.0001 g.
- Sub-sampling for analysis of elemental composition (C, N) and stable isotopes (δ13C, δ15N) using mass spectrometry.
- Inorganic content correction performed by combusting a subset of samples at 550°C for 5 h (ash-free conversion).
- Temperature, storage, and laboratory workflows standardized to ensure consistency.

## Nature and units of recorded values
- SOM metrics include:
  - CPOM (coarse particulate organic matter) and FPOM (fine particulate organic matter) per sample (grams).
  - CPOM and FPOM concentrations in water (mg/L).
  - Subsample weights for isotopic and elemental analysis (µg).
  - Isotopic and elemental data: δ13C, δ15N for CPOM and FPOM (with associated comments where applicable).
  - Discharge (L/s) and reach designation (Experimental or Control).
  - Time indicators: before/after manipulation, sampling month and date.
  - Site and reach metadata: site_code, landuse, region, replicate, etc.

## Data structure and quality control
- Data stored as flat CSV files.
- Detailed variable naming and unit definitions provided for all fields (e.g., cpom.g.per.sample, cpom.afdm.mg.l, fpom.d15N).
- Quality control measures include ash-free conversion to adjust organic matter measurements and replication codes to track experimental reliability.
- Supporting site metadata provided to contextualize measurements (site_code, Eastings/Northings, coordinates, elevation, catchment).

## Supporting documents and metadata
- Site description file: DURESS_CU_site_description.csv containing:
  - Site_code, Name, grid references, latitude/longitude, elevation.
  - Survey campaigns and catchment information for context.

## Monitoring and policy-relevant implications
- Provides a standardized, manipulable experiment to quantify how organic matter inputs alter SOM stocks in stream ecosystems.
- BACI design strengthens attribution of observed changes to leaf litter additions rather than natural variability.
- Rich, well-structured data (CPOM/FPOM masses and concentrations, isotopic signatures, discharge, and site metadata) enable cross-site comparisons and trend analysis—useful for evaluating policy scenarios around catchment wood-input management and organic matter subsidies to streams.
- Data governance aspects are evident through explicit data structure, metadata availability, and ancillary site descriptions, illustrating practical considerations for openness, data sharing, and reproducibility in monitoring frameworks.

## Considerations for monitoring framework authors
- The approach demonstrates how to couple ecological manipulation with robust pre- and post-intervention Monitoring Metrics (SOM components and isotopic signatures).
- Highlights the importance of detailed metadata, standardized sampling, and transparent data processing (e.g., ash-free corrections) to ensure data usability for policy evaluation.
- Exemplifies handling data across multiple streams with reference and treatment arms, which is valuable for scalable monitoring programs and inter-jurisdictional comparisons.