### Mood and Anxiety Disorder Indicator (Z-Score)

**Description:**
This field (identified as `MoodAnxietyDisorders` in the spatial dataset) represents the standardized Z-score for the rate of mood and anxiety disorders within a given Lower Super Output Area (LSOA). It measures how the local concentration of these mental health conditions in a specific neighbourhood compares to the national average across England.

**Vulnerability Rationale:**
This metric is a supporting indicator within the "Health" domain, which is utilized to evaluate a community's biophysical "Sensitivity" to extreme climate events such as floods and heatwaves. 

Higher rates of mood and anxiety disorders in an area indicate a higher level of social vulnerability. The rationale driving this includes:
*   **Psychological Susceptibility:** Extreme weather events, such as flooding, are highly stressful and can cause serious mental health impacts, including post-traumatic stress disorder, depression, and anxiety. 
*   **Exacerbation of Existing Conditions:** While post-event stress is likely to affect everyone, evidence shows that individuals with pre-existing mental health conditions are likely to suffer the most during and after a crisis.
*   **Long-term Impacts:** The psychological effects of extreme weather events often last much longer (2+ years) than any adverse physical health effects.

**Interpretation:**
Because this metric is standardized as a Z-score, it allows for direct relative comparisons across different geographic areas:
*   **Positive values** denote a higher rate of mood and anxiety disorders than the national average, indicating poorer mental health and a higher level of relative vulnerability.
*   **Values around 0** indicate that the rate is approximately average for England.
*   **Negative values** signify a lower rate than the national average, indicating lower relative vulnerability.

To map and categorize the relative severity of this vulnerability, the dataset groups these Z-scores into standard classifications:
*   **≥ 2.5:** Acute
*   **1.5 to 2.5:** Extremely high
*   **0.5 to 1.5:** Relatively high
*   **-0.5 to 0.5:** Average
*   **-1.5 to -0.5:** Relatively low
*   **-2.5 to -1.5:** Extremely low
*   **≤ -2.5:** Slight

**Data Source:**
For the 2022 England LSOA dataset, the underlying data for this indicator is derived from the English Indices of Deprivation 2019 (IMD 2019). Specifically, it utilizes the "Mood and Anxiety Disorders Indicator" from the IMD Health Deprivation and Disability Domain, which is sourced from the Office for National Statistics. It carries a weight of 0.143 within the broader "Health" domain for the Sensitivity index, sharing this dimension with other health indicators such as the comparative illness and disability ratio, emergency hospital admissions, and years of potential life lost.