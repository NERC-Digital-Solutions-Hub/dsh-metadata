# Broad Habitat Area Estimates by Land Class for Great Britain 1998

- The Countryside Survey 1998 provides national estimates of Broad Habitat stock (Habitats 1-17) for Great Britain, derived from the 2007 ITE Land Classification. Estimates are given as total areas (in 000s hectares) per Land Class, with lower and upper 95% confidence intervals. Freshwater habitats used a different statistical model.
- The field survey occurred in 1998 (with a few sites in 1999) and is often referred to as the Countryside Survey 2000.

## Data files and structure

- CS1998_Broad_Habitat_Stock.csv
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class
  - BROAD_HABITAT: Broad Habitat code
  - BROAD_HABITAT_NAME: Broad Habitat description
  - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
  - MEAN_ESTIMATE: Mean area of Broad Habitat for relevant Land Class (000s ha); negative values may occur due to the statistical model and should be treated as 0
  - LOWER_ESTIMATE: Lower 95% CI
  - UPPER_ESTIMATE: Upper 95% CI
- CS1998_stock.tif
  - A 1 km pixel raster where each pixel band corresponds to a Broad Habitat class. Band mappings reflect combinations of Broad Habitat codes with Land Class:
    - For example, Broad Habitat 2 with Broad Habitat 1 equals Coniferous Woodland; Broad Habitat 2 with Broad Habitat 1 equals Band 2, etc.
  - Provides mean percentage habitat per 1 km cell within each Land Class stratum.

## Spatial and technical details

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain
- Data must be acknowledged as Countryside Survey data owned by NERC-CEH
- Freshwater data analyzed with a different model; some negative mean estimates exist and should be treated as zero

## Data usage and interpretation notes

- The dataset links national habitat stock to the ITE 2007 Land Classification and to historical Countryside Survey methods; refer to the associated publications for methodology.
- The 1998 survey provides a baseline for historical comparisons and trend analyses at the national level.
- Users should ensure proper attribution when publishing or presenting results.

## Data quality, gaps, and caveats

- Availability of data is limited to the 1998 snapshot (with some 1999 sites); granularity and timeliness may limit applicability for current planning without accompanying updates.
- Data complexity arises from:
  - Scattered data across Land Classes, requiring careful crosswalks to ITE classifications
  - Variable data quality across habitats and the need to interpret confidence intervals
  - Potential data access barriers for some users, given licensing and acknowledgement requirements

## Relevance for data strategy and governance (Data Leaders perspective)

- Data asset management
  - Clear documentation of data lineage, classification alignment (ITE Land Classification), and exact meaning of MEAN_ESTIMATE, LOWER_ESTIMATE, and UPPER_ESTIMATE
  - Explicit attribution requirements to NERC-CEH Countryside Survey
  - Clear handling of zero-values when mean estimates are negative to avoid misinterpretation
- Discoverability and access
  - Availability of both CSV and raster TIFF formats supports different analytic workflows
  - Metadata should emphasize spatial resolution, coordinate system, and crosswalk to current habitat classifications
- Data quality and standards
  - Acknowledge the methodological differences for freshwater habitats
  - Maintain metadata on potential limitations due to age (1998 data) and model specifics
- User needs and governance
  - Baseline data useful for policy assessment, historical trend analysis, and national-scale planning
  - Potential gaps identified: need for more granular or contemporary data; encourage data sharing across partners to reduce fragmentation
  - Supports co-ownership ideas by providing a national context that can be linked to partner datasets and national reporting
- Collaboration and community
  - References and publications provide methodological transparency; alignment with broader UK habitat classification efforts
  - Opportunities to coordinate with the wider data community to update or extend the dataset with newer survey rounds

## References and supporting publications

- Carey, P.D. et al. (2008) Countryside Survey: UK Results from 2007
- Scott, W.A. (2007) CS Technical Report No.4/07: Statistical Report
- Bunce, R.G.H. et al. (1996, 2007) ITE Land Classification of Great Britain
- Barr, C.J. and colleagues (1998, 1990s) Countryside Survey field handbooks
- Jackson, D.L. (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification
- Additional links to Countryside Survey website and related datasets and dois on the NERC EH NORA data centre