DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Overview
- Documents the carbon stock of standing dead wood; part of ESPA programme and P4GES project.
- Provides site-level measurements and derived metrics to enable assessment of standing dead wood carbon.
- Includes guidance and acknowledgements for data use, with a note that missing data is indicated.

## Key fields and definitions
- site_ID: P4GES site code; Text String; used to identify sampling locations.
- Surface: information/variable type placeholder; blank values indicated.
- DBH: diameter of dead wood trunk at 130 cm height; Numeric; Unit: centimeters; field materials/resources: forester compass.
- Diam_base: diameter of trunk at 30 cm height; Numeric; Unit: centimeters; field materials/resources: forester compass.
- Diam_top: estimated diameter at the top of the trunk; Numeric; Unit: centimeters.
- Height: height of the standing dead wood; Numeric; Unit: meters; field materials/resources: vertex.
- Volume: volume calculated by volume = (1/3) * π * H * (r1^2 + r2^2 + r1*r2); Numeric; Unit: cubic meters (m^3); H is height; r1 and r2 are base/top diameters.
- Category: wood density classification; Categorical; values: S = sound, I = intermediate, R = rotten.
- Density: numeric; unit not specified.
- Carbon_stock: carbon stock of standing dead wood; Numeric; Unit indicated as milligrams per hectare (Mg.ha-1) (note: terminology in parentheses may imply megagrams per hectare).

## Provenance and references
- Dataset header is titled “DATA HEADER information for Standing_dead_wood_carbon_stock.csv.”
- Related materials: Manual 1_Classical_Survey.
- Programme: ESPA; Project: P4GES.
- Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- DOI provided for the data resource.

## Usage and dissemination notes
- Data supports creating user-friendly products (e.g., dashboards, pivot tables) to explore standing dead wood carbon stock.
- Encourages data cleaning, transformation, and combination with other datasets to enable self-service analysis.
- Emphasizes attribution and appropriate acknowledgement when using outputs.

## Data quality and caveats
- Missing data indicated by the notes section (e.g., “Notes – means no data available”).
- Some fields contain placeholder or blank values (e.g., Surface information).
- Unit specification for Carbon_stock may be inconsistent in the header (mentions milligrams per hectare alongside Mg.ha-1).