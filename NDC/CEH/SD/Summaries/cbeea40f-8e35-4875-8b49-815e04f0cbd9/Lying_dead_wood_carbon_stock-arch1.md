# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

## Overview
- Describes biomass stock in the lying dead wood pool, including fallen trees sampled along transects for each plot.
- Associated with ESPA and the P4GES project; DOI provided.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data structure and key variables
- Site_ID: P4GES site code; Text; no specified unit
- Category: wood density category (S: sound, I: intermediate, R: Rotten); Categorical; Unit: (none)
- Density: corresponding density values for the wood category; Numeric; Unit: Unitless; 0 indicates absent dead wood
- Diameter: diameter of the dead wood trunk in the transect crossing area; Numeric; Unit: Centimeter (cm)
- Volume: estimated volume of lying dead wood; Numeric; Unit: cubic metres (m3); Method: based on Winrock International 2005
- Biomass: biomass stock of lying dead wood; Numeric; Unit: Mg.ha-1
- Stock_C: carbon stock of lying dead wood; Numeric; Unit: Mg.ha-1
- Field and materials_ressources: equipment or methods referenced (e.g., forester compass for diameter)

## Notes and data quality
- Notes field indicates “means no data” for missing values in applicable records.

## Data provenance and references
- Density, diameter, volume, biomass, and carbon stock derived from field measurements and established methods.
- Volume method references Winrock International 2005: Impact of logging on carbon stocks of tropical forests – Republic of Congo case study.
- References DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Reference: Winrock International 2005 report available at the provided link.

## Usage considerations for analysis
- Data can be used to estimate lying dead wood biomass and carbon stocks, explore relationships between wood density category, diameter, volume, and carbon content.
- Missing data should be handled according to the “Notes” guidance; 0 density indicates no dead wood.
- Methodological provenance (Winrock 2005) informs volume-to-biomass conversions and context for interpreting results.
- Documentation and metadata emphasize dataset discoverability and traceability via site codes and project provenance.

## Acknowledgements
- Acknowledgement of Laboratory of Isotopes, University of Antananarivo required for products derived from these data.