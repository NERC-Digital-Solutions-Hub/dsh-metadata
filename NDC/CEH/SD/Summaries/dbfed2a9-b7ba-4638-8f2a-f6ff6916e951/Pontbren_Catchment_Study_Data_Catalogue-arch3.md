# Pontbren Database Catalogue

## Overview and Purpose
- Describes the Pontbren Database and the instrumentation used to generate its data.
- Establishes a framework for data organization, description, quality assurance, and sharing.
- Structures files/directories to support data governance, traceability, and reuse for environmental monitoring and policy evaluation.
- Appendices provide supplementary QA codes, borehole and neutron log data, and field diaries.

## Data Organization and Access
- Data stored in directories following a defined framework; QA-coded data flagged in files.
- Most data are in .txt format, typically split into January–June and July–December blocks.
- Filenames indicate the covered dates; appendices offer metadata context (QA, logs, diaries) to aid users.
- Emphasis on data provenance, traceability, and readiness for reuse by policymakers and researchers.

## Data Content by Site and Data Type
- Automatic Weather Station (AWS) at Bowl site: 1-minute sensor sampling; outputs include daily and 10-minute averages; variables include radiation, wind, temperature, humidity, net radiation; 2009 sensor updates added new humidity/temperature columns.
- Bowl site runoff and soil water tension: weir boxes and tipping buckets for runoff; flow estimates in L/s; evaporation can affect readings; data quality varies by method.
- Groundwater (boreholes): five monitoring locations with Diver barometric-transducer systems; water height and groundwater temperature; sampling intervals range from 10 to 30 minutes; borehole details logged in appendices.
- Hillslope (tree shelterbelt) runoff and soil tension: weir-derived runoff data; tensiometers at multiple depths; central loggers; data gaps due to rodent damage noted.
- Llyn Hir site: soil water tension at various depths; tensiometer arrays; varying sampling frequencies.
- Land use manipulation plots: Grazed, Ungrazed, and Trees treatments with replicates; tensiometer readings at multiple depths; overland flow measurements within plots; detailed layout information.
- Neutron probe soil moisture: profiles from bowl, hillslope, plots, tree areas, and Llyn Hir; measurements to ~120 cm depth with site-specific calibration equations.
- Rain gauges: tipping bucket and storage gauges across multiple Pontbren locations; rainfall reported as mm/day.
- Field diaries: Word documents capturing field notes, issues affecting interpretation.
- Streamflow: multiple gauging sites (Sites 1–9, 13; others using different methods); Starflow bed-mounted acoustic Doppler instruments provide stage, velocity, depth, temperature, etc., with site-specific calibrations; some sites use alternative methods (depth/velocity, v-notch weirs).

## Quality Assurance and Metadata
- Appendix A outlines QA codes for data quality and sub-systems (tensiometers, tipping buckets, weirs, groundwater, Starflow, etc.), plus field issues and data-specific problems (rodent damage, debris, calibration drift).
- Appendices B–D contain borehole logs, neutron probe logs, and additional field data logs detailing equipment, methods, geologic descriptions, depths, and datum references.
- Field diaries and calibration notes accompany datasets to enhance interpretation and traceability.

## Calibration, Processing, and Site-Specific Details
- Streamflow calibration: Starflow outputs calibrated against manual spot measurements using site-specific linear relationships (y = αx + β); very low flows are considered unreliable for calibration (<50 mm depth).
- Neutron probe moisture: uses calibration parameters (e.g., α ≈ 0.96, β ≈ -0.01) based on clay calibration; site-specific adjustments for soil layers (peats, etc.); data include raw counts (soil, shield, water) to derive volumetric moisture.
- Groundwater: barometric corrections applied; logs include depth, soil description, and completion details to support interpretations.

## Notable Considerations for Monitoring Frameworks
- Data completeness and accessibility: extensive datasets exist across sites and data types, but some are patchy or compromised (rodent damage, calibration issues, low-flow unreliability).
- Metadata and governance: gaps in metadata (e.g., contributing drainage area) can hinder reuse; public-data-sharing requirements may pose barriers; governance processes are in place or implied to ensure storage, sharing, and updates.
- Data transformation and communication: diverse formats/units/depths require normalization for cross-site comparisons; communicating complex site-specific calibrations and quality flags is a challenge.
- Data provenance and standards: emphasis on data governance, open data considerations, QA flags, and documentation to support transparency and reproducibility.

## End Notes
- The Pontbren Database Catalogue consolidates diverse environmental monitoring data from multiple sites and instruments.
- Provides a structured, well-documented approach to data storage, quality assurance, metadata, and calibration to enable informed monitoring, policy evaluation, and future decision-making.
- Highlights provenance, site-specific considerations, and the ongoing need for data governance to maximize data utility.