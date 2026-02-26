# Data overview

- Purpose and scope
  - Records of flower species and their estimated abundances on farmland.
  - Study across eight farms in Hampshire and West Sussex, England, UK.
  - Data from two years: May–August 2014 and May–August 2018.
  - One transect of 3 km per farm; transect marked in 2013 by TJW.
  - Transects encompassed diverse habitat types: hedgerows, sown seed mixes for birds/bees, grass margins, and areas left to regenerate.

- Locations and transects
  - Eight farm locations labeled A–H with precise latitude/longitude coordinates provided.
  - Each transect was divided into sections to be walked, with sections retained for both 2014 and 2018 surveys.

- Collection/generation methods
  - Floral surveys conducted along each transect in 2014 and 2018, aligned by rounds.
  - Rounds in 2014: 17–27 May, 21 Jun–9 Jul, 3–15 Aug.
  - Rounds in 2018: 14–19 May, 20 Jun–7 Jul, 3–7 Aug.
  - Each transect section surveyed separately; all sections kept across years.
  - Counts calibrated between surveyors using photographic estimates and a scaling factor.

- Nature and units of record
  - For each transect section: record flower species and the number of open flowers estimated within 2 m on either side of the observer.
  - A flower is counted when fully open and includes singles, umbels/spikes, or capitula.

- Data structure and file
  - Primary data file: FloralResources.csv (an Excel spreadsheet).
  - 11 columns: Year, Round, Type (ELS or HLS), Farm, Label (transect section), What (management type), Length (m), Width (m), Family, Species, Abundance.
  - Key metadata:
    - Year indicates data collection year (2014 or 2018).
    - Round indicates survey round (1, 2, or 3).
    - Type indicates countryside stewardship agreement: ELS or HLS.
    - Length and Width specify the transect section surveyed.
    - Abundance provides the estimated number of open flowers in the section.

- Data quality and utility
  - Quality control via cross-checks between surveyors.
  - Data structured to enable comparisons across farms, habitat types, management (What), rounds, and years.
  - Designed to support subsequent analysis and self-service exploration of flower abundance patterns by species, habitat type, and management regime.