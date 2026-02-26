# Pollinator effectiveness in oilseed rape ( Brassica napus L.) in relation to behavioural and morphological characteristics

- Overview
  - A dataset from the Wessex BESS project aims to quantify the number of pollen grains delivered in a single visit by various pollinators to oilseed rape (Brassica napus L.) and to relate pollen delivery to behavioural and morphological traits.
  - Dataset can be used alongside other Wessex BESS data, especially the landscape-scale pollinator survey.

- Data Collection and Scope
  - Field site: Wiltshire, UK (central point 51.185988° N, -1.832657° W).
  - Timeframe: April–June, across three field seasons (2014–2016).
  - Sites: 15 fields of winter sown oilseed rape.
  - Experimental design: flowers observed and exposed to pollinators using two methods (bouquet method for bees; plastic box method for non-bees). Each visit recorded for duration and type of interaction (probing, crawling, short contact).
  - Control: flowers prepared but unvisited to assess baseline pollen deposition.

- Datasets and Structure
  - Two linked data files:
    - NERCPollinatorEfficiency: captures pollinator visits, visit type, duration, method, and deposition metrics.
    - NERCPollenSwab: captures pollen loads on pollinator bodies (head, thorax, and other body parts) via swabs.
  - Linkage: both files link via PollinatorID, enabling integrated analysis of pollinator behavior, pollen loads, and pollen deposition on stigmas.

- Key Variables and Measurements
  - Pollen deposition on stigmas (PolPerVis) after a single visit.
  - Pollen loads on pollinators from swabs (Back, Feet, Head, Under) with counts of pollen grains.
  - Morphological traits:
    - Body_Length (mm)
    - Intertegular_distance (ITD) for most species; proxy ITD for some beetles
    - Hair density on the thorax (percentage, 5% increments)
    - Hair_type (Branched, Smooth, No_hair)
  - Visit metrics:
    - VisitType (P = probed, C = crawled, S = short)
    - LengthVisit (seconds; 0.5 s for short visits)
  - Experimental method and taxonomy:
    - MethodUsed (B = bouquet, PB = plastic box)
    - PollinatorID, SpeciesCode, Description
    - Family, FunctionalGroup (size/behavior), FunctionalGroupPollSwab
  - Data quality and provenance:
    - Date of collection (dd/mm/yyyy)
    - Source fields stored in MS Access; notes on data processing and QA processes
  - Data quality observations:
    - Missing PollinatorID for one record; some columns have NA (e.g., Feet in NERCPollenSwab) due to measurement limitations on small beetles.
    - Control stigma pollen counts reported (median 11; range 0–99, n=31) to contextualize pollinator-derived pollen.

- Data Quality Assurance and Documentation
  - Adherence to set field and lab protocols; data entry performed in MS Access with anomaly checks.
  - Training provided for protocol adherence.
  - Documentation includes detailed field methods, variable definitions, unit conventions, and missing data notes to aid interoperability and reuse.

- Usage, Reuse, and Linkages
  - Data are designed for integration with the broader Wessex BESS pollinator datasets, enabling landscape-scale analyses.
  - Cross-references available to connect NERCPollinatorEfficiency with NERCPollenSwab via PollinatorID, and to FunctionalGroupPollSwab for dataset linkage.
  - Clear metadata conventions accompany the files (e.g., units, categorical vs. continuous, and description of each variable) to support data discovery and reuse.

- Data Governance Considerations
  - Provides metadata-rich description of data collection, processing, and measurement methodologies to support data stewardship, reproducibility, and future reuse.
  - Acknowledges data limitations and incomplete data at the level of individual identifiers, enabling informed handling in downstream governance and analysis.
  - Emphasizes potential interoperability considerations due to differing collection methods (bouquet vs. plastic box) and species-specific measurement constraints.