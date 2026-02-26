# Concentration Levels of Resistance Genes in Wastewater and Receiving Environment Brief description of the dataset

- The dataset records weekly concentrations of the qnrS resistance gene in wastewater and receiving water in South West UK.
- Timeframe: seven consecutive days between June and October 2015.
- Location and scope: five major wastewater treatment plants (WWTPs) contributing to a single river catchment, covering ~2,000 km2 and a population of ~1.5 million (over 75% of catchment population).

## Study area and sampling points

- WWTPs employ different treatment technologies (activated sludge and trickling filters); most use conventional sedimentation after secondary treatment, except sequencing batch reactors (SBRs) with in-situ settling.
- Matrices sampled: influent wastewater (24 h composites) and effluent (time-proportional composites), plus river water sampled upstream and downstream of effluent discharge points at varying distances; river sampling not conducted for Site E (direct discharge to estuary).
- Sampling details:
  - Influent: volume-proportional composites with ~15-minute subsamples.
  - Effluent: time-proportional sampling due to limited variation.
  - River water: 8 L grab samples.
- Sample handling: all samples transported to the lab on ice for processing.
- Site coverage: data collected across five WWTPs within the catchment.

## DNA extraction and quantification

- DNA extraction from 1 mL unfiltered wastewater using a Roche High Pure PCR Template Preparation Kit with a defined lysis and binding workflow (lysozyme, proteinase K, binding/washing steps).
- Extraction quality control: DNA quantified with a Thermo Fisher Nanodrop to verify successful extraction.
- qnrS quantification: performed by digital PCR (dPCR) using a QuantStudio 3D system with a 20× qnrS TaqMan assay.
  - Reaction setup included Master Mix V2, qnrS assay, nuclease-free water, and DNA template.
  - Platforms: high-density nanofluidic chips loaded into the QuantStudio 3D system.
  - PCR cycling: initial 95°C for 10 min; cycles between 60°C and 98°C for 40 cycles; final hold at 60°C, then cooling.
- Data processing: AnalysisSuite software used to derive gene copy quantifications and perform statistical analysis.

## Format of the dataset

- Reported concentrations: qnrS gene copies per microliter (copies/μL) for influent and effluent wastewater across all sites during the monitoring week.

## Data quality, provenance, and references

- Provenance: detailed methodology for field sampling, DNA extraction, and dPCR analysis provided to support reproducibility.
- Storage: extracted DNA stored at -20°C.
- Metadata and supporting information: study area description, sampling points, treatment technologies, and specific laboratory procedures are documented.
- References for methodology and context:
  - Castrignano et al. 2018
  - Castrignano et al. 2020
  - Petrie et al. 2016