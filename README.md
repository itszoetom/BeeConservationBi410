# BI410 Data Science for Ecological Conservation Term Project Final Writeup  
**Zoe Tomlinson, Madi Kloberdanz**  

## Introduction  

### Background  
Wildfires, exacerbated by climate change, are increasing in frequency and severity, presenting significant ecological challenges. Recent studies highlight the impact of changing fire regimes on ecosystems. For example, large and severe fires in the Pacific Northwest are associated with warmer, drier conditions, projected to increase with climate change (Halofsky et al., 2020). Post-fire environments can significantly alter plant communities, affecting bee populations by changing the availability of nectar and pollen sources (Nevins et al., 2014).  

Wildfires reshape habitats by clearing dense forests and altering vegetation, potentially offering bees new foraging opportunities. However, the role of fire severity in shaping bee populations, particularly in post-fire environments, remains underexplored. Understanding this relationship is crucial for developing informed land management strategies to support pollinator conservation.  

This research investigates how varying fire severities influence bee populations and their distribution after wildfires, specifically assessing whether fire severity correlates with changes in bee density.  

## Hypotheses  

### Hypothesis 1: Fire Severity  
- **Null Hypothesis**: There is no linear correlation between wildfire severity and the percent change in bee counts after the fire. (r = 0)  
- **Alternative Hypothesis**: There is a linear correlation between wildfire severity and the percent change in bee counts after the fire. (r ≠ 0)  

### Hypothesis 2: Population Change  
- **Null Hypothesis**: There is no significant difference in bee counts before and after the fire.  
  \( \mu_{\text{before\_fire}} = \mu_{\text{after\_fire}} \)  
- **Alternative Hypothesis**: There is a significant difference in bee counts before and after the fire.  
  \( \mu_{\text{before\_fire}} \neq \mu_{\text{after\_fire}} \)  

## Data  

### Fire Severity Data  
Spatial data from the BAER (Burned Area Emergency Response) program, provided by the U.S. Geological Survey, measures fire severity in Oregon wildfires from 2020. Fires analyzed include Umpqua, Hood, Holiday, Beachie, Fremont, Ben Young, Brattain, Lionshead, Thielsen, Two Four, and Whiteriver.  

### Bee Population Data  
Data from the Oregon Bee Atlas (OBA) covers 2018–2022, focusing on changes in bee density and distribution before and after the 2020 fires. Plant taxonomy information was excluded, though future research could explore species composition changes and plant interactions.  

### Oregon Ecoregions Data  
A shapefile from the Oregon Conservation Strategy dataset represents ecoregions in Oregon. This dataset was transformed to align with the Beachie 2020 fire dataset, assisting in regional habitat composition analysis.  

### Data Engineering  
- Created variables: `Average_Severity` and `Percent_Change_in_Bees` for regression analysis.  
- Plotted bee locations and fire buffers before and after wildfires on the ecoregions dataset.  

## Hypothesis Tests  

### Test for Hypothesis 1: Fire Severity and Percent Change in Bees  
- **Statistical Test**: Pearson Correlation Coefficient  
  - **Coefficient**: -0.48  
  - **P-value**: 0.13  
- **Result**: Fail to reject the null hypothesis.  

**Interpretation**: While a moderate negative correlation exists, the lack of statistical significance suggests the relationship may result from random variation rather than a causal link.  

### Test for Hypothesis 2: Bee Population Change  
- **Statistical Test**: Paired T-Test  
  - **T-statistic**: 3.13  
  - **Mean Difference**: 560.73  
  - **P-value**: 0.01  
- **Result**: Reject the null hypothesis.  

**Interpretation**: The significant difference in bee populations before and after fires highlights measurable impacts, emphasizing the importance of post-fire environmental conditions.  

## Visualization  

Plots of bee populations and fire buffers overlaid on ecoregions datasets before and after the fires are included in the analysis.  

## Conclusion  

This study investigated the impact of wildfire severity on bee populations in Oregon, focusing on changes in density and distribution.  

### Key Findings  
- **Hypothesis 1**: No significant linear relationship exists between wildfire severity and bee density changes.  
- **Hypothesis 2**: Bee populations show significant changes before and after fires, suggesting wildfires influence bee density.  

### Implications for Conservation  
Findings highlight the importance of targeted land management strategies to support bee resilience post-fire. Conservation efforts should focus on habitat restoration to ensure the availability of nectar and pollen sources. Future research could explore the interaction between bee populations and plant communities in greater detail.  

## References  
- Halofsky, J.E., Peterson, D.L., & Harvey, B.J. (2020). *Changing wildfire, changing forests: The effects of climate change on fire regimes and vegetation in the Pacific Northwest, USA*. *Fire Ecology, 16*(4). [https://doi.org/10.1186/s42408-019-0062-8](https://doi.org/10.1186/s42408-019-0062-8)  
- Melathopoulos, A., Edmunds, B., & Rivers, J. (n.d.). *How do wildfires affect bees?* Oregon State University Extension. Retrieved from [OSU Extension](https://extension.oregonstate.edu/forests/fire/how-do-wildfires-affect-bees)  
- Nevins, S., et al. (2014). *Impact of post-fire environments on pollinator availability*. *Journal of Ecology*.  
