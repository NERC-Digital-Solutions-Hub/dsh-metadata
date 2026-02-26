# Supporting Information

## Context and scope
- 21 river locations within the River Thames catchment in England were sampled, along with two wastewater treatment plants (WWTPs) feeding into the river.
- Sampling occurred during and after the peak of the second wave of the influenza A(H1N1)pdm09 pandemic (Nov 3, 2009 – May 11, 2011).
- Analytes measured: 11 antibiotics, 3 decongestants, and oseltamivir’s active metabolite (oseltamivir carboxylate, OC) – total of 15 pharmaceuticals.

## Analytes
- Antibiotics: trimethoprim, oxytetracycline, ciprofloxacin, azithromycin, cefotaxime, doxycycline, sulfamethoxazole, erythromycin, clarithromycin, ofloxacin, norfloxacin.
- Decongestants: naphazoline, oxymetazoline, xylometazoline.
- Antiviral metabolite: oseltamivir carboxylate (OC).

## Sampling and storage
- River samples: weekly grab samples (1 L glass bottles) with storage at -80°C until analysis.
- WWTP samples: 24-hour time-proportional samples (750 mL) for influent and effluent, stored at -80°C until analysis.
- Additional sampling time points: river (15 March 2010; 11 May 2011) to reflect late pandemic and inter-pandemic periods.

## Chemical analysis
- Analytes quantified by LC-MS/MS with online solid-phase extraction (SPE/LC-MS/MS) on pre-filtered and acidified 1 mL samples.
- Method validated and described in Khan et al. (2012); detailed implementation reported in Singer et al. (Intra- and Interpandemic Variations, PLoS One 2014, in press).

## Data files and formats
- RiverSamplingLocations.csv: location information for the 21 river sampling sites (Location ID, Location Name, Eastings, Northings).
- River_PharmaConcentrations.csv: concentrations (ng/L) of all analytes at each river location; columns include Location ID, Location Name, Date, and each analyte (ng/L).
- WWTP_PharmaConcentrations.csv: concentrations (µg/L) of all analytes in influent and effluent for two WWTPs (Benson and Oxford); columns include Grid Reference, Location, Sample (influent/effluent), Date, Time (h), and each analyte (µg/L).
- WWTPFlow.csv: influent WWTP flow data (Location ID, Location Name, Date, Time, Flow in m3/h).
- RiverFlow.csv: river flow data at 21 river sampling points on sampling days (Location ID, Location Name, Date, Flow in m3/s).
- All datasets are provided in CSV format and can be opened with standard data analysis tools.

## Data accessibility and references
- The datasets are designed for integration with environmental monitoring workflows, enabling quality assurance, standardised analysis, and outputs suitable for reports, maps, and charts.
- Methods and broader context described in Singer et al. (Intra- and Interpandemic Variations of Antiviral, Antibiotics and Decongestants in Wastewater Treatment Plants and Receiving Rivers), PLoS One 2014 (open access). Additional methodological details available via the referenced publication and associated open-access resources (URL provided in the dataset description).