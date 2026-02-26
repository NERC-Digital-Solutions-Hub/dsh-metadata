# Materials and methods, and metadata for Phosphorus, carbon and nitrogen concentrations in UK soil mineral fractions, 2013-2014. Data taken from 'An investigation of the distribution of phosphorus between free and mineral associated soil organic matter, using density fractionation', Adams et al 2018, Plant & Soil

## Overview
- Describes the laboratory methods, data components, and metadata for concentrations of carbon, nitrogen, and phosphorus in UK soil mineral fractions from 2013–2014.
- Data derive from density fractionation separating light and heavy organic matter fractions and subsequent analyses of organic and inorganic phosphorus, organic carbon (OC) and total nitrogen (TN) across bulk, light fraction (LF), and heavy fraction (HF).
- Provides procedural details, unit conventions, and table-specific column definitions to support data integration and GIS-based mapping.

## Data types and measurements
- Analytes:
  - Carbon: Organic Carbon (OC) in bulk, LF, HF
  - Nitrogen: Total Nitrogen (TN) in bulk, LF, HF
  - Phosphorus: Total Phosphorus (TP), Inorganic P (IP), Organic P (OP) in bulk, LF, HF
- Fractions:
  - Bulk (total soil), Light Fraction (LF), Heavy Fraction (HF)
  - Organic Carbon and Nitrogen content and recoveries for OC and TN
  - TP, IP, OP concentrations and their recoveries for TP, IP, OP
- Sample identifiers and metadata:
  - Sample ID encodes vegetation type, sample number, and depth indicator (s = shallow, d = deep)
  - Catchment name, land use (e.g., IG = improved grassland), database ID, and depth
  - Spatial context: latitude, longitude, mean annual precipitation (MAP), mean annual temperature (MAT)
  - Climate and site descriptors: MAP, MAT, and other location-based fields
- Units:
  - C and N fractions: percentages (%)
  - TP, IP, OP: mg g-1
  - OC & TN recoveries: percentages (%)
  - Mass measurements and recoveries recorded in mg or g as appropriate

## Methodology workflow
- Density fractionation:
  - Subsamples: 25 g of sieved soil in 400 mL bottles with 250 mL NaPT solution (density 1.6 g cm-3)
  - Centrifugation at 5500 rpm for 30 min
  - Very light fraction (NLF) removal and processing into 60 μm nylon mesh bags
  - Re-suspension and repeated separation until all NLF accounted; rinsed to remove NaPT
  - Conductivity checks to ensure NaPT removal (<50 μs cm-1; <200 μs cm-1 accepted for calcareous soils)
  - Drying at 40 °C and storage
- Organic Light Fraction (OLF) extraction:
  - Sonication to disrupt aggregates; microscopic verification of complete disruption
  - Centrifugation and transfer of OLF to LF, repeated centrifugation as needed
  - Combine OLF with NLF in LF bags; rinse until conductivity thresholds achieved
  - Dry and grind LF+OLF to fine powder
- Heavy Fraction (HF) handling:
  - Remaining material washed and centrifuged until conductivity thresholds met
  - Dried, weighed, and ground to a fine powder
- Pre-analysis treatments:
  - If inorganic carbonate suspected (bulk soil pH > 5.5), acid treatment with 0.1 M HCl and CO2 release monitored microscopically
  - Re-drying prior to analyses
- Analytical measurements:
  - Total Organic Carbon (TOC) and Total Nitrogen (TN): Vario EL elemental analyzer
  - Total Phosphorus (TP): Ignition-extraction method (Olsen & Sommers 1982)
  - Inorganic P (IP): Extraction with 0.5 M sulfuric acid, followed by molybdate analysis
  - Organic P (OP): Calculated as TP − IP
  - Replication: All analyses replicated four-fold
- Bulk analyses (context):
  - Bulk C and N and IP follow the same methods as above
  - Different TP method previously used by Toberman et al. (aqua regia with microwave digestion)

## Tables and metadata structure
- Table S1 – Information about the soil samples:
  - Sample ID structure, catchment, land use, database ID, depth, latitude/longitude, MAP, MAT, and related descriptive fields
  - Includes explicit column header explanations for multiple fields (e.g., sample labeling, depth notation, catchment/land-use codes)
- Table S2 – Recovery of soil mass in density fractionation:
  - Collection date, lat/long, mean annual precip, MAT, map/latitude/longitude fields, masses for starting, light, heavy fractions, and related fractional recovery metrics
- Table S3 – OC & TN concentration data:
  - OC and TN for bulk, LF, HF with corresponding units and notes
- Table S4 – TP, IP & OP concentration data:
  - Bulk, LF, HF TP, IP, OP with units and notes
- Table S5 – Recoveries of OC & TN:
  - OC/TN bulk, LF+HF, and recoveries (%)
- Table S6 – Recoveries of TP, IP & OP:
  - TP, IP, OP bulk and LF+HF masses and their recoveries (%)
- Column heading explanations are provided for all tables, detailing the meaning of each field, units, and interpretation

## Quality assurance and data handling
- Use of conductivity thresholds to confirm complete removal of NaPT and to validate rinsing
- Microscope-based verification of complete OLF disruption
- Repetition of extraction steps to maximize recovery of LF material
- Carbonate removal checks via acid treatment when necessary
- Four-fold replication for analytical measurements to ensure robustness
- Clear encoding of Sample IDs to enable consistent data joins and GIS integration

## Spatial and temporal scope
- Temporal: Data collected and processed during 2013–2014
- Spatial: UK soils with geolocated sample metadata; includes catchment-level and site-level descriptors plus coordinates

## GIS relevance and integration
- Rich metadata enables spatial joins to soil maps and environmental layers (catchment, land use, coordinates, MAP, MAT)
- Fraction- and fraction-referenced C, N, and P data across bulk, LF, HF can be mapped to study mineral-associated organic matter distributions
- Consistent units and clearly defined table structures facilitate data ingestion into GIS workflows and data portals
- Sample ID encoding provides a scalable approach to link soil chemistry with vegetation, depth, and site characteristics

## References
- Adams et al. 2018, Plant & Soil (source for methodology)
- Cerli et al. 2012; Olsen & Sommers 1982; Schrumpf et al. 2013; Toberman et al. 2016 (methods and context for fractionation, measurements, and prior data)
- Toberman et al. 2016 (bulk soil methods for comparative analyses)