# Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017

## Overview
- A dataset and methodology to quantify airborne pollen from nine grass species in the UK during 2016 and 2017 using quantitative PCR (qPCR).
- Aimed at informing environmental health monitoring and decision-making through species-specific pollen abundance data.

## Data access and licensing
- Data are available under the Open Government Licence.
- Access: https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925
- Required citation: Brennan, G.; Creer, S.; Griffith, G. (2020). Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017. NERC Environmental Information Data Centre. Dataset. https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925

## Data collection and methods
- Technology: Data collected using qPCR on air-derived DNA (QuantStudio 6 Flex Real-Time qPCR). Species-specific ITS2 primers targeted multiple common UK grasses.
- Target information: Nine grass species and related genera, with one degenerate probe that could not discriminate species.
- Sampling equipment: Burkard Automatic Multi-Vial Cyclone Samplers (air intake 16.5 L/min) collecting aerial particles into 1.5 mL vials.
- Sampling locations and timing:
  - 13 sites across the UK, on exposed rooftops (4–6 floors high) to sample representative mixed air flow.
  - Sampling aligned with Met Office Pollen Monitoring Network.
  - 2016 sampling: 25 May–28 August; 2017 sampling: 5 May–10 September.
  - Bangor site included, with methodology matching the Met Office network.
- Research sample scope: Aerial particles including pollen; samples were restricted to plant-derived material.

## Sampling strategy and data structure
- Geographic coverage: Sites chosen to represent broad geographic areas with diverse soils and land use.
- daily pollen context: Each sampling unit operated alongside a seven-day Burkard pollen trap to provide daily pollen counts.
- Data organization: Data stored in a file named qPCR_copy_number_abundance_data_aerial_DNA.csv; Table 1 describes headers and data structure.
- Data columns include:
  - Sample identifiers (qPCRID, Site, Target.Name, ID)
  - Temporal scope (start.date, end.date, number.of.days.pooled, year)
  - qPCR metrics (Y.Intercept, R^2, Slope, Efficiency)
  - Quantitative outcomes (Quantity.Mean, Quantity.SD, Quantity.var, Quantity.SE)
  - qPCR CT metrics (CT.Mean, CT.SD, CT.var, CT.SE)
  - Sample timing (day-month, year-month)
  - Location coordinates (Lat, Long)
  - Sampling progression (MaxPoaceaeConc, number.of.days)

## Data processing, quality control and reproducibility
- Data exclusions and quality criteria:
  - From 1,400 daily aerial samples, 1,210 advanced to downstream molecular analysis.
  - Excluded when pollen extraction failed due to rainwater, qPCR efficiencies outside 85–115%, high replicate variability (>6.95 in upper quartile range), or extreme CT cycles (<10 or >38) to minimize false positives/negatives.
- Data reliability: Positive and negative controls used to assess reproducibility.
- Randomization:
  - DNA extractions randomized for Bangor samples.
  - qPCR data collected on a single plate with randomization to avoid batch effects.

## Data governance and usage
- Data were prepared with attention to metadata availability and data sharing standards.
- Metadata completeness and standardization issues (e.g., incomplete metadata) are acknowledged as potential barriers in broader use.
- The dataset emphasizes openness, data provenance, and clear reporting through standardised headers and documentation (Table 1 description included).

## Endnotes for monitoring framework relevance
- Demonstrates practical workflow for environmental health monitoring: from data collection and sampling design, through molecular analysis, to quality control and transparent data sharing.
- Highlights common challenges identified by monitoring framework authors, including data accessibility, metadata quality, data transformation needs, and governance requirements for data to be usable in policy and decision-making.