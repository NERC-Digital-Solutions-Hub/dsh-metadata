# NPPMF_CropPollinationPilot_2015_TransectData_SupportingInformation

- Overview
  - Data on insects observed visiting flowers of three crops: apples, field beans, and oilseed rape.
  - Collected from 13 flowering crop fields by teams at the University of Reading and the James Hutton Institute (Scotland) in 2015.
  - Involves mixed-ability recorders (novice to expert farmers/agronomists) and varying sampling coverage across transects and days.

- Field sampling design and protocol
  - Transect surveys conducted along 50 m straight transects in each field, over a 10-minute period.
  - Observers recorded all flower-visiting insects within a moving observation area 1 m ahead and 1 m to the side.
  - At each field site, 4 transects were surveyed by different recorders.
  - Weather data collected with a Kestrel weather recorder before each transect or once per survey day.

- Crop-specific measurements
  - Oilseed rape and beans: floral density estimated by counting plants per m^2 at three locations along the transect; flowers per plant counted on 5 plants at each location to estimate total flowers per m^2.
  - Apples: density estimated by counting trees along the transect and measuring flowers on 3 trees; density extrapolated to the total number of trees on the transect.

- Data structure and main variables
  - Crop, Site (RD = Reading team, JHI = James Hutton Institute), Date, Recorder (unique code), Recorder type (Novice, Researcher, Farmer/Agronomist).
  - Transect, Start time, Finish time, Temp C, Av wind mph, Max wind mph, Cloud %.
  - Flowers/m2 (flowers per m^2 along transect), Flowers/transect (Flowers/m^2 × 50 for beans/oilseed; for apples: flowers per tree average × trees per transect).
  - Pollinator counts by taxa:
    - Honeybee
    - Bombus species (e.g., B. terrestris/lucorum, B. hortorum, B. pratorum, B. pascuorum, B. lapidarius, unknown/unidentified)
    - Andrena sp.
    - Helictid sp.
    - Solitary bee unknown/unidentified
    - Hoverfly unknown/unidentified
    - Other Diptera
    - Butterfly
    - Moth
    - Coleoptera
    - Other invertebrate
  - Quality Assurance: No specific QA performed.

- Data collection considerations and variability
  - Data collected by diverse recorders, including novices, researchers, and farmers/agronomists; not all recorders sampled all transects or all days.
  - Temperature, wind, and cloud data may be missing (NA) or recorded at different frequencies (per transect vs. per day).
  - Some inconsistencies in naming (e.g., repeated or misspelled taxa entries) and variable sampling across crops.

- Key limitations to consider in analyses
  - Scale and comparability: combining data across crops, sites, recorders, and days may require harmonization of methodologies and units.
  - Missing or uneven data: NA weather fields and incomplete transect coverage can bias results if not properly handled.
  - Taxon identification: potential misidentification or unidentified taxa, especially among non-honeybee/ non-bumblebee groups.
  - Variability in recorder expertise may influence detection and counting of pollinators.

- Potential analyses and research questions
  - Correlations between floral density (Flowers/m2) and pollinator visitation rates across crops.
  - Effects of weather variables (temperature, wind, cloud cover) on pollinator activity and flower visitation.
  - Differences in pollinator assemblages among crops (apples vs beans vs oilseed rape) and sites.
  - Influence of transect-level factors (start time, duration, observer) on recorded pollinator counts.
  - Development of predictive models linking floral density, weather, and crop type to visitation metrics and flower-level pollination potential.

- Provenance and accessibility
  - Data assembled from two institutions (University of Reading; James Hutton Institute) across 13 field sites.
  - Metadata includes site codes, recorder identifiers, and sampling details to support traceability and potential replication.