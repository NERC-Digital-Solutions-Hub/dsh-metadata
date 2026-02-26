# EIDC Supporting information Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

## Overview
- Provides monthly atmospheric concentrations from NI DELTA Gas and Aerosol Monitoring Network for 2019 and 2020.
- Data cover inorganic reactive gases (NH3, HNO3, SO2) and inorganic aerosols (NH4+, NO3-, SO4 2-, Cl-, Na+, Ca2+, Mg2+).
- Joint effort by AFBI and UKCEH; funded by DAERA.

## Monitoring network and sites
- Four NI DELTA sites across NI to improve spatial coverage:
  - Hillsborough (AFBI25)
  - Ballynahone (AFBI26)
  - UoU Coleraine (AFBI27)
  - Sandholes (AFBI28)
- Start dates in 2019; ongoing at each site.
- Sites designed to capture spatial variability and seasonal trends; enables assessment of NH3 with acid gases and inorganic aerosol relationships.

## Methodology: UKCEH DELTA® system
- Low-volume diffusion denuder method for long-term monitoring of reactive gases (NH3, HNO3, SO2) and aerosols (NH4+, NO3-, SO4 2-, Cl-, Na+, Ca2+, Mg2+).
- Sampling: monthly cycles; flow rates 0.2–0.4 L/min; volume recorded by gas meters.
- Analysis performed by UKCEH Lancaster; extracts analyzed for ions via IC, SEAL-AA3, ICP-OES.
- Sample train captures both gas and aerosol phases; includes denuders and filters; key species listed in Tables 2–4.
- Typical monthly detection limits (LOD) provided for major ions.

## Data collected and units
- Concentrations reported as monthly time-integrated averages in micrograms per cubic meter (µg m-3).
- Calculations based on measured mass divided by sampled air volume (m3); volume typically ~15 m3 per month.

## Quality control and data processing
- Stage 1: Automated QC in AAGA with EBAS-style flags; checks for:
  - Correct date sequencing
  - Normal monthly exposure duration (±5 days) (extended periods flagged, e.g., COVID-related)
  - Consistent sampling flow
  - Outlier rejection from blanks
  - Handling of missing samples (-9999; marked invalid)
- Stage 2: Manual QC
  - Manual review of blanks, ion balance (Na+:Cl-, NH4+:NO3-+2SO4 2-), malfunction flags, and outliers
- Stage 3: Expert/project manager review
  - Site context, expected patterns, year-to-year and site-to-site comparisons
  - Relationships between gas and aerosol phases
  - Final ratified output with timestamp and version
- All outputs are time-stamped, version-controlled, and flagged as ratified or not.

## Data structure and contents
- Data organized per site and month; unit: µg m-3.
- Key fields (example from Table 5):
  - site_id, site_name, network_id
  - parameter_id (gas: NH3_g, a_HNO3_g, a_SO2_g; aerosols: a_NH4_p, a_NO3_p, a_Cl_p, a_Na_p, a_Ca_p, a_Mg_p)
  - measurement_start_date/time and measurement_end_date/time
  - measurement (concentration value)
  - less_than flag (LOD status)
  - verification_id, unit_id, data_capture, validity_id, EMEP_code
  - MONTH, YEAR
  - Comments
- Final ratified dataset combines all data with appropriate flags.

## Data flags and EBAS alignment
- EBAS data flags used across NI networks for consistency with European monitoring (EMEP).
- Flags grouped into:
  - Missing (Group 9)
  - Unknown/miscellaneous (Group 7)
  - Mechanical/instrumental problems (Group 6)
  - Chemical problems (Group 5)
  - Extreme/inconsistent values (Group 4)
  - Exceptions for aggregated datasets (Group 3)
  - Other exception flags by database coordinator (Group 2)
  - Accepted irregular data (Group 1)
  - Valid data (Group 0)
- Examples (non-exhaustive): 147 V (below detection limit but reported), 659/658 (sampling anomalies), 699 I (mechanical problem), 999 M (missing), 000 V (valid data).
- Full EBAS flag list available at the provided EBAS/NILU URL.

## Resource locators and references
- AGANet (Acid Gas and Aerosol Network): https://uk-air.defra.gov.uk/networks/network-info?view=aganet
- NAMN / NH3 monitoring network (ALPHA/DELTA): https://uk-air.defra.gov.uk/networks/network-info?view=nh3
- EBAS flags (EMEP data submission): https://projects.nilu.no/ccc/flags/
- EN 17346 (ammonia diffusion sampling standard) and related literature cited for methodology and validation

## Potential uses for analysts
- Testing atmospheric transport models and estimating annual budgets for reduced vs. oxidised nitrogen and for sulphur in NI.
- Assessing spatial and seasonal patterns of NH3, NH4+, NO3-, SO4 2-, and other base cations.
- Supporting cross-network comparisons by harmonized data flags and standardized data structure.
- Enabling data re-use via well-documented QC stages, versioned outputs, and EBAS-compatible flags.