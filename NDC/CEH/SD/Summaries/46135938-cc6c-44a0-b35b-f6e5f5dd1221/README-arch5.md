# Supporting document for 'Reservoir inflows and release data, and optimised monthly rule curve ordinates (upper, lower and critical) for Pong and Bhakra reservoirs in Northern India' data

## Overview
- Provides supporting data for research on reservoir operation for the Pong and Bhakra reservoirs in Northern India.
- Contains time series for reservoir releases (including spills), evaporation loss, and rule curves.
- Rule curves indicate target storage levels to be maintained monthly to meet demand.

## Data Files and Contents
- ReservoirData.csv
  - Monthly data for Pong and Bhakra: inflows, net-evaporation loss, and releases.
  - Units: million cubic metres (x 10^6 m^3).
  - Temporal coverage and scenarios:
    - Baseline: 1989–2008
    - Mid-century: 2032–2050
    - End-century: 2082–2100
  - Future inflows produced by WEAP model forced with climate projections from the GFDL-CM3 CMIP model.
- RuleCurve.csv
  - Optimised rule curve ordinates (x 10^6 m^3) for Pong and Bhakra:
    - Smax: Maximum storage level (reservoir capacity)
    - URC: Upper Rule Curve (monthly targets)
    - CRC: Critical Rule Curve (monthly triggers for water rationing)
    - LRC: Lower Rule Curve (monthly targets)
    - DS: Dead storage
  - Includes associated reservoir rationing ratios to apply to gross demand when rationing occurs.
  - When rationing is triggered, release towards demand is capped at RR * D, where RR is the rationing ratio and D is the gross demand for the period.

## Variables, Units, and Definitions
- Inflows, releases, and evaporation (ReservoirData.csv):
  - Measured in million cubic metres.
  - Monthly time series for each reservoir and period.
- Rule curve ordinates (RuleCurve.csv):
  - Smax, URC, CRC, LRC, DS in million cubic metres.
  - Monthly (January–December) storage targets and capacities.
- Rationing mechanics:
  - RR (rationing ratio) applied to gross demand D to cap releases when rationing is triggered.

## Temporal Coverage and Scenarios
- Baseline period: 1989–2008
- Mid-century projection: 2032–2050
- End-century projection: 2082–2100

## Modelling and Provenance
- WEAP (Water Evaluation And Planning) model used to generate future inflows.
- Climate forcing for future inflows: GFDL-CM3 CMIP projections.
- Data prepared to support assessment of reservoir operation and rule curves under climate and demand changes.
- Authors: Dau, Q and Adeloye, A.J. Corresponding author: a.j.adeloye@hw.ac.uk

## Data Quality and Governance Considerations for Data Stewards
- Metadata should clearly specify units, definitions, and the monthly temporal resolution.
- Document modelling methods and scenarios (WEAP configuration, climate forcing) to ensure reproducibility.
- Maintain provenance: link ReservoirData.csv and RuleCurve.csv to the underlying research publication and model runs.
- Assess and record uncertainties inherent in climate projections and model outputs.
- Ensure versioning and updates if new projections or model runs are added.

## Access, Sharing, and Reuse
- Data accompany the cited research on reservoir operation for Pong and Bhakra reservoirs.
- No explicit licensing in the provided text; verify and attach appropriate data use/license information before sharing or publication.
- Clearly credit the authors and provide contact information for inquiries and data requests.

## Additional Notes for Data Stewards
- Ensure compatibility of data formats with repository standards and data portals.
- Provide guidance on how to interpret the rule curves and rationing logic for potential users applying the data to operational planning.