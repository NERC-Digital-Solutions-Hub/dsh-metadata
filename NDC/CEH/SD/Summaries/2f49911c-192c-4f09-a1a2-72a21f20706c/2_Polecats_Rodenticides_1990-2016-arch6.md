# Secondary exposure to second-generation anticoagulant rodenticides in European polecats ( Mustela putorius ) in Great Britain.

## Overview
- Supplementary dataset to the 2018 Environmental Pollution paper examining long-term secondary exposure to anticoagulant rodenticides in British polecats.
- Contains liver-residue chemical analyses and associated metadata for polecats collected between 1990 and 2016, across three survey periods.
- Enables exploration and self-service analyses of exposure patterns by time, location, and environmental context.

## Data structure and key fields
- record: unique animal identifier.
- data: data origin for chemical analyses (NEW = Sainsbury et al. 2016; OLD = Shore et al. 2003).
- year: year of carcass collection (1990–2016).
- time: years since first animal collection.
- survey: which rodenticide analysis survey the sample originated from (ONE: 1990–1995; TWO: 1995–1998; THREE: 2013–2016).
- season: season of carcass collection (Spring, Summer, Fall, Winter).
- halfYear: half of year when collected (FIRST: Dec–May; SECOND: Jun–Nov).
- x, y: OSGB36 coordinates (metres) for collection location.
- region: geographic region (North, South, East, West).
- expansion: inside or outside the 1990s range (IN/OUT).
- sex: biological sex where known (Male/Female).
- landClass: predominant land use at the location, derived by GIS overlay with CEH Land Cover Map 2007; mainly distinguishing arable vs pastoral.
- hBrom, hDifm, hBrod: concentrations of bromadiolone, difenacoum, brodifacoum in liver (µg/g) for the 2018 dataset; LODs applied from Shore et al. 2003.
- hBBrom, hBDifm, hBBrod: detection flags for each compound (0 = none detected; 1 = detected; LOD-based treatment).
- hBRods: number of rodenticide compounds detected in the liver (0, 1, 2, or 3; LOD-adjusted).
- hCRods: total number of rodenticide compounds detected (same coding scale as hBRods).
- hConcT: total concentration of rodenticide compounds (µg/g) for the 2018 dataset; LOD-adjusted per Shore et al. 2003.
- Notes: NA indicates missing data for that field.

## Data provenance and versions
- Data build combines Shore et al. 2003 (1992–1999 range) and Sainsbury et al. 2018 (2013–2016 range) analyses.
- NEW vs OLD coding reflects origin of chemical data; NEW corresponds to the Sainsbury et al. 2018 dataset.
- LOD values from Shore et al. 2003 are applied to the 2018 dataset where needed.
- Geographic and land-use classifications derived via GIS methods (CEH Land Cover Map 2007; 1 km buffers; majority class).

## Geographic and temporal coverage
- Temporal span: 1990–2016, with three survey windows (1990–1995; 1995–1998; 2013–2016).
- Geographic scope: Great Britain; coordinates use OSGB36; regional breakdown into North, South, East, West.
- Spatial processing: carcass coordinates mapped to land-use class via 1 km buffers around each point.

## Data quality, limitations, and notes
- Data are partially patchy due to combining multiple studies; some fields may be NA where data were not collected or recorded.
- LOD-based imputation applied to detectability and concentration fields; care needed when interpreting low-level detections.
- Sex and some location details may be missing for certain records.
- Users should reference the associated publications for methodological context: Shore et al. 2003; Sainsbury et al. 2018.

## Potential uses for data support
- Build self-serve dashboards or reports on rodenticide exposure by year, survey, region, or land-use type.
- Create choropleth or point maps showing exposure intensity and detection across Great Britain.
- Compare patchy historical data with newer data, harmonizing by LOD handling and site-level variables.
- Support policy or conservation analyses by identifying temporal trends and geographic hotspots in secondary exposure.

## References
- Shore RF, Birks JDS, Afsar A, Wienburg CL, Kitchener AC (2003) Spatial and temporal analysis of second-generation anticoagulant rodenticide residues in polecats ( Mustela putorius ) from throughout their range in Britain, 1992-1999. Environmental Pollution, 122, 183-193.
- Sainsbury KA, Shore RF, Schofield H, Croose E, Pereira MG, Sleep D, Kitchener AC, Hantke G, McDonald RA (2018) Long-term increase in secondary exposure to anticoagulant rodenticides in European polecats Mustela putorius in Great Britain. Environmental Pollution, 236, 689-698.