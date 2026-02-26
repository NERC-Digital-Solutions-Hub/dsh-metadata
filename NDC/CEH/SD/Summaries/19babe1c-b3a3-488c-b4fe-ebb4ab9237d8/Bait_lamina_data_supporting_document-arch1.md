# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016)

## Overview
- A dataset package accompanying the study of soil biological activity in the Chernobyl Exclusion Zone (CEZ) for 2005 and 2016, linked to the paper Beresford et al., 2021.
- Combines radionuclide concentration data, bait-lamina feeding activity data, reader assessments, site metadata, and modeled dose-rate estimates for soil biota.
- Aims to enable analysis of correlations between radionuclide contamination, soil invertebrate/ microbial feeding activity, and estimated radiation doses to soil organisms.

## Data files and what they contain
- Radionuclide_concentration_data_2005.csv (Table 1)
  - Column headings include sample identifiers, sample type (soil), date, location (latitude/longitude), site (Low, Medium, High; Dead near High), plot, and activity concentrations for Cs-137, Sr-90, Cs-134, K-40, Co-60 (all in dry mass basis; some values may be listed as < minimum detectable activity).
- Bait_lamina_2005.csv (Table 2)
  - Radionuclide data for Am-241, Eu-154, Eu-155, Pu-238+239+240 (all in dry mass; detectable activities or < LOD as applicable).
- Reader_1_bait_lamina_2016.csv and Reader_2_bait_lamina_2016.csv (Table 3)
  - Field deployment: 18 sites, 3 plots per site, 16 bait-lamina sticks per plot in a 4x4 grid.
  - For each strip: top-to-bottom hole status (1 = pierced, 0 = not), reader 1 and reader 2 tallies, with strand-level hole data (16 holes per stick across 16 bite indicators per reader).
  - Includes plot and replicate identifiers, and notes on quality checks.
- Main_data_2016.csv (Table 4)
  - Contains site/location metadata (Location, Plot, Latitude, Longitude), ambient dose rate (µSv/h), soil properties (Cs-137, Sr-90, Am-241, Pu isotopes by Bq/kg dry mass), Pu below LOD indicator, dose-rate estimates for three organisms (Annelid, Detritivorous Arthropod, Bacteria) in µGy/h, and bait-lamina derived feeding metrics (Reader 1/2 total bites, average total bites, percent utilization, bite holes per segment, soil pH, soil moisture, bulk density, soil temperatures in Apr/May 2016, habitat classification, and field notes).
  - Includes aggregated bite metrics (e.g., Bite_holes_1_4, 1_8, 9_16; Bite_holes_1_8; etc.) and simple habitat categorization.
- Concentration_ratios.csv (Table 5)
  - Concentration ratios used for dose modeling, separated by organism groups (Annelid; Detritivorous Arthropod) and nuclides (Cs, Sr, Am, Pu), with notes indicating the nuclide, target organism, and respective ratios.
- Additional context elements
  - Figure 1 caption describes bait lamina strips being read after ~18 days in soil.
  - Tables 1–5 include column heading explanations, clarifying units/methodology for each data file.

## Study sites, design, and sampling timing
- 2005 study
  - Four CEZ sites: Red Forest (two sites named High and Dead in the dataset), Izumrudnoe (Low), and Novoshepel Forestry (Medium).
  - Dead site: area with pine trees killed in 1986 near the High site.
  - Bait lamina deployed; soil pH and moisture recorded.
- 2016 study
  - Eighteen CEZ sites; eight within the Red Forest; ambient dose rates span roughly a twenty-fold range.
  - Habitat groups: Coniferous woodland, Deciduous woodland, Red Forest.
  - GPS locations recorded; three 1x1 m plots per site; 16 bait lamina sticks per plot deployed in a 4x4 grid.
  - Deployment dates: 17–19 April 2016; retrieval ~18 days later (5–7 May 2016).
  - Soil temperature measured at insertion and removal.

## Bait lamina methodology and data collection
- Bait lamina sticks: PVC strips (~155 x 6 x 1 mm) with 16 bi-conical apertures at 5 mm intervals. Apertures filled with bait (70% cellulose, 25% finely ground wheat bran, 5% active charcoal).
- Field protocol (ISO 2016): three plots per site; 16 sticks per plot; strips inserted with top aperture just below soil surface; one additional strip inserted/withdrawn to check abrasion.
- Readout: strips read blind by two readers; feeding activity recorded as a binary pierced/unpierced outcome per hole; results averaged across readers.
- Data aggregation: in analyses, results per plot summed across the 16 sticks.

## Lab analyses and radionuclide measurements
- Cs-137 and Sr-90 measured in soil samples; Cs-137 via gamma spectroscopy (HPGe detector), Sr-90 via beta spectroscopy; quality controls and detection limits noted (e.g., MDAs and uncertainties).
- Am-241 and Pu isotopes (238, 239, 240) measured via HPGe detector; method cross-referenced to radiochemical methods; isotopic ratios from Red Forest studies used to estimate Pu inputs for ERICA/R&D128 modeling.
- Concentration data are reported as activity per unit dry mass (Bq/kg DM) for the radionuclides.

## Dose-rate estimation for key soil organisms
- Annelid (earthworms) and Detritivorous Arthropod dose rates estimated with the ERICA Tool (Brown et al. 2008, 2016).
- Soil Bacteria dose rates estimated with the R&D128 approach (Environment Agency/R&D 128), due to limitations of ERICA for bacteria size.
- Assumptions:
  - 100% occupancy within the soil column for all organisms.
  - Internal concentrations derived from concentration ratios (CRs): Lumbricidae-derived CRs (2014 data) for annelids; ERICA default CRs for detritivorous arthropods.
  Pu isotopes input uses Red Forest 2014 isotopic ratios for 238Pu/239Pu/240Pu.
- Measured soil dry matter used to scale absorbed dose rates; changes in dry matter fraction affect external dose rate proportionally.

## Data quality, standards, and provenance
- Data include standardized column explanations (Tables 1–5) to support reproducibility and reuse.
- Readers’ bite data are averaged across two independent observations, with blind readings to reduce bias.
- Dose modeling relies on established tools (ERICA Tool; R&D128) and published CR/Isotope data; uncertainties and LOIs are acknowledged in the methods.
- Metadata and accompanying references provide traceability to ISO standards, calibration sources, and prior work on the CEZ.

## How analysts can use this data
- Correlation analyses between ambient/radionuclide contamination (Cs-137, Sr-90, Pu isotopes, Am-241, etc.) and feeding activity (percent utilization, total bites, bite-hole distributions) across sites and habitats.
- Cross-year comparisons (2005 vs. 2016) to assess changes in soil biology activity relative to contamination and environmental conditions.
- Dose-response modeling for three organism groups (Annelids, Detritivorous Arthropods, Bacteria) using modeled dose rates and measured contamination levels.
- Habitat-specific effects by comparing Coniferous vs. Deciduous vs. Red Forest sites.
- Spatial patterns analyses leveraging site coordinates and ambient dose rate measurements.
- Data integration and reproducibility supported by explicit data dictionaries (Tables 1–5) and detailed methods.

## References and related materials
- Data are tied to Beresford et al., 2021; and related methodological and reference datasets (e.g., ERICA Tool publications, ISO 18311:2016 bait-lamina methodology, and Red Forest isotope studies).
- Primary measurement methods and calibration sources are cited in the Materials and Methods, including standard radionuclide measurement techniques and dose-estimation models.