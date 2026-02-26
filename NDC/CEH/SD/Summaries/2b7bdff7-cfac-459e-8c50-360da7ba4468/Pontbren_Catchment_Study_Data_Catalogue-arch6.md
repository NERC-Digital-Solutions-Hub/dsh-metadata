# Introduction to the DATABASE Catalogue

- Purpose: Describes the Pontbren Database with instrumentation, data collection, and organization to support easy discovery, QA, cleaning, formatting, and self-serve usage of outputs (dashboards, reports, etc.).
- Core emphasis: Data provenance, quality assurance (QA), and the ability to iteratively improve outputs with appendices and field notes.

## Data organization and structure

- Data stored in directories organized by dataset type and site.
- Key folders include: AWS, Bowl study site data, Groundwater, Hillslope study site data, Llyn Hir, Land use manipulation plots, Neutron probe data, Rain gauge data, Field Diaries, and Streamflow.
- Each folder contains subfolders for specific instruments or study components (e.g., tensiometers, runoff boxes, streamflow sites).

## Data types, instruments, and measurements

- Automatic Weather Station (AWS)
  - 1-minute sampling; daily and 10-minute averages.
  - Variables: radiation, wind, temperature, humidity, soil temperature, net radiation, etc.
  - Post-2009 sensor upgrade added Ave Humidity and Ave Temperature columns.
- Bowl study site
  - Runoff data from weir boxes and tipping buckets; drain/overland flow in litres/second.
  - Tensiometers at multiple depths (cm H2O).
- Groundwater monitoring
  - Five boreholes with Diver pressure transducers; barometric correction; water height and temperature.
- Hillslope study site
  - Runoff (overland and drain), tensiometers, tree shelterbelt components, overland-flow traps.
- Llyn Hir site
  - Soil water tension via tensiometers at multiple depths; sampling cadence noted.
- Land use manipulation plots
  - Four sites with Grazed/Ungrazed/Trees treatments; tensiometer arrays and overland-flow data; plot layouts.
- Neutron probe soil moisture
  - Soil moisture profiles across sites and land-use zones; calibration notes and site variations (e.g., peat).
- Rain gauges
  - Tipping bucket and storage gauge data across sites; units in mm/day or mm.
- Field diaries
  - Word documents describing issues affecting data (e.g., equipment problems).
- Streamflow
  - Sites use Starflow acoustic Doppler systems; others use transducers or v-notch weirs.
  - Site-specific calibration equations relate Starflow estimates to manual measurements.

## Data formats, access, and descriptions

- Data files organized into directories with descriptive contents.
- Most data in .txt format; typically split into six-month blocks (Jan–Jun, Jul–Dec).
- Filenames indicate covered date ranges.
- Appendices provide QA coding (Appendix A) and borehole/neutron logs (Appendices B and C).
- Field diaries linked to data issues for anomaly interpretation.

## Quality assurance and metadata

- QA codes annotated on every data point; full codes defined in Appendix A.
- QA covers good data, questionable quality, calibration issues, sensor/logger problems, and site-specific notes (e.g., rodent damage, degassed tensiometers).
- Borehole logs (Appendix B) and neutron probe logs (Appendix C) accompany datasets.
- Field diaries document data issues that aid interpretation.

## Calibration, site-specific considerations

- Streamflow calibration uses site-specific linear relationships (y = αx + β) to align Starflow estimates with manual measurements; parameters documented with uncertainties.
- Neutron probe moisture data rely on established calibration with notes about deviations in certain surface layers (e.g., peat).
- Calibration and site notes are recorded to support accurate cross-site comparisons.

## Notable data issues and challenges

- Patchy data due to environmental factors (e.g., rodent damage to traps) and incomplete sensor operation.
- Variation in data formats, sampling frequencies, and data gaps requiring careful QA and extensive documentation.
- Data consideration gaps within wider teams can affect the time spent understanding the ask and data provenance.

## Purpose, use cases, and impact for data support

- Enables discovery, integration, and cross-site hydrological/environmental analysis.
- Supports the creation of dashboards, pivot tables, and reports for self-service data exploration.
- Comprehensive provenance and QA documentation to promote re-use and transparency.

## Equipment & Methods (illustrative examples)

- Borehole logging and N-probe data collection
  - Hand auger with AQ drill rod/guide tube; pneumatic hammer; CEH involvement.
  - Sites S3 (easternmost, central, westernmost) with labeled N-probe boreholes (NP20–NP23, NP21, NP22, etc.).
  - Grid references and datum levels recorded; logs include soil types, depths (mBGL), completion tubes (16 gauge aluminium), and sample intervals.
  - Date: 14/05/06; multiple sheets detailing depth, soil description, and borehole completion details.
- Groundwater monitoring and field documentation
  - Logs include depth, soil description, sampling intervals, and instrument specifics (aluminium access tubing, borehole logs).
- Appendix D: Streamflow gauging
  - Flow metered spot measurements with start/finish times and flow estimates across multiple sites (Site 4–13, etc.), illustrating cross-site calibration and validation data.