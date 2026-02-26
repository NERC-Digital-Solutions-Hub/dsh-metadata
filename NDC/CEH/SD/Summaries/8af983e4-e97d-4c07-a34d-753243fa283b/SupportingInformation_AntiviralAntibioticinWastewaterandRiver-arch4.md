# Supporting Information

## Overview
- Describes a study of 21 river locations in the River Thames catchment, England, and two wastewater treatment plants (WWTPs) sampled from November 2009 to May 2011.
- Measured 11 antibiotics, 3 decongestants, and oseltamivir carboxylate (Tamiflu metabolite).
- Data include river concentrations (weekly), WWTP influent/effluent (hourly over 24 hours), and flows for both rivers and WWTPs.

## Data assets and structure
- RiverSamplingLocations.csv: location information for all 21 river sampling sites, including Location ID, Location Name, Eastings, Northings, and coordinates; used as the primary key for site identification.
- River_PharmaConcentrations.csv: river concentrations by Location ID, Location Name, Date, and all analytes (trimethoprim, oxytetracycline, ciprofloxacin, azithromycin, cefotaxime, doxycycline, sulfamethoxazole, erythromycin, clarithromycin, ofloxacin, norfloxacin, naphazoline, oxymetazoline, xylometazoline, oseltamivir carboxylate) in ng/L.
- WWTP_PharmaConcentrations.csv: WWTP concentrations (influent/effluent) for the same analytes, with fields including British Grid Reference, Location, Sample type (influent/effluent), Date, Time, and concentrations in µg/L.
- WWTPFlow.csv: influent flows at WWTPs on sampling days, including Grid Reference, Location Name, Date, Time, Flow (m3/h).
- RiverFlow.csv: river flows at 21 locations on sampling days, including Location ID, Location Name, Date, Flow (m3/s).
- All datasets are CSVs and are designed for compatibility with standard data analysis tools.

## Temporal and sampling design
- River samples (grab, 1 L) collected weekly during November 2009 on selected dates, plus two additional points: 15 March 2010 (late pandemic) and 11 May 2011 (inter-pandemic).
- WWTP samples (time-proportional, 24-hour) collected on 10–11 November 2009, with an additional point on 11 May 2011.
- Data units: river concentrations in ng/L; WWTP concentrations in µg/L; flows in m3/h (WWTP) and m3/s (river).

## Analytical methods and data provenance
- Analytes quantified using on-line SPE/LC-MS/MS after pre-filtering and acidification of samples.
- Method referenced from a detailed open-access publication by Khan et al. (2012) and the data paper describing intra- and interpandemic variations.
- Full methodological details available in the linked open-access paper (PLOS One 2014; in press at the time) and NORA record placeholder for the data repository.

## Geospatial and metadata details
- River locations include Eastings/Northings coordinates, with RiverSamplingLocations.csv providing the mapping between Location ID and descriptive names.
- WWTP data use British National Grid references for grid positioning.
- Data columns consistently label Location ID, Location Name, Date, and analyte concentrations to support cross-dataset joins and reproducibility.

## Data quality, standards, and discoverability
- Data are provided in standardized CSV format for broad accessibility and interoperability.
- Clear naming conventions for locations (Location ID) and links between river sites and WWTPs enable consistent data integration.
- Metadata encompasses sampling type, date/time, location identifiers, and units to support quality checks and proper interpretation.

## Access, reuse, and governance
- All datasets are machine-readable CSV files; suitable for integration into data platforms and analytical workflows.
- Data and methods are tied to a published, open-access study, enhancing transparency and reuse potential.
- The publication and data description indicate a collaborative, multi-site effort across institutions, with emphasis on cross-site comparability and long-term monitoring.

## Implications for data leadership and strategy
- Demonstrates the value of a structured, multi-layer data asset: site metadata, river concentrations, WWTP concentrations, and flow data, all harmonized by Location ID.
- Highlights importance of consistent identifiers, coordinate systems, and units to enable cross-site synthesis and policy-relevant analysis.
- Illustrates effective data openness: sharing raw CSV datasets and linking to detailed methodological documentation to support reuse, replication, and networked data initiatives.
- Reveals potential data governance considerations: maintaining alignment between river and WWTP datasets, handling different sampling frequencies, and documenting provenance for temporal comparisons (pandemic-related phases).