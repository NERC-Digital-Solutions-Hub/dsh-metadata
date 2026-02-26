# Intra- and Interpandemic Variations of Antiviral, Antibiotics and Decongestants in Wastewater Treatment Plants and Receiving Rivers

- Context and scope
  - Study sampling across 21 river locations in the River Thames catchment, England, plus two wastewater treatment plants (WWTPs) feeding the river.
  - Sampling period from 3 November 2009 to 11 May 2011, covering pandemic, late pandemic, and inter-pandemic periods.
  - Analytes include 11 antibiotics, 3 decongestants, and oseltamivir carboxylate (OC), the active metabolite of Tamiflu.
  - River samples were collected weekly during November 2009 with two additional time points (15 March 2010 and 11 May 2011); WWTP samples were collected hourly over a 24-hour period on 10–11 November 2009, plus an additional time point on 11 May 2011.

- Data files and formats ( GIS-ready elements)
  - RiverSamplingLocations.csv: 21 river sampling sites with Location ID, Location Name (River at Village/City), Eastings, Northings (grid coordinates).
  - River_PharmaConcentrations.csv: concentrations of all analytes at each river location, including Date, Location ID, Location Name, and analyte columns in ng/L.
  - WWTP_PharmaConcentrations.csv: concentrations for influent/effluent at two WWTPs (Benson and Oxford) with British Grid Reference, Location, Sample type (influent/effluent), Date, Time, and analyte concentrations in µg/L.
  - WWTPFlow.csv: flows at WWTP inflows, with Grid Reference, Location Name, Date, Time, Flow (m3/h).
  - RiverFlow.csv: river flows at the 21 river locations on sampling days, with Location ID, Location Name, Date, Flow (m3/s).
  - All datasets are in CSV format and can be opened in standard data analysis and GIS software.

- Analytes and measurements
  - Eleven antibiotics: trimethoprim, oxytetracycline, ciprofloxacin, azithromycin, cefotaxime, doxycycline, sulfamethoxazole, erythromycin, clarithromycin, ofloxacin, norfloxacin.
  - Three decongestants: naphazoline, oxymetazoline, xylometazoline.
  - Oseltamivir carboxylate (OC) as the antiviral metabolite.

- Methods and data provenance
  - Chemical analysis performed using on-line solid-phase extraction/liquid chromatography-tandem mass spectrometry (SPE/LC-MS/MS).
  - Method details and validation described in the authors’ publication and prior work (Khan et al., 2012).
  - Open-access publication reference: Intra- and Interpandemic Variations of Antiviral, Antibiotics and Decongestants in Wastewater Treatment Plants and Receiving Rivers (PLoS One, 2014, in press).
  - Data capture includes grab river samples (1 L) and time-proportional wastewater samples (750 mL over 24 h), preserved at -80°C until analysis.

- GIS-ready potential and usage
  - Spatial component: Location IDs with precise coordinates (Eastings/Northings and British Grid references) enable mapping of contaminant concentrations across the Thames catchment.
  - Temporal component: Weekly river data and hourly WWTP data allow both snapshot and time-series mapping of concentrations and flows.
  - Useful GIS workflows: join concentration data to RiverSamplingLocations and WWTP locations via Location ID; create chloropleth or point maps of analyte levels; visualize relationships between river/WWTP flows and contaminant concentrations; perform spatiotemporal analyses to assess distribution patterns during different pandemic phases.

- Practical considerations for GIS work
  - Ensure coordinate systems are harmonized (Eastings/Northings or Grid References) before mapping.
  - Link all concentration entries to corresponding locations and dates for time-enabled visualization.
  - Consider data resolution differences (weekly river data vs hourly WWTP data) when designing analyses or visualizations.

- References and data access
  - Primary data and methods described in Singer et al. (Supporting Information) with detailed data file descriptions.
  - Related methodological details available in Khan et al. (2012) and the cited PLoS One publication (2014).