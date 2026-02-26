# Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014

- Overview
  - Study collects habitat data across a restoration gradient (intense/reference, restoration/creation, pristine) for grassland, moorland/heathland, woodland/orchard within South West England.
  - For each habitat type, three locations (one of each habitat) are selected within a 2 km radius, across multiple sites.
  - Habitat-option codes reflect agri-environment schemes (e.g., HK7).

- Experimental design
  - Each site includes three habitat types (grassland, heathland/moorland, woodland/orchards, plus Culm variants) mapped to the restoration gradient.
  - The gradient designates Reference (control), Restoration/creation, and Pristine states with specific option types.
  - Locations are chosen to represent the land-use type within a 2 km radius.

- Sampling regime
  - Within each site, a representative 50 × 50 m plot is surveyed.
  - Survey path: zig-zag along a central line with 25 m offset sampling points on each side.
  - Data collected:
    - Vascular plant and bryophyte percent cover in five quadrats along the line.
    - Abundance of vascular plants and bryophytes across the entire plot using the DAFOR scale.
    - Sward height measured at five locations per plot using two methods: direct measure and drop disc.
  - Data recording: on paper forms, then entered into an Access database via a purpose-built form.

- Data structure
  - Two main data files:
    - SWHabitatData.csv (quadrat data)
    - SWSwardData.csv (sward height data)
  - Linking keys: SiteID and LocationID.

- Nature and units of recorded values
  - SWHabitatData.csv includes:
    - SiteID (numeric), LocationID (numeric), Option (text), HabitatType (text), OptionType (text), SurveyDate (date), QuadratSize (text, in metres), SpeciesName (text), Dafor (text), Cover1–Cover5 (percent, numeric)
    - Notes: Blank cover indicates absence in that quadrat; null Dafor indicates not recorded (caution in interpretation)
  - SWSwardData.csv includes:
    - SiteID (numeric), LocationID (numeric), Option (text), HabitatType (text), OptionType (text), SurveyDate (date), Method (text: direct or drop disc), SwardHeight (numeric, cm)
  - Data caveats:
    - Some SiteIDs and LocationIDs are missing in certain files (e.g., SiteID 39 in habitat data; 31, 39, 65, 89 absent in sward data; LocationIDs 18, 32, 88, 121 missing in sward data).

- Quality control
  - Data collected by experienced botanical surveyors.
  - Checks for anomalous values (e.g., >100% cover) and cross-checked against original recording sheets with corrections as needed.

- Data reuse and citation
  - Licensed under the Open Government Licence (OGL).
  - Citing guidance: Peyton, J.; Nuttall, P.; Gerard, F.; Pywell, R.F. (2017). Habitat data from grassland, moorland and woodland restoration sites in South West England in 2014. NERC Environmental Information Data Centre. https://doi.org/10.5285/110199cf-245e-4fa8-a9ca-386657b5fe20