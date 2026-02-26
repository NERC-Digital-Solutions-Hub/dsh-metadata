# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

- Background
  - Data collected by Robin Curtis for his PhD fieldwork.
  - Vegetation cover estimates from 54 sites in southern England, all part of the UK Butterfly Monitoring Scheme (UKBMS).
  - Sites dominated by semi-natural grassland.

- Experimental design & data collection
  - Surveys conducted in summer 2008–2009, mainly August.
  - Used UKBMS transect structure to determine quadrat locations; transects divided into 1–15 sections (mean 7.5).
  - Four 1 m² quadrats per section, totaling 1,624 quadrats (54 sites × mean sections × 4).
  - Quadrat positions chosen at random from a 10 m wide polygon centered on the transect route.
  - For each quadrat: recorded percent cover of plant species; counted flower heads and florets, and the subset that were inflorescent.
  - Average of 10.3 plant species per quadrat; 16,720 plant-abundance estimates across 165 plant species.
  - Site-level aggregation yields 2,934 plant:site combinations; mean 54.3 plant species per site.
  - Vegetation structure recorded as percent cover in four categories: Bare ground, grass, herbaceous, woody vegetation; also percent cover of dung.

- The dataset
  - Two files: Vegetation.csv and Quadrats.csv.

- Vegetation.csv
  - Contains 16,720 vegetation-cover estimates.
  - Key columns:
    - Taxon.name (Latin binomial)
    - Common.name (English common name)
    - Site.name (UKBMS transect route name; matches Quadrats.csv)
    - BMS.ID (unique transect ID)
    - Section (section number within transect)
    - Date (date quadrat was sampled)
    - QuadratNum (quadrant replicate within the section)
    - %Cover (percentage cover of the plant)
    - FH (number of flower heads)
    - FI (number of florets)
    - Fl_I (flower heads that are inflorescences)
    - Fl (number of florets on inflorescences)

- Quadrats.csv
  - Contains information about the 1,624 quadrats.
  - Key columns:
    - Site.name (UKBMS transect route name)
    - BMS.ID (transect ID)
    - GRIDREF (Ordnance Survey grid reference for site centroid)
    - LATITUDE, LONGITUDE (coordinates)
    - Date (sampling date; matches Vegetation.csv)
    - Section (section within transect)
    - QuadratNum (quadrant replicate within the section)
    - Aspect (slope direction in degrees, rounded to 5°)
    - Slope (slope angle, nearest 5°)
    - Unevenness.cm (elevation range within quadrat)
    - Distance (distance from ground to base of crown)
    - Av.Turf.Height
    - %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung (percent covers)

- Data relationships and usage notes
  - Vegetation and Quadrats files are linked by Site.name, BMS.ID, Section, QuadratNum, and Date.
  - Site-level summary: ~54.3 plant species per site; quadrat-level average ~10.3 species per quadrat.
  - Temporal and geographic scope: 2008–2009, southern England; vegetation dominated by semi-natural grasslands.
  - References for methodology:
    - Carey et al. (2008) UK Headline messages from 2007.
    - Shimwell (1972) vegetation description and classification.

- Potential analyses for analysts
  - Examine correlations between vegetation structure (BareGround, Grass, Herbaceous, Woody) and plant-species richness or composition.
  - Model relationships between flower-head/floret metrics and species abundance or diversity.
  - Explore spatial patterns using LATITUDE/LONGITUDE and GRIDREF to relate vegetation cover to location.
  - Integrate with UKBMS butterfly data to assess how vegetation structure relates to butterfly abundance or diversity.
  - Compare within-site and cross-site variability in vegetation cover and floral resources.

- References
  - Carey, P. D., et al. (2008). Countryside Survey: UK Headline messages from 2007.
  - Shimwell, D. W. (1972). The description and classification of vegetation.