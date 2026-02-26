# Physical, chemical and biological data from peatland ponds, Pennines, UK, 2012-2014

## Overview
- A dataset comprising biological (invertebrate abundances) and physical/chemical measurements from peatland ponds in the Pennine hills, northern England, collected 2012–2014.
- Data used in the study Beadle et al. Landscape-scale peatland rewetting benefits aquatic invertebrate communities (Biological Conservation; in press).
- Biological data: invertebrate taxa abundances (species-level where possible; Chironomidae may be sub-sampled when abundant).
- Physical data: pond location, altitude, aspect, and morphometrics.
- Chemical data: dissolved ions, pH (with occasional measurements), and various solutes.

## What has been recorded and in what form
- Biological data: invertebrate abundances per pond ( taxa listed as columns in CSVs).
- Physical data: coordinates, location details, altitude, aspect, pond morphometrics (long/short axis, perimeter, volume, depth).
- Chemical data: dissolved oxygen, temperature, pH, total nitrogen, total phosphorus, dissolved organic carbon, aluminum, iron, silica, and other solutes.
- Data are stored in four CSV files with structured columns and pond-identifiers to link datasets.

## Where and when data were collected
- Location: peatland ponds in the Pennine hills, northern England (specific sites listed in the dataset).
- Study sites include six peatlands for a chronosequence and additional naturally-formed ponds in 2012; total ponds sampled: 105.
- Sampling period: 2012–2014, with regular bi-monthly visits (04/2013–06/2014 for the chronosequence; 07/2012 for naturally-formed ponds).

## How data were collected
- Biological sampling: 3-minute macroinvertebrate sampling per pond across mesohabitats (open water, floating vegetation, littoral vegetation, bottom sediments), plus 1 minute for surface-dwelling taxa; specimens preserved in 70% ethanol and identified (species level where possible); Chironomidae sub-sampled when abundant.
- Field measurements: distance and depth measurements; GPS-based coordinates; on-site visual estimation of vegetation cover; water column measurements of DO, temperature, and pH (on-site with portable meter).
- Laboratory analyses: filtered water samples analyzed for TN, TP, DOC, Al, Fe, Si using appropriate instruments (Analytikjena multi N/C 2100, San++ analyzer, ICP-OES).
- pH sensor failure: month 12 pH values missing and imputed using the established relationship with [Mg] (r = 0.81).

## Study design and site characteristics
- Chronosequence: Moor House National Nature Reserve, with random pond sampling along ditches; ponds were disturbed and marked due to small size; at least five ditches per visit, one pond per ditch.
- Chronosequence sampling: from 06/2013 to 06/2014 (ages 0.5–2 years in 2013; older in 2014); two-monthly visits.
- Additional sites: six peatlands for chronosequence; twenty naturally-formed ponds across four peatlands (07/2012); natural ponds sampled where landowner access permitted.
- Site metadata recorded: location, altitude, aspect, pond dimensions (long/short axis, perimeter), volume, age, and restoration status where applicable.
- Total ponds: 105 across all study sites.

## Data structure and formats (files)
- Four CSV files containing linked datasets:
  1) Chron_nat_inverts.csv — 82 columns; pond code as first column; site codes; invertebrate taxa abundances per pool.
  2) MH_inverts.csv — 45 columns; pond code as first column; invertebrate taxa abundances per pool.
  3) Chron_natural_physical_chemical.csv — 26 columns; fields include pond code, location, sampling date, pond age, coordinates, aspect, elevation, pond dimensions, volume, temperature, DO, pH, and dissolved solutes (T-Y).
  4) MH_physical_chemical.csv — 26 columns; detailed pond measurements (pond code, location, date, pond age, OS Grid reference, easting/northing, aspect, elev, mindepth, maxdepth, meandepth, longaxis, shortaxis, perimeter, volume, temp, do, ph, tn, tp, doc, al, fe, si, vegcover) with units and methodology notes.
- Data identifiers and structure:
  - Pond codes include site abbreviations (e.g., MHC for Moor House Chronosequence) and denote pond numbers.
  - Naturally formed ponds are prefixed with n (e.g., nWFN01).
  - Clear cross-referencing between invertebrate and physical/chemical datasets via pond codes.

## Data quality, completeness, and governance
- Completeness: dataset described as complete; one noted pH value was missing and imputed from a statistical relationship with magnesium concentration (r = 0.81).
- Quality control:
  - Macroinvertebrate identifications verified by independent experts.
  - Field sensors (DO, temperature, pH) calibrated before each visit.
  - Laboratory equipment for solutes calibrated with standards beyond the sample range.
- Provenance and documentation: full sampling methodology and site details are described in Beadle et al. (in press); data files reference this publication for complete methodological context.
- Governance considerations for reuse:
  - Metadata present across files to enable data discovery, linking of biological and physico-chemical measurements, and reproducibility.
  - Clear pond identifiers and site metadata support data integration and provenance tracking.
  - Data are suitable for analyses of community structure, temporal changes, and relationships between physico-chemical variables and ecological communities, with attention to restoration status and chronosequence design.
  
## Publication and provenance
- Primary methodology and full details are described in Beadle et al., Landscape-scale peatland rewetting benefits aquatic invertebrate communities (Biological Conservation, in press).
- Data are provided as structured CSVs with explicit units, methods, and field protocols to support reuse and governance in data stewardship contexts.