# PRECIPITATION CHEMISTRY Version 1.1 (supplier contact details updated July 2005)

## Aim
- To measure the chemical composition of precipitation and dry deposition (bulk precipitation) at ECN sites using a continuously open gauge.
- Context: acid rain and atmospheric deposition have long been studied; deposition impacts ecosystems and will be influenced by future emissions.
- Bulk deposition measurement integrates both wet and dry deposition; separating components is possible but was deemed too costly for ECN.
- Results can be linked with UKPCMN data to map geographical distribution and trends.

## Context and GIS relevance
- Data describe spatial distribution of precipitation chemistry across ECN sites and can be integrated with other networks (e.g., 32 rural UKPCMN sites).
- Core identifiers for mapping: Site Identification Code, Core Measurement Code, Location Code, and Sampling Date/Time.
- Enables temporal mapping of chemical constituents (weekly measurements) and comparison across sites.

## Equipment and site setup
- Bulk collector design: conical polythene funnel, 63° cone, 115 mm or 152 mm diameter, mounted ~1.75 m above ground, with a 1 mm mesh filter and steel jacket.
- Site placement guidelines: place upwind of contamination sources, away from dusty tracks and animals, clear of obstructions; secure to ground or structure.
- Regular maintenance: funnel cleaning, decontamination procedures, and bird deterrents; ensure proper containment and minimize contamination.

## Sampling, labeling, and handling
- Sampling cadence: weekly collection, typically on Wednesdays at 0900 GMT; bottle changes performed with clean components.
- Volume and chemistry determination: measure precipitation volume by weight, then analyze unfiltered water for conductivity, pH, and major ions; filtered analyses follow specified protocols.
- Labeling: samples identified by ECN Measurement Code (PC), Site ID, Location Code, and Sampling Date; include recording codes for potential disturbances (insects, dust, bird droppings, fires, etc.).
- Chain of custody and transfer: data accompany results to ECN database; site records and disturbances logged on field forms.

## Data structure, recording conventions, and standards
- Core measurement: precipitation chemistry (PC) with weekly variables recorded per site.
- Key identification fields (required in all datasets):
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date/Time (GMT)
- Recorded variables and units (examples):
  - Sampling time, Volume (ml)
  - pH, Conductivity (µS cm^-1, with precision)
  - Alkalinity (mg L^-1)
  - Major ions: Na+, Ca2+, Mg2+, Fe2+, Al3+, NH4+-N, Cl-, NO3--N, SO4--S, PO4- -P
- Data quality and transfer:
  - Data transfer documentation specifies dataset formats; restricted access via Site Managers’ extranet.
  - Recording precision is defined for each parameter (e.g., 3 significant figures for many ions).
- Volume and flux calculations may use nearby weather station data for more accurate precipitation volumes, due to bulk collector limitations.

## Quality assurance and references
- QA procedures follow established networks (e.g., Acid Deposition Monitoring Network) and include assessment of sampling, handling, and analytical errors.
- Key references include documentation on UK precipitation networks, collector design, and QA standards.

## Appendices (summary)
- Appendix I. Routine sample collection
  - Required field items and steps for bottle/change, funnel handling, contamination checks, and leakage prevention.
- Appendix II. Equipment details
  - Full assembly components, spare parts, and recommended site provisioning (three funnel assemblies, bottles, and filters per site).
  - Supplier information and recommended funnel size (primarily 152 mm).

## Additional notes
- The protocol emphasizes meticulous labeling, contamination avoidance, and secure sample handling to ensure data suitability for spatial analyses and long-term GIS datasets.