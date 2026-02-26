# Cumbria_Land_Classification file details

- Purpose and scope
  - Documents the Cumbria Land Classification dataset, which partitions Cumbria (Great Britain) into 16 Land Classes (strata) based on environmental characteristics such as climate, altitude, and slope.
  - Describes the data format, resolution, coordinate system, and the methodological approach used to define and describe the classes.

- Dataset and format
  - Format: ESRI Shapefile
  - Resolution: 1 km
  - Coordinate system: British National Grid (OSGB1936), Transverse Mercator projection
  - Extent: Great Britain
  - Context: Part of an ecological survey of Cumbria with historical references (1975–1978)

- Methodology and analysis
  - Sampling design: 11% sample created by overlaying a grid of 3 x 3 km squares; central square selected from each grid block
  - Data collection: Map characteristics derived from one-inch scale Ordnance Survey maps, supplemented by geological attributes
  - Analysis methods:
    - Indicator Species Analysis (ISA) to identify characteristics that best discriminate between land classes
    - Reciprocal Averaging (RA) ordination to assess relationships and correlations among sample squares
  - Classification approach: Uses a hierarchical land-class framework and a dichotomous key (land classification hierarchy) to assign remaining squares
  - Key insights: Altitude exerts a dominant influence; major division is between upland and lowland; classification integrates geology and land-use attributes

- The land classes (descriptions)
  - Land Class 1: Lowland, flat to gently undulating; medium quality agricultural land with mixed cultivation; variable soils (brown earths)
  - Land Class 2: Slightly higher elevation but still lowland characteristics; undulating with hedges; medium to good quality land; deep brown earths
  - Land Class 3: Lowland characteristics at higher elevation; limestone-associated; medium to poor quality agriculture; stony brown earths
  - Land Class 4: Mixed lowland/upland features; variable soil types; coniferous and broadleaved woods; mix of improved and moorland pastures
  - Land Class 5: Predominantly lowland alluvial plains; intensive farming; deep brown earths
  - Land Class 6: Lowland associated with communications/urbanization; intensive grazing; deep brown earths
  - Land Class 7: Coastal estuarine mud and sand
  - Land Class 8: Coastal with bare sand/mud; intensive livestock management; deep soils
  - Land Class 9: Markedly upland foothills; conifer-dominated woodlands; poor agricultural land; moorland
  - Land Class 10: Upland with valley bottoms; varied vegetation between valley floors and upland moorland; poor soil
  - Land Class 11: Complex middle fells; broadleaved woods; poor agricultural land; marginal grazing
  - Land Class 12: Featureless low fells; extensive conifer plantations; poor, well-drained moorland
  - Land Class 13: Steep margins of Pennines/Skiddaw; few trees; poor, poorly drained moorland
  - Land Class 14: High altitude summits; open range sheep grazing; peat-rich soils
  - Land Class 15: Upper slopes of central Lake District fells; rugged; open range sheep grazing; peat soils
  - Land Class 16: Summits and highest slopes; most mountainous; extensive peat/peaty podsols; poor land

- Distribution and summary findings
  - The major division is upland vs lowland; 16 classes reflect geological and land-use differences
  - Nearly two-thirds of Cumbria is classed as lowland
  - Some classes occur in large blocks (e.g., 1 and 2), others in smaller clusters (e.g., 4 and 11); upland classes tend to form more cohesive patterns
  - Illustrative outputs referenced: hierarchical land-class diagram (Fig. 2), example key (Fig. 3), distribution map (Fig. 4), and frequency tables (Table 2) with associations (Table 3)

- Outputs and interpretation
  - Produces a 16-class hierarchical framework enabling rapid classification of grid squares into land classes
  - Demonstrates how altitude, geology, and land use shape landscape structure and class distribution
  - Useful for landscape-scale monitoring, planning, and policy evaluation by providing a standardized baseline map of environmental strata

- Relevance to monitoring frameworks (for policy, governance, data management)
  - Provides a structured, multi-attribute framework (environmental characteristics, geology, land use) suitable for monitoring landscape change over time
  - Emphasizes the need for metadata, data quality, and interoperability when sharing datasets (references to data handling practices and potential barriers)
  - Demonstrates the value of data-driven classification keys and indicator-based analyses (ISA, RA) to derive meaningful, policy-relevant categories
  - Highlights the importance of transparent data formats, coordinate systems, and scalable outputs (shapefiles, maps, and descriptive tables)

- Data quality, access, and governance considerations
  - Metadata gaps and data provenance can hinder verification and reuse
  - Public sharing of underlying data is a potential barrier in some contexts
  - Transformation and harmonization of map-based characteristics may require substantial effort
  - Data governance and documentation (roles, responsibility, standards) are essential to maintain up-to-date classifications

- References and foundational methods
  - Bunce, R. G. H., Morrell, S. K. & Stel, H. E. 1975. The application of multivariate analysis to regional survey
  - Hill, M. O. 1973. Reciprocal averaging: an eigenvector method of ordination
  - Hill, M. O., Bunce, R. G. H. & Shaw, M. W. 1975. Indicator species analysis, a divisive polythetic method of classification

- Note on dataset provenance
  - The dataset draws on historical ecological surveys of Cumbria (1975, 1978) and uses established multivariate analysis methods to derive land classes
  - Outputs are intended to support spatial planning and environmental monitoring at county and broader scales