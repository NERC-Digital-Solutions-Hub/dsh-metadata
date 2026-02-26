# Data access, licensing and citation

- Open licensing and access
  - Data are available under the Open Government Licence.
  - Access point: https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925
- Citation requirements
  - When using the data, cite: Brennan, G.; Creer, S.; Griffith, G. (2020). Abundance of airborne pollen for nine grass species, measured by qPCR, UK, 2016-2017. NERC Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/28208be4-0163-45e6-912c-2db205126925

## Data collection and methods

- Molecular assay
  - Data collected via qPCR using a QuantStudio 6 Flex Real-Time qPCR machine.
  - Species-specific primers target the ITS2 region of abundant UK grasses; includes several named species and a degenerate probe unable to discriminate some.
- Data analysis
  - qPCR data analyzed with QuantStudio Software V1.3.
  - Copy numbers quantified using copy number standards (2 to 2×10^5 copies/µl).
- Timing and sampling
  - Seasons: 2016 and 2017.
  - Sampling windows: 25 May–28 August 2016; 5 May–10 September 2017 (dates vary slightly by site).
- Location and sampling design
  - 13 sampling sites across the UK; coordinates provided in the data file.
  - Exposed rooftop locations (4–6 storeys) to capture mixed air flow; away from vents or suppressors to avoid bias.
  - Research samples comprise aerial particles captured with Burkard Automatic Multi-Vial Cyclone Samplers (16.5 L/min) into 1.5 ml vials.
  - Sampling targeted aerial plant-origin particles only.

## Sampling strategy and data context

- Geographic and methodological coverage
  - Sites chosen to cover broad geographic areas and varied soils/land use; aligned with Met Office UK Pollen Monitoring Network requirements.
  - Each site paired with a seven-day Burkard volumetric trap for daily pollen counts; Bangor site used the same methodology despite not being part of the Met Office network.
- Data structure and data file
  - Primary data file: qPCR_copy_number_abundance_data_aerial_DNA.csv.
  - Table 1 provides descriptors for the CSV headers, covering sample identifiers, site, target species, qPCR task, date ranges, and copy number/CT metrics.

## Data quality, exclusions, and quality control

- Data exclusions
  - Of 1,400 daily aerial samples, 1,210 advanced to molecular analysis.
  - Exclusions due to: insufficient pollen extraction from rain-filled tubes.
  - qPCR quality filters: efficiencies outside 85–115% removed; replicate SDs > 6.95 removed; Ct cycles outside 10–38 removed to reduce false positives/negatives.
- Reproducibility and controls
  - Reliability checked via positive and negative controls.
  - Randomization implemented for reproducibility: Bangor samples randomized for DNA extractions; DNA extracts randomized on a single 96- or 384-well plate for qPCR.

## Data management, provenance, and metadata

- Data processing and reporting
  - Data include detailed qPCR metrics per target (e.g., Quantity.Mean, Quantity.SD, CT.Mean, CT.SD, etc.) and standard curve parameters (R^2, Slope, Efficiency).
  - File includes geographic and temporal metadata: site ID, sampling start/end dates, number of days pooled, year, and location coordinates (Latitude, Longitude).
- Data structure details
  - Key columns described in Table 1: qPCRID, Site, Target.Name, Task, ID, start.date, end.date, number.of.days.pooled, year, standard-curve metrics, copy-number statistics, CT statistics, and location info.

## Governance and stewardship considerations

- Accessibility and discoverability
  - Data openly licenced and deposited with a persistent DOI; metadata fields and data headers are described to support discovery and reuse.
- Standards and interoperability
  - Clear reporting of assay design (ITS2 primers, species list), analytical workflow (QuantStudio v1.3), and standard curves; includes quality thresholds for reproducibility.
- Documentation and provenance
  - Comprehensive dataset description, including sampling strategy, site selection, and randomization procedures, to support auditability and future reuse.
- Usage considerations for data stewards
  - Ensure future users understand licensing terms, citation requirements, and the exact data file structure (qPCR_copy_number_abundance_data_aerial_DNA.csv and Table 1 header descriptions).
  - Maintain linkage to sampling context (sites, date ranges, and sampling methods) to enable proper interpretation and reuse.