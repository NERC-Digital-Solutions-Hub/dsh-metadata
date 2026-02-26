# Additional notes and changes to the plot location and sampling information in Marrs et. al . 1986

- Purpose of the notes
  - Provide updated guidance to enable accurate relocation and repeatable ordering of sampling locations across multiple plots and sites.
  - Document changes to markers, transects, and frame configurations since the original Marrs et al. 1986 references.

- Common methodological themes across sites
  - Each site typically includes an exclosure (enclosed) plot and a grazed plot, with transects and frame positions arranged in a defined grid.
  - Frame positions are centered on transects and marked relative to marker lines or fence features; the pin frame location generally straddles the transect line.
  - Transects and frames are spaced regularly (commonly 3 m between transects and 3 m between frame positions, though some sites use slightly different conventions).
  - Marker reliability: marker posts may be replaced by Permablock markers; where markers are obscured by vegetation, metal detectors are recommended for locating them.
  - Orientation and numbering vary by site (e.g., transects numbered east-to-west or north-to-south; frame numbering can run opposite directions between exclosure and grazed plots).
  - Some sites experience disruptions to transect completeness (e.g., Pennine Way routing affecting transects) and have reduced transects recorded accordingly.
  - Data products of interest include precise pin positions (e.g., 500 positions per site with 5–10 frame positions per quadrat, depending on the site).

Site-specific notes

- Knock Fell (Agrostis-Festuca Grassland, D31)
  - Plots: exclosure and grazed plot; transects 3 m apart; frames 3 m apart along each transect; pin frame straddles transect line.
  - Exclosure: not a perfect square, but interior plot is.
  - Exclosure transects start at the south end; stakes outside first frame by 2 m; 1 m from south fence.
  - Transect 1 and 10 distances from fences specified; transect end marks 1 m outside Frame 10 position.
  - Grazed plot (south of enclosure): divided into 2 sections (Frames 1–6 and Frames 7–10); only 1–8 transects recorded due to trampling risk; marker posts replaced with Permablocks (2 m outside ends of sections; exact Permablock positions provided for selected transects).
  - Data implications: detailed geolocation anchors exist for multiple Permablocks and frame references to support relocation.

- Hard Hill (Festuca Grassland, D40)
  - Exclosure: end markers ~3 m apart; marker posts for grazed plot replaced with Permablocks; two NW/SW marker coordinates provided, 27 m apart.
  - Transects: numbered N–S; frames 1–10 run north–south; frame locations 1 m from marker lines, then every 3 m.
  - Grazed plot: Permablocks mark start of transects; direction measured Mag (bearing) values documented.
  - Data implications: relocation relies on Permablock placements and reference distances from exclosure posts.

- Little Dun Fell (Festuca Grassland, D42)
  - Structure: within exclosure, original fence line reference; transects end markers 2 m outside frame positions; frames 1–10 at 3 m intervals; start/end distances from fences specified.
  - Grazed plot: marker posts replaced with Permablocks located at different positions from exclosure markers; transects run from south to north on this plot; distance between start markers is given (27 m between end markers through frame 1 positions).
  - Data implications: frame numbering differs between plots (south-to-north in grazed vs north-to-south in exclosure).

- Silverband (Eriophoretum, D34)
  - Plots: both exclosure and grazed each have 5 transects with 10 frame positions (500 pin positions total); frames straddle transect lines.
  - Exclosure: posts 2 m outside frame 1; 1 m outside frame 10.
  - Grazed plot: marker positions relative to exclosure posts documented; transects run SE–NW; markers placed 2 m from frame 1 position at start of transect 1.
  - Data implications: detailed relative measures enable precise relocation within peat vegetation context.

- Troutbeck Head (Eriophoretum, D30)
  - Plots: both with 5 transects and 10 frame positions; 500 pin positions; transects mark with wooden stakes; frames straddle transect lines.
  - Exclosure: transects run north–south with 2 m gaps between transects; ends offset from West fence and North fence.
  - Grazed plot: transects run West–East; 2 m gaps between transects; end/frame positions defined relative to marker posts.
  - Data implications: orientation differences between plots require careful alignment of transect numbering and frame coordinates for GIS mapping.

