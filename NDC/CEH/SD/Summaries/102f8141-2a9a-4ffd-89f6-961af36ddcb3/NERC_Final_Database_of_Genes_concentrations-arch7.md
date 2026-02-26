# Concentration Levels of Resistance Genes in Wastewater and Receiving Environment Brief description of the dataset

## Overview
- Weekly concentrations of the qnrS resistance gene in the South West UK.
- Monitoring period: 7 consecutive days (Wednesday to Tuesday) between June and October 2015.
- Study area: five major wastewater treatment plants (WWTPs) contributing to a single river catchment (~2,000 km2) with ~1.5 million people (>75% of catchment population).
- Sampling focuses on influent and effluent wastewater, plus river water at various upstream/downstream points; one site (Site E) discharges directly to the estuary and river sampling was not conducted there.
- WWTPs employ different treatment technologies (activated sludge, trickling filters; some SBRs).

## Sampling design and laboratory methods
- Sampling frequency and types:
  - Influent wastewater: 24 h composites with ~15-minute sub-samples.
  - Effluent wastewater: time-proportional sampling due to matrix stability.
  - River water: 8 L grab samples, upstream and downstream of discharge points.
- Sample handling: all samples kept on ice during collection and transported to the lab.
- DNA extraction and quantification:
  - Extraction performed from 1 mL unfiltered wastewater, with a specific lysis and purification protocol using a Roche kit.
  - DNA quantified by Nanodrop for quality check.
  - qnrS gene quantified using digital PCR (QuantStudio 3D, high-density nanofluidic chips) with a TaqMan assay.
  - PCR cycling and analysis described, with results processed in AnalysisSuite software.
- Output units: qnrS gene concentrations reported as copies per microliter (µL) of sample.

## Data format and scope
- Data describe concentrations of qnrS in influent and effluent wastewater across monitoring sites during the study week.
- Reported in copies per microliter.
- Spatial scope includes five WWTPs within the catchment; river sampling points provide upstream/downstream context.
- Notable methodological details:
  - Influence of treatment technologies (activated sludge, trickling filters; some SBRs) on observed concentrations.
  - Sampling coordination between wastewater and river sampling days.

## GIS considerations and recommended usage
- Potential map products:
  - Point layers for WWTPs and river sampling locations with time-stamped concentration values.
  - Spatial visualization of qnrS concentrations across the catchment to assess spatial patterns relative to plant type and discharge points.
  - Time-enabled maps showing weekly variation (7-day window) and comparison between influent vs. effluent concentrations.
- Data preparation notes:
  - Harmonize sampling dates and ensure consistent units (copies/µL) across sites.
  - Geocode all sampling locations and link to WWTP infrastructure (treatment technology, capacity).
  - Consider integrating with hydrological layers (river network, catchment boundaries) and population data for impact assessment.
- Limitations and caveats:
  - Short temporal window (7 days) limits long-term trend analysis.
  - River site E not sampled; spatial completeness around estuary may be reduced.
  - Variations in sampling strategies and treatment technologies across sites may affect comparability.
  - Data quality depends on laboratory methods and QA steps described (DNA extraction efficiency, dPCR accuracy).

## References
- Castrignano, E.; A. M. Kannan; E. J. Feil; B. Kasprzyk-Hordern. 2018. Enantioselective fractionation of fluoroquinolones in the aqueous environment using chiral LC-MS/MS. Chemosphere 206:376-386.
- Castrignano, E.; A. M. Kannan; K. Proctor; et al. 2020. (Fluoro)quinolones and quinolone resistance genes in the aquatic environment: A river catchment perspective. Water Research 182.
- Petrie, B.; J. Youdan; R. Barden; B. Kasprzyk-Hordern. 2016. Multi-residue analysis of 90 emerging contaminants in liquid and solid environmental matrices by UHPLC-MS/MS. Journal of Chromatography A 1431:64-78.