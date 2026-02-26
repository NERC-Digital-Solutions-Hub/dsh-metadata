# Digestate_HF_and_NW_NH3_v2.csv

## Overview
- Dataset from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW) research stations.
- Contains 8 columns and 304 rows describing NH3 emissions under different digestate treatments.
- Emissions measured over a 7-day period with site-specific sampling schedules; data are presented as NH3-N emissions expressed as NH3 flux converted to NH4 and captured with acid traps.
- Digestate sources differ by site: HF uses digestate from Fre-energy (Wrexham); NW uses digestate from Holsworthy. Treatments include digestate, acidified digestate, and nitrification inhibitor variants.

## Dataset scope and structure
- Sites: HF (Henfaes) and NW (North Wyke).
- Measurements cover NH3 emissions captured over 7 days, with site-specific sampling times.
- Data structure captures treatment, plot-level design, and emission results.
- Data are accompanied by a concise method description for NH3 capture and conversion to NH4, including detection limits.

## Column definitions
- Site: HF or NW, indicating measurement location.
- Midpoint_time: Midpoint of the NH3 measurement period (timepoint within the period; no explicit unit stated).
- Hours_since_digestate_app: Hours elapsed since digestate application.
- Block: Blocking factor in the randomised block design (values 1–4).
- Plot: Experimental plot identifier.
- Treatment: Digestate treatment code:
  - D = digestate
  - AD = acidified digestate (pH ~5.5 at HF, ~3 at NW)
  - DNI = digestate with nitrification inhibitor (DMPP)
  - ADNI = acidified digestate with nitrification inhibitor (DMPP)
- NH3_qa1: NH3-N emissions from the plot over the 7-day measurement period (units: kg ha⁻¹).
- NH3_qa2: Same as NH3_qa1, but negative NH3 fluxes replaced with 0.

## Treatments and coding
- Digestate treatments are coded to reflect processing and inhibitors:
  - D: standard digestate
  - AD: acidified digestate
  - DNI: digestate with DMPP inhibitor
  - ADNI: acidified digestate with DMPP inhibitor

## Measurement methods and QA
- NH3 captured using gas traps containing phosphoric acid; NH3 converted to NH4 upon contact with acid.
- Air circulated from wind tunnels to traps via intake pipes positioned at plot edges.
- NH4 traps changed 2–3 times per day on the first day at HF/NW due to expected higher volatilization rates.
- Detection limit: 0.01 mg NH4-N L⁻¹.
- Emission values are represented as NH3-N flux aggregated to NH3_qa1 and adjusted to NH3_qa2 where negative fluxes are set to zero.

## Measurement schedule and sites
- HF: Emissions measured over 7 days at 4 h and 24 h, and 2–7 days post-application.
- NW: Emissions measured over 7 days at 1 h, 3 h, 6 h, and 24 h, and 2–7 days post-application.
- Different digestate sources and pH adjustments applied per site (HF uses Fre-energy digestate; NW uses Holsworthy digestate).

## Data quality, limitations, and notes
- 8 columns, 304 rows; timeline and sampling frequency differ between sites, which may affect cross-site comparability.
- NH3_qa2 capping negative fluxes to zero should be considered during analysis.
- Units: NH3_qa1/ NH3_qa2 are in kg ha⁻¹; Hours_since_digestate_app in hours; detection limit for NH4-N is 0.01 mg L⁻¹.
- Documentation describes methodology and data lineage; potential gaps include missing explicit units for Midpoint_time.

## Provenance and data lineage
- Derived from field trials at two sites with distinct digestate treatments and emission collection methods.
- Data supplement to broader supporting documentation for CINAg experiments.
- Data file name indicates version: v2.

## Governance implications and recommendations for Data Stewards
- Metadata completeness:
  - Include explicit Midpoint_time units if available; currently unspecified.
  - Clarify any site-specific differences in measurement timing and sampling protocols for consistent downstream use.
- Data consistency:
  - Maintain clear mapping of Treatment codes to definitions in a data dictionary.
  - Preserve NH3_qa1 and NH3_qa2 definitions (negative flux handling) for reproducibility.
- Provenance and reproduction:
  - Record digestate source details (facility, location) and pH adjustment specifics per site.
  - Document the wind tunnel setup and trap deployment to enable replication.
- Data quality management:
  - Capture detection limits and any data censoring or handling rules (e.g., replacement of negative values).
  - Include notes on any data cleaning steps performed prior to sharing.
- Access and lifecycle:
  - Maintain versioning (v2) and record any updates or corrections to the dataset.
  - Link to the main Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf for full methodological context.

## Access, storage, and sharing considerations
- Ensure dataset is stored with accompanying data dictionary and measurement protocol.
- Provide clear references to site-specific methods and supporting documents to aid discoverability and reuse.
- When updating, preserve previous versions and document changes to column definitions or measurement methods.