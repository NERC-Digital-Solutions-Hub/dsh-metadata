# Pontbren Database Catalogue

## Overview
- Designed to identify useful environmental health measures to scrutinise policy outcomes and inform future decisions.
- Aims for reproducibility, data quality, openness, and transparent data governance within a government/research collaboration context.
- Targets monitoring framework authors and policy evaluators responsible for evaluating environmental health monitoring approaches.

## Data Organization and Access
- Data stored in well-described directories; files often in .txt and split into 6-month blocks (January–June, July–December) to manage volume.
- Each data point includes a quality assurance (QA) code; QA details provided in Appendices.
- Supplementary context provided by field diaries and borehole logs to aid interpretation.
- Metadata and site descriptions are embedded; Appendix materials (QA coding, borehole logs, field diaries) support data interpretation.

## Database Framework and Data Domains
- Weather (AWS) data: sensors sampled every minute; daily and 10-minute averages produced; key variables include incident radiation, wind, soil/air temperatures, humidity, net radiation. Post-2009 sensor changes added Humidity and Air Temp columns.
- Bowl study site: runoff and soil water tension data (drainage/runoff via weir boxes and tipping buckets; tensiometers at various depths).
- Groundwater: five boreholes with Diver transducers; barometric correction via BaroDiver; outputs as height above soil surface; includes groundwater temperature.
- Hillslope site: runoff (weir boxes, overland flow) and soil water tension; tensiometers; shelterbelt data.
- Llyn Hir site: soil water tension via tensiometers (0/10/30/50 cm); sampling cadence adjusted over time.
- Land use manipulation plots: four plots with three replicates each; treatments include Grazed, Ungrazed, Trees; tensiometer readings and overland flow data; replication and treatment mapping documented.
- Neutron probe soil moisture: measurements along access tubes (0–120 cm, typically in 10 cm steps); site-specific calibration and plot identifiers (M1–M4).
- Rain gauges: tipping-bucket and storage gauges across multiple sites; data provided as mm/day; storage data in mm.
- Field diaries: Word documents noting field observations and data issues per location.
- Streamflow: 13 gauging sites with various instrumentation (bed-mounted Starflow Doppler, pressure transducers, v-notch weirs); data include stage, velocity, flow, water temperature, instrument status; calibration relationships with manual measurements documented.

## Quality Assurance, Metadata and Standards
- QA coding system (Appendix A) classifies data quality and flags instrument or data issues (e.g., logger faults, sensor problems, interference, calibration concerns).
- Metadata and site descriptions are embedded; borehole logs and field diaries provide contextual information to support data interpretation.
- Neutron probe data include calibration relationships and site-specific notes on material properties (e.g., clay calibrations).

## Data Governance, Openness and Dissemination
- Outputs are designed for public sharing; underlying data are governed to maintain standards, provenance, and reproducibility.
- Public sharing is a stated objective, but barriers include data ownership, privacy, and data management requirements.

## Challenges and Practical Considerations
- Data gaps and variable data quality across sites and instruments (patchy records, calibration issues, accessibility, weather-related interruptions).
- Silos and organizational barriers hinder data sharing and integration across datasets.
- Metadata sufficiency and consistency are critical for reuse and cross-site comparability.
- Data transformation and calibration steps (e.g., calibrations between Starflow and manual measurements) require site-specific documentation.

## Implications for Monitoring Framework Design
- Emphasizes the need for:
  - Clear, machine-readable metadata and documentation for each dataset.
  - Consistent QA coding and logging of data issues to support transparency and reproducibility.
  - Integrated data governance balancing openness with data stewardship and quality assurance.
  - Documentation of calibration and data processing steps to enable traceability and comparability across sites and time.
- Highlights the value of multi-site, multi-parameter monitoring (weather, runoff, soil moisture, groundwater, vegetation manipulation) for evaluating policy interventions and flood/risk management.

## Practical Takeaways for Authors of Monitoring Frameworks
- Use Pontbren as a model for organizing data and metadata to support policy evaluation and decision-making.
- Prioritize structured QA, robust metadata, and transparent governance to enhance data reuse and comparability.
- Plan for data accessibility challenges, data ownership issues, and ongoing data maintenance to ensure long-term utility.