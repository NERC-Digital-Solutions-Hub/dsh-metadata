# Supporting Information

## Overview
- Describes a dataset from sampling 21 river locations within the River Thames catchment (England) and two WWTPs feeding the river.
- Timeframe: November 3, 2009 to May 11, 2011 (peak and post-peak of the second H1N1 pandemic).
- Analyte set includes antibiotics, decongestants, and oseltamivir carboxylate (OC).

## Context and Analytes
- Analytes quantified:
  - Antibiotics: trimethoprim, oxytetracycline, ciprofloxacin, azithromycin, cefotaxime, doxycycline, sulfamethoxazole, erythromycin, clarithromycin, ofloxacin, norfloxacin.
  - Decongestants: naphazoline, oxymetazoline, xylometazoline.
  - Antiviral metabolite: oseltamivir carboxylate (OC).
- Measurements reported in:
  - River: nanograms per liter (ng/L).
  - WWTP influent/effluent: micrograms per liter (µg/L).

## Sampling Strategy and Frequency
- River sampling:
  - Grab samples (1 L) collected weekly in November 2009 (dates: 3rd, 11th, 16th, 24th) and two additional points (March 15, 2010; May 11, 2011).
- WWTP sampling:
  - Time-proportional samples (750 mL) collected over 24 hours for influent and effluent; sampling included two days (10–11 November 2009) with an additional point on May 11, 2011.
- Locations and timing:
  - 21 river locations with corresponding location IDs and names.
  - WWTPs: Benson and Oxford with specified grid references.
- Storage and preparation:
  - River samples stored at -80°C until analysis; WWTP samples similarly stored until analysis.

## Data Files and Format
- RiverSamplingLocations.csv
  - Contains location information for all 21 river sites (Location ID, Location Name, Eastings/Northings coordinates).
- River_PharmaConcentrations.csv
  - Concentrations (ng/L) of all analytes at each river location and sampling date.
  - Columns include Location ID, Location Name, Date, and each analyte.
- WWTP_PharmaConcentrations.csv
  - Concentrations (ng/L) for influent and effluent at Benson and Oxford WWTPs.
  - Columns include grid reference, Location, Sample (influent/effluent), Date, Time, and each analyte (in µg/L).
- WWTPFlow.csv
  - WWTP influent flow data on the sampling day.
  - Columns: Grid Reference, Location Name, Date, Time, Flow (m3/h).
- RiverFlow.csv
  - River flows at the 21 river sites on the sampling day.
  - Columns: Location ID, Location Name, Date, Flow (m3/s).
- All datasets are provided in CSV format and can be opened with common data analysis software.

## Methods
- Analytical approach:
  - On-line solid-phase extraction/liquid chromatography-tandem mass spectrometry (SPE/LC-MS/MS).
  - Analytes quantified in pre-filtered and acidified samples (1 mL) for river water; WWTP samples analyzed similarly with appropriate preparation.
  - Method details and validation are described in prior publications:
    - Khan et al. 2012: Development and application of a system for determining anti-infectives and nasal decongestants.
    - Singer et al. 2014 (PLOS ONE): Intra- and Interpandemic Variations of antiviral, antibiotics, and decongestants in WWTPs and rivers (open access).
- Data context and usage:
  - Data accompany a publication examining spatial and temporal variations of pharmaceuticals in wastewater and receiving rivers during and around the influenza A(H1N1)pdm09 pandemic.

## How this data supports analysis and reuse
- Enables spatial mapping of pharmaceutical concentrations across 21 river sites and two WWTPs within the Thames catchment.
- Facilitates temporal analyses across pandemic phases (early pandemic, late pandemic, inter-pandemic) using specified sampling dates.
- Supports data integration with geographic coordinates and flow metrics to assess environmental loading and dilution.
- Useful for creating dashboards or self-serve analyses of river/WWTP pharmaceutical concentrations, and for cross-comparison with other water-quality datasets.