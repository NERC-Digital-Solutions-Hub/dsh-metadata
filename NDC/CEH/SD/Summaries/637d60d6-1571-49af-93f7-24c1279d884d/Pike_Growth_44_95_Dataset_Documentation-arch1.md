# Pike Growth Data 1944-1995

## Overview
- Dataset of growth (length) data for Pike (Esox lucius) derived from net sampling.
- Time span: 1944–1995; collected initially by the Freshwater Biological Association (FBA), continued by CEH and its predecessor IFE since 1989.
- Contains only female pike in this dataset.
- Used in Vindenes et al. (2013) American Naturalist to study climate-related trait-based dynamics in a top freshwater predator.

## Data Content and Format
- Format: Comma separated values (CSV); file size ~675 KB.
- Columns: YEAR (year of capture), LENGTH (fork length in cm to 1 mm precision), IND (individual fish identity number).
- Location: Windermere Lake, Cumbria, Great Britain. Approximate center coordinates provided (OS Grid and WGS84).
- Species: Esox lucius (Pike).

## Related Data and Metadata
- Metadata record for the data series: Pike 1944-2002.
- Related datasets:
  - Pike - Fecundity Data 1963-2002
  - Pike - Survival Data 1953-1990
  - Windermere Lake Temperature 1944-2002
- Access: CEH data portal and metadata entries.

## Sampling Design and Field Methods
- Study area: Windermere Lake, with monitoring in north and south basins.
- Primary method: Gill netting with standardized protocol established from 1982 onward.
- Net specifications (since 1982): 64 mm bar mesh multifilament gill nets, 40 m length, 3 m depth; deployed on the bottom at ~4–5 m depth, across 10 sites per basin.
- Sampling season and process (typical): October to December; nets set at five sites during daylight, inspected and catches removed on a two-day cycle, and lifted on a Friday; site rotation to cover the lake; each site fished for two weeks per season.
- Sampling effort:
  - 1982–1989: total annual sampling effort ~348 net days, distributed roughly evenly between basins.
  - 1990 onwards: total annual sampling effort ~240 net days, maintaining basin balance.
- Historical variation: earlier nets (1940s–1982) used larger mesh (initially 5 inches / 64 mm knot-to-knot) with different sampling regimes; post-1982 standardization aimed to improve comparability.

## Analytical Methods and Data Processing
- Laboratory processing:
  - Each pike assigned an IND (identity number).
  - Measurements recorded: LENGTH (fork length to 1 mm) and WEIGHT (to 100 g); sex determined through dissection.
  - Age estimation: left opercular bone analyzed with Frost & Kipling (1959) method; nominal birth date set to 1 April.
- Quality control: measurements verified by permutations involving three individuals to reduce errors.

## Dataset Provenance and Usage
- Primary use within the Vindenes et al. (2013) study on climate effects and trait dynamics in a top freshwater predator.
- Provides long-term, female-only growth records enabling analyses of growth trajectories and potential climate or prey-related influences when combined with other datasets (e.g., temperature, fecundity, survival).
- Data provenance documented via related methodological references (Le Cren 2001; Winfield et al. 2008; Frost & Kipling 1959).

## Considerations for Analysts
- Strengths:
  - Long temporal coverage with standardized methods since 1982 facilitates growth trend analysis over decades.
  - Individual-level data enables growth trajectories and age-length relationships when combined with ageing data.
- Limitations:
  - Female-only subset may limit generalization to the entire population.
  - Pre-1982 data may be less standardized due to methodological variations prior to standardization.
  - Spatial granularity limited to Windermere Lake and its basins; fine-scale local patterns outside this scope may be absent.
- Potential analyses:
  - Growth rate modeling as a function of year, age, and environmental covariates (e.g., accompanying temperature data).
  - Correlations between length-at-age and prey abundance or climatic variables (as in related studies).
  - Integration with fecundity and survival datasets to explore life-history trade-offs.

## Access and Contact
- Data and metadata are accessible via CEH data portals and associated metadata records:
  - Pike Growth Data 1944-1995 metadata and related entries.
  - Related datasets: Pike - Fecundity Data, Pike - Survival Data, Windermere Lake Temperature data.