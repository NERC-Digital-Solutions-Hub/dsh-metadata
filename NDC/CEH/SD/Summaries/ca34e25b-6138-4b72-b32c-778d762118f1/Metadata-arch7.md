# Vegetation cover at 54 UK Butterfly Monitoring Scheme sites in southern England, 2008-9

## Overview
- Vegetation cover estimates collected by Robin Curtis as part of his PhD fieldwork.
- 54 sites in southern England, all dominated by semi-natural grassland.
- Sites are part of the UK Butterfly Monitoring Scheme (UKBMS).

## Experimental Design & Collection Methods (GIS context)
- Surveys conducted in summer 2008 and 2009, mainly August.
- UKBMS transect structure used to determine quadrat count/location.
- Transects divided into sections (1–15; mean 7.5); four 1 m² quadrats per section (total 1,624 quadrats: 54 sites × ~7.5 sections × 4 quadrats).
- Quadrat locations chosen randomly from a 10 m wide polygon centered on the transect route.
- For each quadrat: percent cover per plant species; counts of flower heads (FH), florets (FI), and inflorescent heads (Fl_I, Fl).
- ~10.3 plant species per quadrat; 16,720 species-coverage estimates across 1,624 quadrats and 165 plant species.
- Aggregated to site level: 2,934 plant:site combinations; average ~54.3 plant species per site.
- Additional vegetation structure data: percent cover of bare ground, grass, herbaceous, woody vegetation, and percent dung.

## The Dataset
- Two CSV files: Vegetation.csv and Quadrats.csv.

- Vegetation.csv
  - Contains 16,720 vegetation-cover estimates.
  - Key columns: Taxon.name (Latin binomial), Common.name, Site.name, BMS.ID, Section, Date, QuadratNum, %Cover, FH, FI, Fl_I, Fl.

- Quadrats.csv
  - Contains 1,624 quadrats metadata.
  - Key columns: Site.name, BMS.ID, GRIDREF (OS grid centroid), LATITUDE, LONGITUDE, Date, Section, QuadratNum, Aspect, Slope, Unevenness.cm, Av.Turf.Height, %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung.

## Spatial Data & GIS Implementation
- Relationship between files: join Vegetation.csv and Quadrats.csv via Site.name, BMS.ID, Section, QuadratNum, and Date.
- Spatial references available: latitude/longitude (digital degrees) and OS Grid Reference (GRIDREF) for precise site centroids.
- Data structure supports mapping per quadrat and aggregating to sites or transect sections.
- High-level spatial coverage: 54 transects across southern England, with 1,624 quadrats offering fine-grained vegetation data within transect routes.

## GIS Applications
- Map per-quadrat species cover and vegetation structure across the 54 sites.
- Create site-level and transect-level vegetation maps (e.g., %BareGround, %GrassLayer, %HerbLayer, %WoodyLayer, %Dung).
- Analyze spatial patterns of vegetation against UKBMS transects for ecological or policy-oriented visuals.
- Combine with UKBMS butterfly data or other GIS layers for habitat suitability or landscape analysis.
- Time-stamped data (Date) enables temporal comparisons within the 2008-09 window.

## Data Quality, Limitations & Considerations
- Temporal scope: data from 2008–2009 only; not a multi-year time series.
- Quadrat placement: random within a 10 m wide polygon around transect; may introduce spatial sampling bias relative to exact transect path.
- Species coverage: 165 plant species documented; per-quadrat estimates may include collinear or rare species.
- Data integration requires careful matching by Transect/Section/Quadrat and Date; ensure consistent naming conventions.
- Potential data gaps or ambiguities in taxon naming; reference taxon fields for standardization.

## References
- Carey, P. D., Wallis, S., Emmett, B. A., Maskell, L. C., Murphy, J., Norton, L. R., Simpson, I. C. and Smart, S. M. (2008). Countryside Survey: UK Headline messages from 2007, NERC Centre for Ecology and Hydrology.
- Shimwell, D. W. (1972). The description and classification of vegetation. Seattle, University of Washington Press.