- Bog Hill (Calluna-Eriophoretum, D26)
  - Plots: 7 transects with paired 1 m × 1 m quadrats (A and B) on each side of transects; 9 m quadrat length; 40 quadrats repeatedly resurveyed.
  - Plot grid: corner posts 16 m apart (West-East) and 11 m apart (North-South); transects at 2 m intervals; quadrats at 1 m intervals from North to South; A/B positions within quadrats.
  - Sampling: within each survey, 40 quadrats are recorded; pin frame across quadrats; 5 frame positions used with 2 randomly allocated pin locations per frame (10 pins per quadrat; 400 pins total).
  - Quadrats recorded: detailed enumeration of which quadrats (A/B, enclosed/grazed) were sampled per survey.
  - Data implications: strong quadrat-level geolocation requirements; 40-quadrat repeat subset to support temporal analysis.

- Cottage Hill (J1, Juncus Squarrosus Grassland, D20)
  - Plots: 10 transects per plot; 10 frame positions; all 10 frame points recorded (1000 pin positions total).
  - Orientation: SE–NW orientation; frames run SE to NW; transects 1 m apart; frames start 1 m from marker post and then at 2 m intervals.
  - Grazed plot: adjacent to enclosure along NE slope; relative offsets to exclosure end markers provided to facilitate relocation.
  - Data implications: consistent high-density pin-position data; orientation must be accounted for in GIS.

- River Tees (Nardus Stricta Grassland, D33)
  - Plots: 10 transects × 10 frame positions × 10 points per frame (1000 pin positions); both exclosure and grazed plots recorded.
  - Exclosure: end transect posts oriented N–S; first frame 0.5 m from North marker post; frame spacing 1.5 m.
  - Grazed plot: three sections; transects run East–West; numbering from East to West; sections defined relative to exclosure position; three-section layout with specified longitudinal offsets.
  - Data implications: section-based structuring requires careful section ID mapping in GIS.

- Moss Burn (Johnny's Flush, D44)
  - Plots: 10 transects × 6 frame positions; 5 frame positions per quadrat with replicates; total 300 pin positions.
  - Plot setup: fenced area with grazed plot 2 m upslope of fence; recording plots divided into 1 m × 1 m quadrats labeled A–J (long axis) and 1–6 (short axis); pin frame placed across quadrat at 45 cm from base; pins recorded at positions 2, 4, 6, 8, 10 (replicates 1–5).
  - Data implications: grid and quadrat structure defined; ensures reproducible sampling across peat vegetation.

How to use these notes in GIS workflows
- Build precise geospatial references by capturing:
  - Fixed anchors: fences, exclosure corners, corner posts, and marker posts (including Permablocks).
  - Relative measurements: distances from fences/posts to transects, frame 1 positions, and frame spacing (usually 3 m, but with site-specific exceptions).
  - Orientation and numbering: explicit directionality (N–S vs E–W) and frame/transect numbering schemes per site.
  - Marker accessibility: note that some markers may be hidden; plan for metal-detection workflows where needed.
- Data modeling implications
  - For each site, store: site_id, plot_type (exclosure/grazed), transect_id, frame_id, distance_from_anchor, bearing (Mag), marker_type, frame_position_label, quadrat_id (if applicable), and pin_position_index.
  - Include fields to capture notes on site-specific deviations (e.g., Pennine Way impact, partial transects, orientation differences between plots).
  - Maintain a separate layer or table for marker locations (original posts vs Permablocks) with cross-references to the transect/frame grid for relocation.

Overall takeaway
- This document provides a comprehensive, site-by-site guide to the spatial layout, marker conventions, and measurement schemes used to relocate and compare sampling locations across exclosure and grazed plots, with explicit details to support repeatable GIS mapping and data integration.