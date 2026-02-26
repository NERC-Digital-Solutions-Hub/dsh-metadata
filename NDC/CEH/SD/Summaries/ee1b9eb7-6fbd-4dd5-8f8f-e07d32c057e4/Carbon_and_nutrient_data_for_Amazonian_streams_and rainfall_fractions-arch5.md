# Sampling Regime

## Overview
- Data from Western Amazonian basin in Tambopata National Reserve, Madre de Dios, Peru, collected Feb 2011–May 2012.
- Targeted carbon fluxes in streams and rivers (DIC, δ13C-DIC, DOC, POC) and rainfall fractions (rain water, throughfall, stemflow, overland flow) to understand hydrological controls on carbon concentrations and fluxes.
- Datasets include two small streams (MT, NC) and two rivers (LT, TP) with varying upstream catchment sizes and seasonal activity.

## Datasets and Provenance
- DIC, δ13C-DIC, DOC, POC data for streams and rivers; prior submissions referenced (DOIs provided).
- Rainfall fractions data (DOC, POC, DIC, δ13C-DIC; Ca, Mg, K, Na, P, Si) for rainfall, throughfall, stemflow, and overland flow.
- Data resubmitted where earlier submissions incomplete (MT data limited in previous set; further campaigns added).

## Sampling Campaigns and Temporal Coverage
- Fluvial sampling campaigns across three periods: Feb–Apr 2011, Sept–Dec 2011, Mar–May 2012.
- Rainfall fractions collected Apr–May 2012.
- MT stream dries in the dry season, affecting sample collection during Sep–Nov 2011.

## Site Descriptions
- MT (Main Trail) and NC (New Colpita): small streams with documented widths and upstream drainage areas; MT dries seasonally.
- LT (La Torre) and TP (Tambopata): larger rivers with catchments extending toward the Andes foothills.

## Collection Methods and Instrumentation
- DIC: pre-acidified exetainers; headspace method on Thermo-Fisher Gas Bench/Delta V Plus for DIC concentration and δ13C-DIC.
- DOC: filtered samples, acidified to pH ~3.9, degassed, analyzed by TOC combustion.
- POC: determined by loss on ignition of filtered paper samples.
- Cations (Ca, Mg): Atomic Absorption Spectrometry (AAS) with N2O flame.
- Anions/ nutrients (K, Na): Flame photometry; TotP and Si by colorimetric methods.
- Rainfall fractions: throughfall collectors adjacent to litterfall plot; stemflow collected on eight labeled tree individuals; overland flow captured via bank-side collectors.

## Data Columns and Structure
- Two CSV files: Amazon streams C and nutrients, Amazon rainfall fractions C and nutrients.
- Streams/rivers file: 14 columns including Time (24h), Date, Type (stream/river), Site (MT, NC, LT, TP), CollectorID, DOC, POC, DIC, δ13C-DIC, Ca, Mg, K, Na, TotP, Si; some columns may be NA.
- Rainfall fractions file: 12 columns with similar structure for TF, SF, OF, and RW measurements.
- Data values: reported with units (mg/L for DIC/DOC/POC/Ca/Mg/K/Na; μg/L for P; Si in mg/L; δ13C in ‰).
- NA indicates not analysed or not available.

## Quality Control and Calibration
- DIC: drift correction standards every ~10 samples; replicate checks; randomised sample order.
- DOC: multi-point calibration with drift checks across the run; subset calibrations compared for consistency.
- Cations and Si/TotP: regular instrument checks with blanks and mid-range standards to ensure stability.
- Documentation of calibration ranges and standards used; references to standard methods and method validation.

## Metadata and Documentation
- Detailed procedure notes for field sampling, storage, and laboratory analyses.
- Tables and figures referenced for dataset context (catchment areas, sampling points, tree species/diameters for stemflow).
- References for methods: standard water analysis methods and specific isotope measurement literature.

## Data Use and Governance Considerations for Data Stewards
- Ensure metadata completeness: capture study location, sampling periods, site-specific details, and method descriptions for reproducibility.
- Maintain data provenance: link to prior submissions and DOIs; document dataset versioning and any data resubmissions.
- Standardize units and nomenclature across campaigns to ensure interoperability.
- Preserve measurement uncertainty information via QA/QC notes and calibration details.
- Support data discoverability through clear site IDs, sampling campaigns, and references to related datasets.
- Plan for updates/archiving: track changes across campaigns, note any missing data (NA) and rationale.
- Address interoperability challenges arising from multi-site, multi-year data and varied lab methods.

## References
- American Public Health Association (1999), Standard methods for the examination of water & wastewater.
- Waldron et al. (2014), on precision/accuracy of DIC δ13C measurements.