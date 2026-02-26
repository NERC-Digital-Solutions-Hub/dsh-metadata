# Amazon tree ring isotope records of Macrolobium acaciifolium and Cedrela odorata

## Overview
- Dataset of tree ring oxygen (δ18Otr) and carbon (δ13Ctr) isotope data from Macrolobium acaciifolium and Cedrela odorata.
- Five sites across the Amazon basin: Pacaya (Peru), Maranon (Peru), Leticia (Colombia), Manuripi (Bolivia), and Riberalta (Bolivia).
- Macrolobium represents seasonal floodplain forests; Cedrela represents terra firme forests.
- Aims to capture spatial coverage and climate-related differences in isotope signals.

## Data content
- Isotopes: δ18Otr (oxygen) and δ13Ctr (carbon).
- Resolution: high-resolution sub-annual sampling or annual resolution (Data_type field indicates this).
- Year field indicates the year of ring formation.
- Site and geography: Site name, longitude, and latitude for each sample.
- Sample and core data: Ring_subsection (ring count for high-resolution data), Core (increment core ID), Species.
- Data standards: δ13C expressed relative to Vienna-PDB; δ18O expressed relative to SMOW.

## Data structure (fields)
- Year: Year of ring formation.
- Delta: Isotope ratio value relative to standard (‰).
- Isotope: Which isotope (oxygen or carbon).
- Data_type: High-resolution sub-annual or annual.
- Ring_subsection: Ring count for high-resolution data.
- Core: Increment core identification number.
- Species: Scientific species name.
- Site: Site location name.
- Site_longitude: Longitude of sample location.
- Site_latitude: Latitude of sample location.

## Data collection and processing
- Sample preparation conducted at the University of Leeds (cutting ring sections, cellulose extraction, weighing, packing).
- Isotope ratio measurements performed at the Stable Isotope Laboratory, University of Leicester.
- Data preparation notes reference Cintra et al. 2019 for details on high-resolution sampling.
- Data structure allows integration of measurements across different resolutions and sites.

## GIS and spatial analysis considerations
- Provides precise site coordinates enabling spatial mapping of isotope signals across the Amazon basin.
- Suitable for combining with climate datasets to analyze spatial patterns and environmental drivers of isotope variability.
- Requires careful handling when merging high-resolution and annual data due to differing temporal granularity.

## Access, license, and citation
- License: Open Government Licence.
- Data access: https://doi.org/10.5285/a5a862da-8db2-4881-9046-610c8573b499
- Citation: Cintra, B.; Boom, A.; Schöngart, J.; Gloor, E.; Brienen, R. (2020). Amazon tree ring isotope records of Macrolobium acaciifolium and Cedrela odorata. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/a5a862da-8db2-4881-9046-610c8573b499
- Data are provided under the Open Government Licence; citation of the above is required when using the data.

## Funding and contacts
- Funded by NERC-UK projects on the Amazon hydrological cycle and related themes.
- Contacts: Dr. Bruno Cintra (brunoblcintra@gmail.com); Dr. Roel Brienen (r.brienen@leeds.ac.uk)