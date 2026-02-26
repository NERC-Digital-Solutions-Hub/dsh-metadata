# Radiocarbon dating of charcoal pieces collected from soil in the Amazon Basin

- Scope: Radiocarbon dating data for macrocharcoal pieces (≥1 mm) collected from soil in Amazonia across Guyana, Peru, and Brazil; sites are terra-firme, non-seasonally flooded, and part of the RAINFOR network.
- Samples: 60 macrocharcoal pieces dated from field campaigns in 2015, 2017, 2018, and 2019.
- Funding and publications: Fieldwork supported by NERC (Grant NE/N011570/1) and CAPES Brazil. Dataset linked to published studies:
  - Feldpausch et al. 2022, Frontiers in Forests and Global Change
  - Goulart et al. 2017, Quaternary Geochronology
  - Methodological reference: Slota et al. 1987

## Dataset and data file

- Data file: c14.csv (CSV) containing radiocarbon dating data for macrocharcoal samples.
- File contents: 60 C-14 ages with associated metadata and provenance.

## Collection methods

- Sites and sampling design:
  - Three replicate pits per site, separated by 100 m.
  - Pits located just outside the boundary of 1 ha permanent forest plots.
  - For macrocharcoal, soil was excavated in 1 cm depth increments from the pit wall to 70 cm depth.
- Sample selection per pit:
  - Four pieces of charcoal were chosen per pit.
  - Criteria: (i) nearest-surface sample from each pit, (ii) three deeper samples from progressively deeper 5 cm depth increments.
  - Northern Peru site includes one additional date at 46 cm to balance sample size across pits.
- Handling and storage: Charcoal separated from soil, air-dried, stored in plastic containers.

## Laboratory analysis and processing

- Sample preparation:
  - Surface soil scraped from charcoal at Radiocarbon Facility (UFPE, Brazil).
  - Pre-treatment at NERC facility (UK) using standard acid-base-acid protocol: 0.5 M HCl at 80°C for 2 h, 0.5 M KOH at 80°C for 2 h, then 0.5 M HCl at 80°C for 2 h.
  - Combusted to CO2 in sealed quartz tubes, cryogenic purification, and conversion to graphite via Fe/Zn reduction (Slota et al., 1987).
- Dating:
  - 14C dated using Accelerator Mass Spectrometry (AMS) at NERC Radiocarbon Facility and at the Physics Institute of UFPE, Brazil.

## Data units, structure, and quality control

- Units: 14C age recorded as years before present (BP).
- Data structure: CSV with columns
  - Location, Plot, Latitude, Longitude, Soil_Pit, Depth, C-14_age_yr_BP, C-14_age_Uncertainty, Lab_ID
- Quality control:
  - Failed or non-converging runs were discarded and not included in the dataset.
- Missing data: Represented as 'NA' when field data were not recorded or are inaccessible.

## Data availability and provenance

- Provenance: Directly tied to field campaigns (2015–2019) and laboratory analyses (NERC UK and UFPE Brazil). Pre-treatment and AMS methods are described to support reproducibility.
- Related outputs: Data underpin publications listed above; additional methodological references provided for laboratory procedures.

## Governance and stewarding considerations

- Metadata and discoverability:
  - Ensure complete metadata for all records: precise location (Location, Plot, Latitude, Longitude), sampling context (Soil_Pit, Depth), measurement data (C-14_age_yr_BP, C-14_age_Uncertainty), and Lab_ID.
- Provenance and traceability:
  - Maintain linkage to field campaign dates, sampling strategy, and laboratory protocols (acid-base-acid pretreatment, AMS facilities).
- Data management:
  - Store as CSV with clear versioning; document any updates or corrections to ages or metadata.
- Access and reuse:
  - Dataset is associated with published work; provide licensing or access notes where possible to facilitate reuse.
- Cautions for users:
  - 14C ages are not calendar-calibrated in this dataset; depth-based sampling context should be considered when interpreting temporal signals.
  - QC decisions (discarded runs) should be acknowledged in any reuse, as only successful runs are included.