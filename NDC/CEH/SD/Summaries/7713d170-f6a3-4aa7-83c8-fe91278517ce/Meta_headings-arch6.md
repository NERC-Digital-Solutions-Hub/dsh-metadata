# Transfer to milk: database and transfer tables for radionuclide concentrations in cow and goat milk

## Overview

- A database was created to handle and process data drawn from diverse sources (books, journals, conference proceedings, institutional reports, and international databases).
- Entries were individually reviewed and revised; augmented with new source data through additional English-language searches and a major review of Russian-language studies (Fesenko et al., 2007) published as peer-reviewed papers.
- When data are sufficient, transfer table values are provided, including: number of data points, geometric mean (GM), geometric standard deviation (GSD), arithmetic mean (AM), and standard deviation (SD). For less well documented radionuclides with a single value, only the arithmetic mean column is filled.

## Data and metrics

- Key transfer metrics include:
  - Cow_milk_Fm_GM_DL-1: Cow milk transfer coefficient (Fm) defined as the ratio of element concentration in cow milk to element daily intake; GM; units: days per litre (DL-1).
  - Cow_milk_Fm_GSD_DL-1: Geometric standard deviation for the cow milk Fm; units DL-1.
  - Cow_milk_CR_GM: Cow milk concentration ratio (CR) defined as the equilibrium ratio of milk element concentration to feed concentration; GM; units: not applicable.
  - Cow_milk_CR_GSD: Geometric standard deviation for the cow milk CR; units not applicable.
  - Cow_milk_N: Number of cow milk data points for individual elements.
  - Goat_milk_Fm_GM_DL-1, Goat_milk_Fm_GSD_DL-1: Corresponding goat milk Fm metrics.
  - Goat_milk_CR_GM, Goat_milk_CR_GSD: Goat milk CR metrics.
  - Goat_milk_N: Number of goat milk data points for individual elements.

## Elements covered

- The dataset includes entries for a range of elements with explanations and unit notes, including:
  - Ag, Am, Ba, Ca, Cd, Ce, Cl, Co, Cs, Fe, I, Mn, Na, P, Pb, Pu, Ru, Se, Sr, U, Y, Zn, Zr
- Each element entry provides the explanation (e.g., element symbol) and indicates that units are not applicable for the listed transfer metrics (as these are dimensionless ratios or relative measures).

## Data structure and naming

- Data are organized into clearly named fields, such as:
  - Cow_milk_Fm_GM_DL-1, Cow_milk_Fm_GSD_DL-1, Cow_milk_CR_GM, Cow_milk_CR_GSD, Cow_milk_N
  - Goat_milk_Fm_GM_DL-1, Goat_milk_Fm_GSD_DL-1, Goat_milk_CR_GM, Goat_milk_CR_GSD, Goat_milk_N
- This naming convention standardizes the representation of transfer coefficients and concentration ratios for both cow and goat milk.

## References

- International Atomic Energy Agency (IAEA). Handbook of Parameter Values for the Prediction of Radionuclide Transfer in Terrestrial and Freshwater Environment. Technical Reports Series No. 472. IAEA, Vienna, 2010.
- Fesenko, S.; Howard, B.J.; Isamov, N.; Voigt, G.; Beresford, N.A.; Sanzharova, N.; Barnett, C.L. Review of Russian language studies on radionuclide behaviour in agricultural animals: part 2. Transfer to milk, Journal of Environmental Radioactivity 98 (2007) 104-136.