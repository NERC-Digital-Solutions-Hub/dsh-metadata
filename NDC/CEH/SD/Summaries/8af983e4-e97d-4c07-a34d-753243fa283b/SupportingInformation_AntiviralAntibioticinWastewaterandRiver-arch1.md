# Supporting Information

## Overview
- Dataset from the River Thames catchment in England, covering 21 river sampling sites and two wastewater treatment plants (WWTPs) feeding into the Thames.
- Sampling period: 3 November 2009 to 11 May 2011, spanning the peak of the second wave of influenza A(H1N1)pdm09 and subsequent periods.
- Analytes measured: 11 antibiotics, 3 nasal decongestants, and oseltamivir carboxylate (OC), the active metabolite of Tamiflu.
- Data formats include location metadata, river concentrations, WWTP influent/effluent concentrations, and flow data.

## Study design and sampling
- River sampling: weekly concentrations measured at 21 sites in ng/L during November 2009 (specific dates: 3rd, 11th, 16th, 24th); two additional river sampling dates on 15 March 2010 and 11 May 2011 representing late-pandemic and inter-pandemic periods.
- WWTP sampling: hourly measurements over a 24-hour period (10–11 November 2009) for influent and effluent; an additional WWTP sampling date on 11 May 2011.
- Sampling approach:
  - River water: grab samples (1 L glass bottles) stored at -80°C until analysis.
  - WWTP: time-proportional samples (750 mL) collected over 24 hours, stored at -80°C until analysis.

## Analytes
- Antibiotics: trimethoprim, oxytetracycline, ciprofloxacin, azithromycin, cefotaxime, doxycycline, sulfamethoxazole, erythromycin, clarithromycin, ofloxacin, norfloxacin.
- Decongestants: naphazoline, oxymetazoline, xylometazoline.
- Antiviral metabolite: oseltamivir carboxylate (OC).

## Analytical method
- Chemical analysis performed by Umeå University using on-line solid-phase extraction/liquid chromatography-tandem mass spectrometry (SPE/LC-MS/MS).
- Sample preparation: pre-filtered and acidified 1 mL samples.
- Method reference: Khan et al. (2012) describing the development and application of the on-line SPE/LC-MS/MS system.

## Data files and format
- RiverSamplingLocations.csv: location information for the 21 river sampling sites, including Location ID, Location Name, and Eastings/Northings coordinates.
- River_PharmaConcentrations.csv: river concentrations (ng/L) for all analytes at each river location. Columns include Location ID, Location Name, Date, and all analytes.
- WWTP_PharmaConcentrations.csv: WWTP concentrations (µg/L) for influent and effluent at Benson and Oxford WWTPs. Columns include grid reference, Location, Sample (influent/effluent), Date, Time, and all analytes.
- WWTPFlow.csv: influent flow data for WWTPs (m3/h) with Location ID, Location Name, Date, Time, Flow.
- RiverFlow.csv: river flow data for the 21 river sites on sampling dates (m3/s) with Location ID, Location Name, Date, Flow.
- All datasets are in CSV format and designed for compatibility with standard data analysis tools.

## Data access and metadata
- Data are accompanied by location codes and names aligned with the publication labels, enabling linkage across river and WWTP datasets.
- Geospatial references include Eastings/Northings and grid references for WWTPs, facilitating spatial analyses and mapping.
- The supporting information points to a related open-access publication for detailed methodology: Intra- and Interpandemic Variations of Antiviral, Antibiotics and Decongestants in Wastewater Treatment Plants and Receiving Rivers. PLoS One 2014 (in press at the time) with a referenced link to the publication.

## Context for analysis and interpretation
- Purpose: enable analyses of spatial and temporal patterns of pharmaceutical compounds from WWTP discharge to river systems, including comparisons between influent and effluent and variations over pandemic-related time periods.
- Potential analyses: correlations between WWTP flows and river concentrations, temporal trends across late-pandemic vs. inter-pandemic periods, spatial comparisons across the 21 river sites, and assessment of removal efficiencies in WWTPs (influent vs. effluent) for multiple analytes.
- Data quality considerations: multiple units (ng/L in rivers, µg/L in WWTPs), discrete time points (weekly river sampling with a few additional dates) and a dense 24-hour WWTP sampling event; data are structured to support cross-dataset analyses but require careful handling of units, timing, and potential missing values.