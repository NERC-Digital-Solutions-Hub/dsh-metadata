# Dataset Originator ECN Data Centre (http://data.ecn.ac.uk - ecn@ceh.ac.uk), Centre for Ecology and Hydrology

- Overview
  - Phenology-based methodology recording the spawning of the Common Frog in selected pools and ditches; uses the number of egg masses as an indicator of frog population health.
  - Includes laboratory analyses of water samples from observed pools.
  - Data are accompanied by quality information to assess data reliability.

- Data provenance and ownership
  - Dataset Originator: ECN Data Centre, CEH.
  - Dataset Owners: UK Environmental Change Network (ECN) programme, funded by a consortium of UK government departments and agencies (e.g., AFBI, BBSRC, NRW, DSTL, DEFRA, EA, Forestry Commission, Welsh Government, Natural England, NERC, NIEA, SEPA, Scottish Government, SNH).
  - Usage and attribution: ECN asks users to acknowledge the data usage and to send one reprint of any publication citing the dataset.

- Data structure and access
  - Data collection procedures: ECN has standard operating procedures to ensure comparability across sites; detailed collection methods are described in accompanying BF.pdf.
  - Data download format: SITECODE (site ID), LCODE (location code within site), FROMDATE (start date), SDATE (sampling date), FIELDNAME (variable measured), VALUE (measured value).
  - Supporting documentation: ECN_BF_qtext.csv provides text explanations for quality issues not captured by standard quality codes.

- Site codes and locations
  - Explanatory site codes and names (example sites): T01 Drayton; T02 Glensaugh; T03 Hillsborough; T04 Moor House - Upper Teesdale; T05 North Wyke; T06 Rothamsted; T08 Wytham; T09 Alice Holt; T10 Porton Down; T11 Y Wyddfa - Snowdon.
  - Coordinates provided for each site location.

- Variables and units
  - Field names cover a wide range of water chemistry and environmental measurements (examples): 
    - Alkalinity (ALKY, mg/L), Aluminium (ALUMINIUM, mg/L), Calcium (CALCIUM, mg/L), Chloride (CHLORIDE, mg/L), Conductivity (CONDY, µS/cm), Colour (COLOUR, nM), Dissolved Organic Carbon (DOC, mg/L), various nutrient metrics (NH4N, NO3N, TOTALN, TOTALP), pH and multiple pH readings, and other parameters (e.g., PHAQCS, PHAQCU, SPAWNDATE, NEWMASS, DEPTH, SURFAREA, etc.).
  - Temporal and biological data include dates of spawning observations (SPAWNDATE), first congregating frogs (CONGDATE), hatching (HATCHDATE), and emergence/leaving dates (LEAVEDATE), plus counts such as NEWMASS and PERCDEAD.

- Quality control and documentation
  - Quality codes (Q1–Q8) and general quality codes (e.g., 100–513, 999) indicate data quality and context; codes are included in the data download.
  - Unusual events and contextual notes are captured in ECN_BF_qtext.csv (with code 999 indicating an unusual event; viewable in the quality text documentation).
  - Data quality considerations may require domain expert interpretation, especially when data come from multi-source collections or non-standard sampling.

- Practical considerations for analysts
  - Data may be incomplete at local scales or for certain sites; heterogeneity in data collection and quality codes requires careful harmonisation.
  - Access often involves navigating multiple data components (site metadata, field variables, quality codes, and textual quality notes); proper metadata enhances usability and reproducibility.
  - When using the data to identify correlations and build models, rely on the accompanying quality metadata to filter or weight observations appropriately; acknowledge data sources and include quality context in analyses and reporting.