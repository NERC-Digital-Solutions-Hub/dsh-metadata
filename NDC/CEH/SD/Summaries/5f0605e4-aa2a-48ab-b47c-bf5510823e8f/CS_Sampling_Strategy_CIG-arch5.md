# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Long-running field survey framework for Countryside Survey, linking sampling strategy with the ITE Land Classification.
  - Aims to produce national and country-specific estimates of habitats and land features across Great Britain, with time-series data since 1978.
  - Emphasizes representativeness through stratified, random sampling to reduce bias and enable robust change detection.

- Core data model and classification
  - ITE Land Classification: environmental attributes (altitude, geology, climate, etc.) used to create land classes.
  - Original system (1978): 32 land classes, built from 1 km squares (centre squares of a 15x15 km grid) plus four surrounding squares; 6039 classified squares in total.
  - 1st surveys produced national estimates by combining class area with mean habitat area per square within each class.
  - Evolution of classes: 1984 retained the earlier framework; 1990 extended classification to cover all GB squares (land cover mapping linked to the survey); by 1998 the system expanded to 40 classes; 2000 and 2007 introduced country-specific subdivisions (England & Wales; Scotland) to support Wales-only and Scotland-only reporting.

- Sampling framework and survey history
  - 1978 (Initial Land Classification & Field Survey)
    - 32 classes; 8 squares per class (256 total) surveyed; focus on vegetation, soils, habitat areas.
  - 1984 (2nd Field Survey)
    - 12 km squares per class (384 total); builds on 1978 framework.
  - 1990 (All Squares Land Classification & 3rd Field Survey)
    - Classification updated to cover all GB squares; 508 squares surveyed.
    - Satellite-derived Land Cover Map linked; results published in CS1990 main report.
  - 1998 (Revised Land Classification & 4th Field Survey)
    - Separate reporting for Scotland introduced; number of classes increased to 40.
  - 2000 (Revised Land Classification & 5th Field Survey)
    - UK-wide changes to enable England & Wales, and Scotland country-unit estimates.
    - Sub-divided classes into country-unit versions; added 19 extra squares to improve representation; introduced upland habitat module.
  - 2007 (Further Developments & 5th Survey)
    - Wales-only reporting formalized; five new Welsh country-unit classes (5w, 6w, 7w, 15w, 18w) created; total strata increased to 45.
    - Welsh sample increased to ensure at least 6 squares per Welsh class (increase from 64 to 107 Welsh squares overall for Wales reporting).
    - England sampling adjusted correspondingly; Isle of Man samples removed and replaced (two new English squares introduced).
    - Additional upland sampling module included to improve upland habitat estimates for England and Wales.

- Country units, Wales, and uplands
  - Separate country estimates introduced to improve policy-relevant reporting (England with Wales; Scotland).
  - Welsh-specific sub-division of land classes and increased Welsh sampling to support Wales-only results.
  - Upland module added to CS2000/CS2007 to boost accuracy for upland habitats in England and Wales.

- Data governance, provenance, and notes for data users
  - Data lineage is explicit: successive revisions of the Land Classification underpin sampling design and estimations.
  - Note on national estimates: changing land-class frameworks affects cross-survey comparability; two approaches exist:
    - Use latest classification for GB-wide estimates (preferred for consistency within a survey).
    - Use original 1990 classification for cross-survey consistency.
  - Documentation and maps accompany data (e.g., Figures 1–7 showing classification maps and sampling frames; Tables detailing square counts by class and year).
  - Isle of Man data are handled separately (two IOM squares replaced by two English squares for country-unit reporting).

- Outputs and documentation
  - Outputs include: spatial dataset of sampled squares, land-class assignments, habitat and landscape feature data per square, and national/country estimates of habitat areas.
  - Publications documenting results and methodologies across surveys (CS1990 main report; CS2000 summary; CS2007 Wales reporting; UK results from 2007).

- Practical considerations for data stewards
  - Maintain clear versioning of Land Classification across surveys (32 → 40 → 45 classes; country-unit distinctions).
  - Capture and expose data provenance: year, survey type, classification version, country-unit designation, and upland module inclusion.
  - Ensure metadata includes sampling design (stratified random, per-class sample sizes, changes in class definitions), data processing steps, and lift/downdate rules for estimations.
  - Provide guidance on comparing estimates across surveys, noting the impact of classification updates on comparability.

- Related references and further reading
  - Foundational papers and project reports detailing the development of the ITE Land Classification and Countryside Survey methodologies.
  - Specific CS reports documenting Wales-only reporting preparations and the 2007 UK results.