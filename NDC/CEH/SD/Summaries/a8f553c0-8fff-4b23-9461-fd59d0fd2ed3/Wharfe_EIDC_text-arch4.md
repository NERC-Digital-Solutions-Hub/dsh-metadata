# Faecal bacteria concentration in the River Wharfe from 2019 to 2021

## Overview
- Dataset of faecal bacteria concentrations in River Wharfe and selected tributaries from 2019 to 2021.
- Bacteria measured: total coliforms (TC), Escherichia coli (E. coli), and intestinal enterococci (IE).
- Concentrations expressed as colony forming units per 100 ml (cfu/100 ml).
- Sampling sites include recreational hotspots and locations near point sources such as sewage treatment works (STWs) and inflowing tributaries.
- Sites are listed in downstream order from the headwaters near Oughtershaw to the Wharfe–Ouse confluence at Cawood.

## Data structure and variables
- Column A: site name.
- Column B: site type (main river or tributary).
- Columns C–D: latitude and longitude (site coordinates).
- Column E: proxy site indicator (downstream site used when direct sampling was not at the recreational site).
- Columns F–J: sample bottle codes corresponding to different projects:
  - iWharfe2020 (sample code iW_20)
  - iWharfe_Upper (sample code iW_Upp)
  - iWharfe2021 (sample code iW_21)
  - Wharfe Addingham Environment Group (sample code AEG)
  - Wharfe Ashlands (sample code Ashlands)
- Additional markers for samples:
  - P = Primary, D = Duplicate
  - TS = Trample sample (sediment re-suspension)
- Measurements cover TC, E. coli, and IE concentrations (cfu/100 ml).

## Sampling, collection, and analysis
- Sampling period: irregular intervals from April 2019 to September 2021.
- Sampling locations targeted recreational hotspots and areas upstream/downstream of effluent discharges.
- Field collection methods varied by flow conditions; volunteers collected ~350 ml water in sterile bottles; higher flow methods included sampling from a rope or from river bank.
- Samples were kept in a cool pack and transported overnight to the ALS Ltd laboratory in Coventry.
- Analysis performed within 24 hours using standard dilution/incubation/counting methods; protocols available via ALS Ltd.

## Projects and provenance
- Data collected across multiple projects with overlapping sites:
  - iWharfe2020
  - iWharfe_Upper
  - iWharfe2021
  - Wharfe Addingham Environment Group
  - Wharfe Ashlands
- Project codes appear in the dataset (columns F–J) and reflect shared site usage and sampling campaigns.

## Purpose and impact
- Collected to raise local awareness of faecal bacteria pollution from treated/untreated discharges.
- Contributed to Ilkley Clean River Group’s successful Defra application in 2019 designating River Wharfe in Ilkley as an official Bathing Water site (first running water in the UK to achieve this).

## Data quality and governance considerations
- Irregular sampling schedule and use of proxy sites may affect comparability over time.
- Presence of duplicate samples (D) and primary samples (P) requires deduplication or explicit handling in analyses.
- Some samples involve unique events (e.g., trample samples TS) that may influence results.
- Data are drawn from multiple projects with potential differences in scope, timing, and site coverage; careful harmonization and metadata management are essential for cross-project analyses.
- Metadata details (site coordinates, sampling protocol, analysis methods) are included to support data discoverability and re-use.

## Authors and responsibility
- Rick Battarbee: project design, field sampling organization, sample transport to the laboratory, data interpretation.
- Malcolm Secrett: field sampling organization, data management, data interpretation assistance.