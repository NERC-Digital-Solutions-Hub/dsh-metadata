# Transfer to milk

## Overview
- Review of information sources including books, journals, conference proceedings, institutional reports, and international/national databases.
- A centralized database was created to handle and process data from these diverse sources; entries were individually reviewed and revised as needed.
- Supplementary data were added through additional searches, including a major review of relevant Russian-language documents (Fesenko et al., 2007), published as peer-reviewed papers.
- Where data existed, transfer tables provide: number of data points, geometric mean (GM), geometric standard deviation (GSD), arithmetic mean, and standard deviation; for less well-documented radionuclides with a single value, only the arithmetic mean is given.

## Data products and descriptors
- Transfer coefficients for milk and concentration ratios are organized in transfer tables with statistical descriptors when available.
- For cow milk:
  - Fm_GM_DL-1: Cow milk transfer coefficient (Fm) = element concentration in milk divided by element daily intake; GM with units days per litre (DL-1).
  - Fm_GSD_DL-1: Geometric standard deviation.
  - CR_GM: Cow milk concentration ratio (MILK/FEED) geometric mean.
  - CR_GSD: Geometric standard deviation.
  - N: Number of cow milk data points.
- For goat milk:
  - Fm_GM_DL-1 and Fm_GSD_DL-1: Goat milk transfer coefficient with GM and GSD; units days per litre.
  - CR_GM: Goat milk concentration ratio geometric mean.
  - CR_GSD: Goat milk concentration ratio geometric standard deviation.
  - N: Number of goat milk data points.

## Specific variables and data items
- Cow_milk_Fm_GM_DL-1 (definition and GM; units DL-1)
- Cow_milk_GSD_DL-1 (definition and GSD; units DL-1)
- Cow_milk_CR_GM (definition)
- Cow_milk_CR_GSD (definition)
- Cow_milk_N (number of cow milk data for individual elements)
- Goat_milk_Fm_GM_DL-1 (definition and GM; units DL-1)
- Goat_milk_GSD_DL-1 (definition and GSD; units DL-1)
- Goat_milk_CR_GM (definition)
- Goat_milk_CR_GSD (definition)
- Goat_milk_N (number of goat milk data for individual elements)

## Elements covered
- Ag, Am, Ba, Ca, Cd, Ce, Cl, Co, Cs, Fe, I, Mn, Na, P, Pb, Pu, Ru, Se, Sr, U, Y, Zn, Zr
- Each element has an explanation (e.g., transfer coefficient, concentration ratio) and is listed with units as not applicable where appropriate.

## Units
- Fm_GM_DL-1: days per litre (DL-1)
- Fm_GSD_DL-1: days per litre
- CR_GM/CR_GSD: not applicable units (ratios)
- N: not applicable (counts)

## References
- International Atomic Energy Agency (IAEA). Handbook of Parameter Values for the Prediction of Radionuclide Transfer in Terrestrial and Freshwater Environment. Technical Reports Series No. 472. IAEA, Vienna, 2010.
- Fesenko, S., Howard, B.J., Isamov, N., Voigt, G., Beresford, N.A., Sanzharova, N., Barnett, C.L. Review of Russian language studies on radionuclide behaviour in agricultural animals: part 2. Transfer to milk. Journal of Environmental Radioactivity 98 (2007) 104-136.

## GIS relevance and potential applications
- Integrates multi-source data into a single database suitable for GIS analyses and map-based visualizations of radionuclide transfer to milk.
- Enables spatial risk assessment by mapping Fm and CR across dairy systems (cow vs goat) and across radionuclides/elements.
- Supports data-driven decision making for policymakers, clients, or the public by providing standardized metrics (GM, GSD, N) and explicit data coverage per species and element.
- Highlights data standardization challenges and the need for consistent data formats when combining multi-language literature and international sources.

## Limitations and data gaps
- For some radionuclides, data are scarce or single-valued, limiting statistical descriptors (GM/GSD) available.
- Data availability may vary between cow and goat milk, and across elements, affecting completeness of maps and analyses.