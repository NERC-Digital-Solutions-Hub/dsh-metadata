# Soil biochemical measurements from saltmarshes of different ages on the Essex coast, UK 2011..

## Aim
- Document soil biochemical properties across a chronosequence of Essex saltmarshes to assess environmental health and changes since tidal restoration or breach.
- Provide standardized data for monitoring environmental condition and policy performance over time.

## Dataset contents (what is measured)
- Bulk density
- Moisture content
- pH
- Electrical conductivity (conductivity)
- Available ammonium (NH4+)
- Total oxidised nitrogen (TON; e.g., NO3-)
- Organic matter content (loss on ignition at 375°C)
- Below-ground biomass to 30 cm depth
- Carbon and nitrogen content (soil C and N percentages)
- Depth: 30 cm soil cores

## Sampling design and scope
- Study sites on the Essex coast: three restored salt marshes and six accidentally breached sites to provide a chronosequence from 16 to 114 years since restoration/breach.
- Natural salt marshes sampled at all sites, plus adjacent fields on former salt marsh where accessible (before time-point reference).
- Temporal scope:
  - Primary sampling: October 2011
  - Tollesbury field samples: July 2010
  - Barrow Hill, Wallasea Island, Brandy Hole field samples: April 2017
  - No repeat sampling planned for most sites
- Spatial details:
  - Grid references and site codes provided for each site
  - Distinct categories: Restored and breached sites; natural marshes; fields on former marsh

## Field and laboratory methods
- Field sampling:
  - Sampling location: permanently vegetated marsh above 1.5 m ordnance datum (OD)
  - Randomly selected sampling locations away from edges
  - 4 cm diameter, 30 cm length soil corers used; 3 cores per sampling location
  - 4 sampling locations per salt marsh; fields on former marsh had 2–6 locations
- Laboratory analyses (per soil core):
  - Core 1: air-dry, grind, sieve <2 mm; determine EC, pH (1:2.5 water suspension), organic matter by LOI at 375°C (16 h), NH4+ and TON by 1M KCl extraction with colorimetric analysis; total C and N by combustion (CN analyzer)
  - Core 2: below-ground biomass to 30 cm via washing, drying at 80°C for 72 h, weighing
  - Core 3: moisture content by weight loss after drying at 105°C
- Calibration and quality control:
  - Calibration of laboratory equipment following CEH Bangor practices
  - Data checking: dataset entered into spreadsheet; screening for outliers
  - Statistical treatment of observations: None reported
- Data formats: CSV files

## Dataset structure and field descriptions
- Primary dataset: Saltmarsh Chronosequence data (2011)
- Secondary dataset: Saltmarsh Chronosequence data (2010–2017)
- Key fields (examples):
  - SiteName, SiteCode
  - BulkDensity, MoistureContent, pH, Conductivity
  - NO3-N (TON), NH4-N
  - OrganicMatter
  - BelowGround
  - Carbon, Nitrogen
  - Other notes: missing data indicated where samples were lost or not analyzed
- File formats: Comma separated values (.csv)

## Site information and spatial references
- Restored and breached sites with grid references and years since breach (to 2011): Tollesbury, Orplands, NortheyMR, Barrow Hill, Ferry Lane (B), Wallasea Island, Northey Island, North Fambridge, Brandy Hole
- Natural salt marsh sites: Tollesbury Natural, Orplands Natural, Northey Natural, Barrow Hill Natural, Ferry Lane (B) Natural, Wallasea Island Natural, North Fambridge Natural, Brandy Hole Natural
- Fields on former salt marsh: Barrow Hill Field, Wallasea Island Field, Brandy Hole Field, Tollesbury Field
- Grid reference data provided for each site (eastings and northings)

## Provenance and references
- Methods references: Avery, B.W., and Bascombe, C.L. 1974; Ball, D.F. 1964 (LOI method)
- Data collection protocols and calibration aligned with Centre for Ecology & Hydrology (CEH) Bangor practices

## Intended use, access, and data stewardship
- Purpose: enable monitoring of environmental health and policy performance over time through standardized, comparable measurements
- Data stewardship: intended to be stored and uploaded to appropriate data portals; datasets are structured for reuse and verification
- Accessibility note: provides detailed site, method, and variable descriptions to facilitate data reuse and cross-site comparisons

## Key considerations for analysts
- Chronosequence design enables assessment of restoration effects on soil biochemistry over time
- Standardised measurement methods support comparability across sites and time
- No planned repeat sampling on most sites; data represent a snapshot with some multi-temporal components (2010–2017 at select sites)
- Missing data acknowledged where samples were lost or not analyzed
- Useful for benchmarking environmental health, restoration outcomes, and potential policy evaluation; underlying data and site coordinates support integrative analyses with other environmental datasets