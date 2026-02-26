# Abstract and lineage Nant Esgair Garn catchment - 20 year derived statistics of rainfall, streamflow and acidity

- Overview
  - A dataset of 20-year derived monthly statistics (April 1982 – April 2013) for Nant Esgair Garn catchment near Llyn Brianne, Wales, UK.
  - Focus on rainfall, streamflow, and stream acidity (pH) associated with a stream gauging station and a nearby water quality station.
  - 2013 observations at 15-minute resolution were used to develop dynamic models that generate the 20-year daily records, from which monthly statistics are derived.
  - Purpose: to understand long-term controls on aquatic biodiversity; data lineage is documented; IP rights vetted.

- Data lineage and modelling approach
  - Observations: daily rainfall, streamflow, and pH for 2013 used to identify model structures with CAPTAIN Toolbox (Matlab) using the RIVC algorithm.
  - Modelling: daily rainfall-to-streamflow and rainfall-to-pH models identified and used to simulate daily streams and pH data from 1982–2013; monthly statistics derived from these simulations.
  - Software: Matlab R2013; CAPTAIN Toolbox; LSIM routine for simulation.
  - Supporting documentation contains full site and lineage details; outputs and data rights vetted by NERC EIDC; code and methods outlined.

- Experimental design and site context
  - Nant Esgair Garn experimental catchment (LI6) near Llyn Brianne, Powys, Wales.
  - Contributory areas: 0.573 km2 (streamflow gauging) and 0.690 km2 (downstream pH monitoring).
  - Geology and soils: Lower Palaeozoic shales, mudstones, greywackes, grits; Podzols and Histosols; catchment historically moorland and improved pastureland.
  - 2013 field data collected at 15-minute intervals using a trapezoidal flume for streamflow and differential pH sensors, installed and maintained by Lancaster University.

- Data sources and data provenance
  - Rainfall: monthly values from 1 Apr 1982 to 1 Apr 2013, compiled from Welsh Water Authority, National Rivers Authority, and Environment Agency Wales; gaps infilled using nearby raingauges.
  - Temperature: monthly values from Felindre weather station; original data from Met Office MIDAS archive.
  - NAO index: monthly values from public data source.
  - All environmental information published via the Environmental Information Data Centre (IPR vetted).

- Data structure and content
  - Format: a single CSV file with 159 columns (columns 2–5 intentionally blank) and 32 rows.
  - Rows: statistics for the first day of each month from 1 Apr 1982 to 1 Apr 2013.
  - Key variable types (examples among many)
    - Rainfall: mean, 10th percentile, total, maximum, coefficient of variation; various estimation periods (365 days, 120 days).
    - Temperature: mean, min/max, range, CV, growing season metrics, high/low pulse durations.
    - NAO index: seasonal estimation period.
    - River flow: mean, percentiles (10th, 95th), moving-average-based metrics, total/maximum/minimum flow, flow range and CV.
    - pH: mean, percentiles (10th, 95th), moving-average metrics, min/max, range, CV.
    - Pulses and growth metrics: number and duration of high/low pulses, average rise rate, etc.
  - The dataset is intended to support long-term trend and biodiversity-related analyses.

- Quality control and data handling
  - Data from CR1000 loggers checked for erroneous values (e.g., power-related glitches) and corrected to NaN where appropriate.
  - Data quality assurance was performed during time-series derivation.

- Access, rights, and references
  - Data released via the Environmental Information Data Centre (EIDC); IP rights vetted.
  - Related literature: Jones and Chappell (2014); Jones, Chappell and Tych (2014); CAPTAIN toolbox methodology references.
  - Contact: Dr Nick A. Chappell, Lancaster University.