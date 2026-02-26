# Glastir Monitoring and Evaluation Programme (GMEP)

## Overview and Aims
- Wales-wide monitoring programme to evaluate the Glastir agri-environment scheme (AES) and its effects on the environment.
- Focus on soil health as part of outcomes related to climate, biodiversity, soil and water quality, and woodland expansion; also aims to quantify general soil quality trends.
- Seeks to identify drivers of change (land use, climate, pollution) beyond Glastir interventions through synthesis and analysis of collected data.

## Monitoring Design and Scale
- 4-year rolling survey cycle (2013–2016) to maximise spatial coverage and detect temporal trends cost-effectively.
- Two main components:
  - Wider Wales Component: baseline estimation and national trends/reporting.
  - Targeted Component: links specifically to Glastir priority areas.
- Integration across metrics using a common spatial unit of 1 km².
- Sampling framework mirrors the Countryside Survey of Great Britain to enable future data integration.
- Total of 300 1 km² squares sampled over the cycle; half randomly selected within Land Classification strata (to maximize environmental heterogeneity between strata), half targeted at Glastir priority areas.
- Exclusions: squares with >75% urban land or >90% sea excluded; confidentiality maintained by plotting at 10 km resolution.

## Field Sampling and Laboratory Methods
- In each 1 km² square, soil samples are taken from 5 randomly dispersed locations.
- Soil cores analysed for soil fauna using a white plastic core (F-core); cores transported to CEH Lancaster for extraction.
- Dry extraction using six 12-bank Tullgren funnels, typically 5 days, with 70% ethanol as preservative.
- Data collected per sample include identifiers (SQXN), depth, start/stop times, etc.
- Primary focus on soil mesofauna extraction and subsequent identification.

## Invertebrate Identification and Data Management
- Identification protocol groups soil mesofauna into broad taxa (e.g., Acari groups, Collembola groups, Enchytraeids, etc.), with counts tallied per broad group.
- Specimens of broad groups sorted into labeled blocks and tallied; 1 in 20 samples cross-checked for QA.
- Data entered into Excel templates and integrated into a central CEH Bangor database.
- Training emphasized: staff familiarisation with broad-group identification before routine processing; voucher-based learning and mock samples.

## Training, Health & Safety, and Quality Assurance
- Training: at least one week for species-group recognition and counting procedures.
- Health & Safety: ethanol handling and storage; risk assessment requirements.
- Quality Assurance: adherence to the DEFRA Joint Code of Practice for Research (JCoPR); mandatory cross-checks (1 in 20 samples) for the early samples to ensure comparability between staff identifications; ongoing QA sampling reduced as processes stabilize.

## Data Products and Accessibility
- Data files include GMEP_TOPSOIL_MESOFAUNA_2013_14.csv, containing counts of soil fauna from 147 1 km² sites across Wales.
- CSV dataset fields cover year, survey square (SQ_ID), plot type, easting/northing, Land Classification (LC), core taken status, and counts for various mite and collembolan groups, plus totals (e.g., TOTAL_MITES, TOTAL_COLL, TOTAL_INVERT).
- Describes how totals are calculated (e.g., TOTAL_MITES = sum of Oribatid box/other and mesostigmatid; TOTAL_COLL = sum of Poduromorpha, Entomobryomorpha, Symphypleona/Neelipleona).

## Roles, Responsibilities and Field Teams
- Appendix lists roles including topic leaders (soil meso-fauna), data management, sample management, field coordination, and project management.
- Field survey teams composed of a large group of named staff and associates responsible for data collection and sampling across Wales.

## Key Points for Monitoring Framework Authors
- Uses a multi-metric, ecosystem-approach design that integrates data across spatial and temporal scales in a single field visit where possible.
- Employs a rolling 4-year cycle with a balanced approach between baseline/national trend estimation and targeted scheme-linked sampling.
- Aligns with an established national framework (Countryside Survey GB) to enable future integration and comparability.
- Emphasizes data quality, transparency, and governance, including metadata management, data sharing considerations, and adherence to the JCoPR.
- Structures data collection and QA processes to ensure reproducibility and reliability of faunal counts, with explicit training and cross-checks to maintain consistency across personnel.
- Provides a concrete data product (GMEP_TOPSOIL_MESOFAUNA_2013_14.csv) with explicit schema and derived totals to support analyses of soil biodiversity and ecosystem health.