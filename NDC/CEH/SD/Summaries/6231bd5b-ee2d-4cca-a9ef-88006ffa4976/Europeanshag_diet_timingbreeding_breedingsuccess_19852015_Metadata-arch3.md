# JAE_Keogan_Europeanshag_phenologymismatch

## Overview
- Datasets designed to examine phenology mismatch for European shag in relation to environmental drivers (SST) and prey availability (sandeels).
- Comprises three linked datasets (shag, diet, and bivariate) to support monitoring, evaluation, and policy-informed decision-making on environmental health indicators.

## Datasets and key variables

- Shag dataset (JAE_Keogan_Europeanshag_phenologymismatch_shagdataset)
  - year: calendar year
  - laydate: first egg lay date (day of year)
  - chicks.fledged.first: number of chicks fledged in the first clutch
  - failedeggsfirst: number of failed eggs in the first clutch
  - Mean.Lay: average lay date in the year
  - relative.lay: nest lay date relative to annual mean lay date (in days)
  - SST.past: average February/March sea surface temperature in year - 1
  - SST.present: average February/March SST in current year
  - pop.size: population size (breeding pairs)
  - yearcentre: year centered around the study period average
  - chicks.fledged.all: total chicks fledged from all clutches
  - failedeggsall: total failed eggs from all clutches

- Diet dataset (JAE_Keogan_Europeanshag_phenologymismatch_dietdataset)
  - Year: year
  - Date: sample collection date (day of year)
  - Age: chick or adult
  - SST: average February/March SST in current year
  - yearcentre: year centered around study average
  - meandate: average date of sample collection in the year
  - datediff: sample collection date centered around annual mean
  - SE1:SE0_proportion: proportion of 1+ sandeels relative to all sandeels in the sample
  - logitSE1:SE0: logit-transformed proportion

- Bivariate dataset (JAE_Keogan_Europeanshag_phenologymismatch_bivariatedataset)
  - Year: year
  - Species: shag or sandeel
  - chicks.fledged: number of chicks fledged
  - failedeggs: number of potential failed eggs
  - sandeelproportion: proportion of 1+ sandeels relative to all sandeels in sample
  - dayofyear: day of laying (shags) or day of sample collection (sandeels)
  - Mean.Lay: average lay date in each year
  - Relative: day of year (lay date or sample date) centered around average lay date

## How the data supports monitoring and policy decisions
- Enables assessment of timing mismatches between breeding phenology and environmental drivers/prey availability.
- Facilitates tracking of reproductive success (chicks fledged, egg failure) in relation to SST trends and prey proportions.
- Supports integration of ecological indicators into monitoring frameworks to inform management actions and policy adjustments.

## Data governance, quality, and accessibility
- Emphasizes the need to verify and harmonize metadata, often by contacting dataset originators.
- Highlights barriers to open data sharing, including the requirement to publicly share underlying datasets.
- Calls for data quality assurance, cleaning, transformation, and transparent presentation of findings (reports, charts, dashboards).
- Recommends establishing data governance processes to ensure datasets meet standards, remain up-to-date, and are storable and shareable.

## Challenges and barriers for monitoring frameworks
- Lack of data or data of insufficient quality.
- Limited data access or delays in receiving data.
- Institutional silos hindering data sharing across organisations.
- Open data requirements conflicting with data ownership or sensitivity.
- Insufficient metadata hindering verification of suitability for use.
- Data formats requiring substantial transformation to be usable.
- Communicating complex findings clearly to policymakers and stakeholders.

## Implications for monitoring framework design
- Develop robust metadata standards and data-sharing agreements to reduce access barriers.
- Invest in data governance, data cleaning, and interoperability to enable timely, transparent reporting.
- Foster cross-organisation collaboration to overcome silos and align on indicators (phenology, SST, prey availability, reproductive success).
- Ensure outputs (reports, dashboards) clearly translate complex ecological signals into actionable policy insights.