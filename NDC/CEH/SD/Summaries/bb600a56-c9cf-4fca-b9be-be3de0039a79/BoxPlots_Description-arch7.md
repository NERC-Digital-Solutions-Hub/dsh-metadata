# LOCAR BASELINE DATASETS

## Introduction
- A box and whisker plot visualises the range, median, and quartiles of a dataset.
- Typically drawn with a number line (horizontal or vertical).
- Purpose: provide a visual check of data quality and assist in interpreting the distribution.
- Helps determine how data cluster within the box, the length of the whiskers, and how many points are outliers.

## Description
- The LOCAR box and whisker plots use a number line on the y-axis; it relates to the units of the determinand being displayed.
- The x-axis shows the different sites for which the determinand was measured; site IDs represent these sites.
- The box’s red line indicates the median.
- The box edges represent Q1 (25th percentile) and Q3 (75th percentile).
- Whiskers are calculated as:
  - Lower whisker = Q1 − 1.5 × IQR
  - Upper whisker = Q3 + 1.5 × IQR
  - IQR stands for the interquartile range (Q3 − Q1).
- Values outside the whiskers are considered outliers.
- The accompanying diagram illustrates these concepts.