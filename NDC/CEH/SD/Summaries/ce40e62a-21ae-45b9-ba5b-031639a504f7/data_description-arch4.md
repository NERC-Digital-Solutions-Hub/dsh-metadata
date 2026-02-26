# SARS-CoV-2 qPCR and water chemistry data from wastewater at six sites in England and Wales between March and July 2020, with associated Covid-19 positive test and related-death data collated from other sources

## Data access, licensing and citation
- Data accessible at: https://doi.org/10.5285/ce40e62a-21ae-45b9ba5b-031639a504f7
- Licence: Open Government Licence (OGL)
- Citation required: Hillary et al. (2021), NERC Environmental Information Data Centre dataset

## Data description
- Two CSV files provided:
  - data_table.csv: main dataset with wastewater SARS-CoV-2 concentrations and associated physicochemical and epidemiological data
  - cases.csv: clinical COVID-19 testing data aligned to the same time period and sites
- Sites and period:
  - Six wastewater treatment plants in Wales and Northwest England: Gwynedd, Cardiff, Liverpool, Manchester, Wirral, Wrexham
  - Population served ~3 million
  - Timeframe: March–July 2020
- Key variables in data_table.csv:
  - Week, Date, Site_Name
  - Flow (m3 per day, population equivalent)
  - SARS-CoV-2: gc per 100 mL for N1 and E gene assays
  - CrAssphage: gc per 100 mL, plus recovery percentage
  - Wastewater chemistry: NO3, NH4, PO4, pH, EC
  - Epidemiology: Deaths, Deaths_100k, Daily_Cases_100k, Rolling_Sum_100k
  - Population_Equivalent, Local_Authority_Population, Week
  - cov_class/cov_detect and E_class for assay detection status
- Key variables in cases.csv:
  - Site_Name, Date
  - Local_Authority_Population
  - Daily_Cases, Cumulative_Cases, Rolling_Sum, Daily_Cases_100k, Rolling_Sum_100k
  - Week

## Sampling sites and wastewater sampling
- Untreated influent and treated effluent collected weekly from six WWTPs in urban areas (Gwynedd, Cardiff, Liverpool, Manchester, Wirral, Wrexham)
- Sampling regime:
  - Weekly grab samples (08:00–09:00) on weekdays, except Wirral (24-hour composite)
  - Treated effluent sampled periodically at the same times as influent
- Sample handling:
  - Transport on the same day or next day on ice; stored at 4 °C; processed within 24 h
  - Aliquots frozen at -80 °C for downstream analyses

## Laboratory methods and data generation
- Wastewater processing:
  - Pasteurisation of samples prior to analyses (60 °C for 90 min)
  - Physicochemical analyses: NH4, NO3, PO4 via colorimetric methods; EC and pH measured with standard meters
- Nucleic acid extraction:
  - Concentration of nucleic acids from wastewater via centrifugal concentrators (50 kDa MWCO) and tangential-flow ultrafiltration for effluents
  - Spiking with murine norovirus (MNV) as extraction control
  - Extraction done with NucliSENS MiniMag system; samples stored at -80 °C prior to q(RT)-PCR
  - All steps performed in separate laboratories within safety cabinets
- q(RT)-PCR/qPCR assays:
  - SARS-CoV-2 targets: N1 (CDC) and E gene (Corman et al.)
  - MNV as extraction control; CrAssphage used as human faecal pollution marker
  - Assays run on QuantStudio 6 System; duplex (N1 + MNV or N1 + E) or triplex (N1 + E + MNV)
  - Reaction details, primers/probes, and cycling parameters provided in the document
  - All samples run in duplicates; mean of extraction replicates used
- Standards and quantification:
  - Serial dilutions with plasmid standards for SARS-CoV-2 targets; controls included
  - CrAssphage quantified with singleplex qPCR
  - Limits of detection (LoD) and limits of quantification (LoQ) previously established
    - LoD: N1 1.7 gc/µL, E 3.8 gc/µL, MNV 3.1 gc/µL
    - LoQ: N1 11.8 gc/µL, E 25.1 gc/µL, MNV 32.1 gc/µL

## Data structure and quality controls
- Data tables include:
  - Data_table.csv: main wastewater measurements and associated metadata
  - Cases.csv: clinical testing data aligned to wastewater sampling
- Quality controls:
  - MNV recovery used to monitor inhibition and extraction efficiency
  - Duplicate runs and negative controls included in each assay
  - Nucleic acid extractions and qPCR setups conducted in separate facilities to minimise contamination
- Data descriptors:
  - Clear column definitions for all measurements (e.g., cov_class, cov_detect, E_class)
  - Flow and population metrics linked to site and local authority areas

## Usage and citations
- Dataset intended for cross-analysis of wastewater SARS-CoV-2 signals with clinical case data and deaths
- Provides a framework for linking environmental surveillance with public health indicators across multiple sites and time
- Useful for evaluating data governance: data access, provenance, metadata richness, and cross-sector collaboration opportunities

## References (as cited in the dataset)
- CDC and Corman et al. primers/probes for SARS-CoV-2 detection
- Farkas et al. methods for SARS-CoV-2 concentration and qRT-PCR
- CrAssphage marker validation studies (Stachler et al.)
- Methodological sources for nitrate, nitrite, phosphate analyses and sample processing