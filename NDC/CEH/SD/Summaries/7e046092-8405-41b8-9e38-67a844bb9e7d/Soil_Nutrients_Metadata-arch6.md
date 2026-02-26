# Dataset Description (Soil_Nutrients)

- A dataset describing soil nutrient availability across unlogged tropical forest, logged tropical forest and oil palm plantation in Sabah, Malaysia. Samples collected March–April 2016 as part of the NERC-funded BALI project.
- Data are presented as nutrient supply rates per 10 cm2 over a 14-day burial period, with units per element provided.

## Sampling design and collection

- Study sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Land uses: Unlogged tropical forest, Logged tropical forest, and Oil palm plantation.
- Plot design: 9 one-hectare plots (1 Ha) across the three sites, sampled using a stratified approach.
- Subplot structure: Each 1 Ha plot subdivided into 25 subplots (20 m x 20 m); 3 subplots randomly selected for sampling.
- Ion exchange membranes: At 3 locations within each subplot, 4 pairs of PRS ion exchange membranes (1 cation + 1 anion pair per location) buried to ~10 cm depth for 2 weeks.
- Sample processing: Membranes collected, washed, eluted with 0.5 M HCl for 1 hour; four probe pairs pooled per location before elution.
- Analyses:
  - NO3-N and NH4-N measured colorimetrically via automated flow injection analysis (FIA).
  - All other elements measured by inductively coupled plasma optical emission spectroscopy (ICP-OES).
- Output metric: Results reported as supply rates per 10 cm2, over 14 days (µg/10 cm2/14 days).

## Dataset structure and metadata

- Key columns (21 total): Identifier, Site, Land_Use, Plot_Name, Subplot, NO3_N, NH4_N, Total_N, Ca, Mg, K, P, Fe, Mn, Cu, Zn, B, S, Pb, Al, Cd.
- Units:
  - NO3_N, NH4_N, Total_N, and all metal/element concentrations: µg/10 cm2 / 14 days.
  - Subplot: numeric; Plot_Name and Site/Land_Use are text fields.
- Total_N is the sum of NO3_N and NH4_N.

## Method detection limits (MDL) and data quality

- MDLs (µg/10 cm2 / 14 days):
  - NO3_N: 2
  - NH4_N: 2
  - Ca: 2
  - Mg: 4
  - K: 4
  - P: 0.2
  - Fe: 0.4
  - Mn: 0.2
  - Cu: 0.2
  - Zn: 0.2
  - B: 0.2
  - S: 2
  - Pb: 0.2
  - Al: 0.4
  - Cd: 0.2
- Data treatment: Values are reported as measured even if below MDL; zeros indicate concentrations below detectable limits.

## Practical uses and data products

- Enables cross-site comparisons of nutrient supply across forest types and land uses.
- Supports data products (dashboards, pivot tables, reports) to enable end-user exploration of nutrient availability and how it varies by site, land-use, and subplot.
- Can be combined with other soil properties or spatial data to explore drivers of nutrient supply and to support conservation or land-management decisions.

## Considerations and caveats

- Sampling spans three sites within Sabah, Malaysia; results are context-specific to these locations and sampling period (Mar–Apr 2016).
- Data reflect supply rates from membrane-based measurements over 14 days and may not map directly to instantaneous soil solution concentrations.
- Patchy data detection (MDL considerations) should be accounted for when combining with other datasets or when performing imputation.

## References

- Qian, P. & J. J. Schoenau (2002) Practical applications of ion exchange resins in agricultural and environmental soil research. Canadian Journal of Soil Science, 82, 9-21.
- Riutta, T., et al. (2018) Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests. Global Change Biology.
- Western Ag. (www.westernag.ca)