# Cow milk and goat milk radionuclide transfer data and transfer coefficients

## Overview
- Compilation and processing of information from books, journals, conference proceedings, institutional reports, and international/national databases.
- A dedicated database was created to handle and process data from diverse sources, with entries reviewed and revised as needed.
- Supplementary data were added through additional searches, including a major review of Russian-language documents (Fesenko et al., 2007) published as peer-reviewed papers.
- Where data were sufficient, transfer table values include: number of data, geometric mean (GM), geometric standard deviation (GSD), arithmetic mean, and standard deviation.

## Data sources and processing
- Data drawn from English and Russian language literature; Russian studies are being published in a series of peer-reviewed papers.
- Entries in the database are continuously supplemented by new source data when available.
- Data handling includes clear documentation of data provenance and enabling future reuse via metadata.

## Data fields and metrics
- Cow milk transfer coefficient (Fm) for each element: Fm = concentration in cow milk / element daily intake; reported as geometric mean (GM) with units days per litre (DL-1).
  - Cow_milk_Fm_GM_DL-1: GM of Fm
  - Cow_milk_Fm_GSD_DL-1: GSD of Fm
  - Units: DL-1 (days per litre)
- Cow milk concentration ratio (CR) for each element: CR = concentration in milk / concentration in feed; reported as GM and GSD.
  - Cow_milk_CR_GM: GM of CR
  - Cow_milk_CR_GSD: GSD of CR
  - Units: not applicable
- Data counts
  - Cow_milk_N: Number of cow milk data points for each element
- Goat milk transfer coefficient (Fm) and concentration ratio (CR) data prepared similarly to cow milk
  - Goat_milk_Fm_GM_DL-1, Goat_milk_Fm_GSD_DL-1
  - Goat_milk_CR_GM, Goat_milk_CR_GSD
  - Goat_milk_N: Number of goat milk data points
- Units and terminology
  - Units for Fm: DL-1 (days per litre)
  - CR values: dimensionless (ratio)

## Radionuclides covered
- Silver (Ag), Americium (Am), Barium (Ba), Calcium (Ca), Cadmium (Cd), Cerium (Ce), Chlorine (Cl), Cobalt (Co), Caesium (Cs), Iron (Fe), Iodine (I), Manganese (Mn), Sodium (Na), Phosphorus (P), Lead (Pb), Plutonium (Pu), Ruthenium (Ru), Selenium (Se), Strontium (Sr), Uranium (U), Yttrium (Y), Zinc (Zn), Zirconium (Zr)
- Data tables and analyses may include these elements in cow and goat milk contexts.

## Data presentation and interpretation
- Transfer tables present both GM and GSD values when data are sufficiently documented.
- For less well-documented radionuclides with a single value, only the arithmetic mean is provided.
- The dataset enables cross-species comparison (cow vs. goat milk) and assessment of element-specific transfer behaviour.

## References
- International Atomic Energy Agency (IAEA). Handbook of Parameter Values for the Prediction of Radionuclide Transfer in Terrestrial and Freshwater Environment. Technical Reports Series No. 472. IAEA, Vienna, 2010.
- Fesenko, S., Howard, B.J., Isamov, N., Voigt, G., Beresford, N.A., Sanzharova, N., Barnett, C.L. Review of Russian language studies on radionuclide behaviour in agricultural animals: part 2. Transfer to milk, Journal of Environmental Radioactivity 98 (2007) 104-136.

## Analyst takeaways and considerations
- The compilation aims to support modelling and risk assessment by providing standardized transfer metrics (Fm, CR) with accompanying uncertainty (GM, GSD).
- Data gaps are acknowledged, particularly for local scales and less well-documented radionuclides; efforts include integration of Russian-language sources to broaden coverage.
- Data provenance and metadata are emphasized to aid future discoverability and reuse.
- Practical use requires attention to scale, data heterogeneity, and potential differences between cow and goat milk transfer behaviours.