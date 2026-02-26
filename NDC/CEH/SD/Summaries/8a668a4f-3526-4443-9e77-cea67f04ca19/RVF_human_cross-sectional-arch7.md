# Rift Valley fever virus seroprevalence data from people involved in a cross-sectional survey in Tana River and Garissa counties, Kenya (December 2013 - February 2014)

## Overview
- Cross-sectional seroprevalence survey investigating Rift Valley fever (RVF) seroprevalence among people in Tana River and Garissa counties, Kenya.
- Focused on land-use change (irrigation schemes vs pastoral/rangeland) and access to ecosystem services.
- Data collected at the household level; includes geographic and demographic information, and RVF IgG test results.

## Study design and geography
- Households were the primary sampling units; sample size planned at 220 households per land-use type using formal power calculations for two independent proportions.
- Study sites included:
  - Bura and Hola irrigation schemes in Tana River County
  - Villages bordering these irrigation schemes with nomadic pastoralism
  - Ijara and Sangailu divisions in Garissa County with transhumance pastoralism
- Sampling aimed to cover irrigated, pastoral, and riverine areas; a few riverine households were included.
- Location data collected at multiple administrative levels: county, district, division, location, sublocation, and village.
- Geographic coordinates and altitude captured, but coordinates were withheld for ethical considerations.

## Data collection workflow
- Ethical approval obtained from AMREF-ESRC; consent at community, household, and subject levels.
- Field intake included group meetings to review objectives and work plans; household heads provided consent before sampling.
- Data collection used Open Data Kit (ODK) on smartphones; included geographic coordinates in decimal degrees and altitude.
- Data linkage and quality controls included:
  - Barcoded tubes linked to households and subjects via smartphone camera reads.
  - Central ODK Aggregate server used for daily uploads.
  - Pre-identified sampling tubes and duplicates to minimize transcription errors.
  - Weekly replenishment of dry ice for sample preservation.

## Sample collection and laboratory methods
- Subjects: individuals aged five years and above.
- Blood collection volumes by age group:
  - 5–12 years: up to 5 ml
  - 13–17 years: 5–10 ml
  - 18+ years: 10 ml
- Samples processed into serum and whole blood; aliquoted into 2 ml cryo-tubes for working and long-term storage.
- Samples preserved in dry ice, then transferred to liquid nitrogen at the ILRI Nairobi biorepository.
- RVF IgG screening performed on working serum using an inhibition ELISA (protocol described in Paweska et al., 2005).

## Dataset and structure
- Data file: DDDAC_Kenya_human RVF seroprevalence.csv
- Contains 23 variables (described in Table 1 of the source document).
- Key variable groups:
  - Geographic/administrative: county, district, division, location, sublocation, villagename
  - Site characterization: area (irrigation, pastoral, riverine)
  - Household and individual identifiers: hhid, relationshiphh, hhgender, hhoccup, hhage, gender, age
  - Demographics and household composition: nmales, nfemales
  - Sample and laboratory: sampleid, aliquot id, result (positive/negative), altitude
  - Livestock and exposure context: livestk_home
- Coordinates and altitude: geographic coordinates collected (decimal degrees) and altitude included; coordinates themselves withheld for ethical considerations in the public dataset.
- Data quality features:
  - Data collected via ODK with built-in data relationships to minimize transcription errors
  - Field and lab processes included duplicates and re-analysis for borderline results

## Data quality, ethics, and governance
- Ethical safeguards:
  - Community, household, and subject-level consent obtained
  - Coordinates withheld to protect privacy
- Quality control measures:
  - Duplicates in laboratory analyses
  - Re-analysis of borderline results
  - Barcoded sampling tubes linked to household and subject data
  - Daily data uploads to centralized server to reduce transcription errors

## GIS-oriented considerations and best uses
- Strengths:
  - Rich spatial context across multiple administrative levels and site types (irrigation, pastoral, riverine)
  - Comprehensive linkage between household, demographic, and serology data
  - Inclusion of altitude and area classification supports spatial analyses of seroprevalence by environment and land use
- Limitations:
  - Precise GPS coordinates are withheld, limiting fine-scale mapping; analyses must rely on available administrative/locational fields (subcounty/division/sublocation/village)
  - Cross-sectional design limits temporal trend analyses
- Potential GIS applications:
  - Mapping seroprevalence patterns by area type and administrative units
  - Analyzing associations between seroprevalence and land-use categories (irrigation vs pastoral vs riverine)
  - Integrating with irrigation scheme boundaries, population density, and ecological variables to explore spatial risk factors
  - Using altitude and area data to assess topographic or environmental influences on RVF exposure

## Notes on Table 1 (variables)
- The dataset includes a detailed list of variables such as sampling date, sample IDs, county/district/division/location details, sublocation and village names, household and individual demographics, area type, sampling results, altitude, and livestock exposure indicators.
- Some geographic detail is present at multiple hierarchical levels, enabling regional analyses despite the intentional withholding of exact coordinates.