# Supporting Information

- Overview of the dataset
  - Context: 21 river sampling locations in the River Thames catchment, England, sampled during and after the peak of the second wave of the influenza A(H1N1)pdm09 pandemic for 15 pharmaceuticals; two wastewater treatment plants (WWTPs) feeding the river also sampled.
  - Timeframe: 3 November 2009 to 11 May 2011.
  - Analytes: 11 antibiotics (trimethoprim, oxytetracycline, ciprofloxacin, azithromycin, cefotaxime, doxycycline, sulfamethoxazole, erythromycin, clarithromycin, ofloxacin, norfloxacin), 3 decongestants (naphazoline, oxymetazoline, xylometazoline), and oseltamivir carboxylate (OC).
  - Sampling cadence: river samples weekly during November 2009 with late-pandemic and inter-pandemic points; WWTPs sampled hourly over 24 hours on 10–11 November 2009 plus additional point on 11 May 2011.
  - Analytical method: on-line SPE/LC-MS/MS. Laboratory: Umeå University (June 2010–June 2011). Method described in Khan et al. 2012; expanded context in Singer et al. 2014.

- Data files and formats (CSV)
  - RiverSamplingLocations.csv
    - Contains 21 river sampling sites with Location ID, Location Name, Eastings, Northings, and other location metadata.
  - River_PharmaConcentrations.csv
    - Contains concentrations (ng/L) of all analytes at each river location; columns include Location ID, Location Name, Date, and each analyte.
  - WWTP_PharmaConcentrations.csv
    - Contains concentrations (ng/L) at WWTP influent and effluent; includes Grid Reference, Location, Sample (influent/effluent), Date, Time, and analyte concentrations (units: µg/L for this file).
  - WWTPFlow.csv
    - Contains influent flow data (m3/h) with Grid Reference, Location, Date, Time, and Flow.
  - RiverFlow.csv
    - Contains river flow data (m3/s) for the 21 river locations with Location ID, Location Name, Date, and Flow.
  - All datasets are CSV and accessible with standard data analysis software.

- Metadata and data model
  - Key identifiers: Location ID and Location Name across river locations; RiverSamplingLocations provides Eastings/Northings (geospatial context).
  - Temporal coverage: Date fields in all concentration and flow datasets; dedicated Time fields for WWTP samples.
  - Units: River concentrations in ng/L; WWTP concentrations in µg/L; flows in m3/h (WWTP) and m3/s (river).
  - Location naming convention aligns with publication terminology (River at Village/City).

- Data provenance and access
  - Source and method details published in:
    - Singer et al. Intra- and Interpandemic Variations of Antiviral, Antibiotics and Decongestants in Wastewater Treatment Plants and Receiving Rivers. PLoS One 2014 (open access; in-press at the time of this document).
    - Analytical methodology described in Khan et al. 2012.
  - Data availability: Included as Supporting Information with the accompanying article; linked via open access resources (e.g., nora.nerc.ac.uk).

- Data quality, governance, and stewardship
  - Quality assurance/transformations: Raw data were collected using standardized laboratories and methods; subsequent QA, cleaning, and transformation undertaken prior to sharing (as described by the associated publications).
  - Metadata completeness: Location metadata, coordinates, sampling dates/times, and analyte names are included to support discoverability and reuse.
  - Data interoperability: Multiple datasets use consistent location identifiers and date formats to facilitate joining and comparisons across river and WWTP contexts.
  - Accessibility and reuse: All datasets are CSV and designed for broad re-use in downstream analyses and governance workflows.

- Practical considerations for Data Stewards
  - Data discovery and discovery metadata: Ensure Location IDs, Names, and coordinates are preserved for discoverability and geo-context.
  - Data integrity and lineage: Maintain reference to the original publications for method details and QA procedures; capture provenance of each data file (sampling dates, lab responsible, method version).
  - Update and governance: Although limited to the 2009–2011 window, document any future updates, embargo considerations, or revisions clearly; be explicit about units and any changes in data aggregation levels.
  - Limitations and caveats: Data reflect specific temporal windows (pandemic periods) and specific sites; cross-dataset joins should account for differing sampling frequencies (weekly river vs. hourly WWTP) and unit conventions.

- References
  - Main publication: Intra- and Interpandemic Variations of Antiviral, Antibiotics and Decongestants in Wastewater Treatment Plants and Receiving Rivers. PLoS One 2014.
  - Method reference: Khan G.A. et al. 2012 (on-line SPE/LC-MS/MS method).