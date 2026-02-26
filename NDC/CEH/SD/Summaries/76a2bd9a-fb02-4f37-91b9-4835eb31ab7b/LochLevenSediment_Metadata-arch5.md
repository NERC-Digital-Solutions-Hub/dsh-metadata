# LochLeven_SedimentDataset.csv

## Overview
- Supporting information for the dataset LochLeven_SedimentDataset.csv, collected during 2004–2005 to study phosphorus cycling between bed sediments and the overlying water column in Loch Leven, Scotland.
- Includes data on indicators of benthic algal biomass and various phosphorus fractions, used in numerous publications on sediment phosphorus mobilisation and the role of benthic microalgae.

## Data Scope and Content
- Location and period:
  - Loch Leven, a lowland, shallow freshwater eutrophic lake in the UK.
  - Monthly sampling from April 2004 to April 2005 across 6 fixed sites along a depth transect (2.0, 2.5, 3.5, 5.5, 10.0, 22.0 m).
- Sites:
  - Table 1 provides site identifiers, UK OS grid references, depth (m), and the number of values per site (Counts; e.g., 500 at the shallowest site, 405 at others).
- Determinands (variables measured):
  - Water quality: Dissolved Oxygen (%sat) at Surface, Bottom, Pore, Sediment; Conductivity (mS/cm) at various zones; pH; Temperature (°C).
  - Nutrients: Soluble Reactive Phosphorus (SRP, µg/L) and Total Phosphorus (TP) fractions; NH4-N; Silicate (SiO2) as SiO2 (mg/L).
  - Algal biomass: Chlorophyll a (µg/L; and related units/gdw in sediments).
  - Phosphorus fractionation in sediments: labile P, reductant-soluble P, reductant soluble plus total soluble P, metal-oxide bound P, apatite-bound P, residual P, organic P (derived from NaOH extraction and related calculations).
  - Additional P metrics include Total P (TP) and multiple sediment/gdw expressions (e.g., mg P/gdw in various fractions).
- Measurements and units:
  - Determinands with specific units and sampling context (Surface, Bottom, Pore, Sediment) as detailed in Table 2.
  - Chlorophyll a analyzed in water and sediment contexts; extraction and correction methods described.
- Data format:
  - Stored in a single ASCII CSV file with columns such as Site, Depth, Month, Date, DO (%sat), Cond (mS cm^-1), pH, Temp (°C), SRP (µg/L), TSP (µg/L), TP (µg/L), NH4 (µg/L), SiO2 (mg/L), Chl a (µg/L), SRP (µg/L), TSP (µg/L), NH4-N (µg/L), labile (mg P/gdw), red sol (mg P/gdw), red sol surp (mg P/gdw), Metal oxide (mg P/gdw), Organic (mg P/gdw), apatite bound (mg P/gdw), Residual (mg P/gdw), TP (mg P/gdw), Chl a (µg/gdw).
- References for methods:
  - Validated standard methods and literature (APHA 1992; Murphy & Riley 1962; Wetzel & Likens 2000; Golterman et al. 1978; Psenner et al. 1988; Farmer et al. 1994; Spears et al. 2006–2012).

## Sampling Regime and Methods
- Sampling regime:
  - Consistent monthly sampling from 6 sites along depth transect over 12 months.
  - Surface waters (and bottom waters from cores) sampled; sediment cores collected for laboratory processing.
- Field measurements:
  - In situ water temperature, DO (%sat), pH, and conductivity recorded per site/date.
  - One sediment core per site collected (approx. 30 cm overlying water, 20 cm sediment).
- Laboratory analyses:
  - Filtration of water samples; pigment analysis from filtered samples after storage.
  - SRP and TP: Murphy & Riley method; TP via digestion converting all forms to SRP.
  - NH4-N: Phenol-hypochlorite method (630 nm).
  - SRSiO2: 810 nm absorbance method.
  - Chlorophyll a: Spectrophotometric method with phaeopigment correction; acetone extraction.
  - Sediment-P fractionation: sequential extractions for labile P, reductant-soluble P, metal-oxide bound P, apatite-bound P, and residual P, with calculations for organic P and related fractions.
  - All extractions performed in dark at 20°C; analyses via centrifugation and filtration of supernatants.

## Data Governance and Quality Considerations
- Metadata and provenance:
  - Methods and site descriptions are documented, with extensive method references and links to prior publications.
  - Data have been used in multiple published works, indicating established utility and need for proper citation.
- Data management notes for stewardship:
  - Data are stored in a single CSV file with clearly defined column headers and units; ensure continued alignment of column definitions if schema evolves.
  - Given the multi-method, multi-fraction phosphorus data, maintain careful tracking of fraction classifications and any recalculations (e.g., organic P derived from NaOH-SRP vs NaOH-TSP).
  - Update procedures should reference the original sampling timeline (Apr 2004–Apr 2005) and maintain consistency with the Tables (1 and 2) and site descriptors.

## Usage, Access, and Citations
- Provenance and reliability:
  - Dataset underpinning studies on phosphorus mobilisation from Loch Leven sediments and the role of epipelon/benthic microalgae.
- Suggested citations:
  - Spears et al. and related works (2006–2012) as listed in the references; APHA (1992) standards; foundational methods by Murphy & Riley (1962) and Wetzel & Likens (2000).
- Data availability:
  - The document describes data storage format and methods; publication references imply accessible, reusable data for research and governance with appropriate attribution.