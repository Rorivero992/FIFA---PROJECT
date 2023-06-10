# FIFA-PROJECT

<font size="4.5">**FIFA PROJECT PRESENTATION:**</font><div style="display: flex; align-items: flex-start;">
  <div style="flex: 1;">
    <!-- Aquí va el texto -->
   Does Age and Time Affect Players' Skills?

<p align="justify">
In this project, we aimed to investigate whether there is a relationship between players' age and their skills on the field. The practical objective behind this idea was to determine the lifespan of a player and identify the age at which players reach their peak skill development. This information would be valuable when negotiating and signing player contracts.
</p>

<p align="justify">
Data Analysis Approach: We started by selecting 27 columns from the initial complete dataframe, which corresponded to players' age and various skills. After exploring the data, we found that all values were 
</p>
  </div>
  <div style="margin-left: auto; padding: 7px;">
    <!-- Aquí va la imagen -->
    <img src="IMAGES/fifa_certificado.png" alt="fifa_logo" width="200px">
  </div>
</div>


<p align="justify">
numeric, with only a few columns containing NaN values. We filled these missing values with the mean of their respective columns. Next, we normalized the numerical variables to ensure a fair comparison.
Data Analysis Approach
We started by selecting 27 columns from the initial complete dataframe, which corresponded to players' age and various skills. After exploring the data, we found that all values were numeric, with only a few columns containing NaN values. We filled these missing values with the mean of their respective columns. Next, we normalized the numerical variables to ensure a fair comparison.

<p align="justify">
Examining Age and Skills Relationship
To investigate the relationship between age and skills, we initially performed a heatmap analysis to assess the collinearity among variables. The results indicated that age did not exhibit strong correlation with the other variables. Therefore, the initial hypothesis that skills decline with increasing age was not fully supported by the data.

<p align="justify">
Introducing Overall (OVA) as a Key Variable
To further explore the relationship between age and skills, we introduced a new variable called "OVA." OVA is a measure of players' overall skills and talent in the game, ranging from 0 to 100, with 100 representing the highest score. OVA takes into account multiple attributes of a player, such as speed, passing ability, shooting, and defense. It serves as an important indicator of a player's quality in FIFA and is highly valued in game modes like FIFA Ultimate Team (FUT). Players with higher OVA ratings are generally more sought after and highly valued.
<p align="justify">
Regression Analysis Results
We conducted a linear regression analysis using OVA as the dependent variable to identify the skills most strongly associated with OVA. The analysis revealed that the following skills had the highest coefficients:
<br/><br/>

| Skill           | p-value | Coefficient |
|-----------------|---------|-------------|
| Goalkeeping     | 0.00    | 0.6260      |
| Ball control    | 0.00    | 0.5433      |
| Composure       | 0.00    | 0.1523      |
| Reaction        | 0.00    | 0.4314      |

<br/><br/>

<p align="justify">
These four skills appeared to have the most significant impact on overall player performance.
<p align="justify">
Investigating the Relationship between Skills and Age
To bridge the analysis back to age, we performed individual linear regressions for each of the identified skills to examine their relationship with age. The results were as follows:
<br/><br/>


| Skill & Age          | p-value | Coefficient |
|-----------------|---------|-------------|
| Reaction        | 0.008   | -1.94       |
| Composure       | 0.000   | 0.0697      |
| Ball control    | 0.000   | 0.0269      |
| Goalkeeping     | 0.000   | 0.0449      |
<br/><br/>

![RELACION OVA AGE](images/age_ova_blue.png)
<br/><br/>

<font size="5">**Conclusions**</font>


<p align="justify">
After analyzing these results, we can draw the following conclusions:
<p align="justify">
Age does not appear to have a direct or significant relationship with players' skills based on the initial analysis. However, it's worth noting that the majority of the sampled players fall within the age range of 20 to 32, with the highest concentration between 27 and 32. There are also a few unique cases of players above the age of 32, such as a single player aged 53. To obtain more conclusive insights on the effect of age, it would be beneficial to include players of older age groups in the analysis.
<p align="justify">
When examining the OVA as a measure of overall skills, we identified four key skills that significantly influenced a player's rating. These skills were goalkeeping, ball control, composure, and reaction. However, there were other skills with a p-value of zero and positive coefficients, such as penalty, movement, and aggression, suggesting their relevance as well. For the sake of simplicity, we focused on the top four skills.
<p align="justify">
To sum up, while age did not show a direct relationship with skills in our analysis, the overall skill rating (OVA) was strongly influenced by certain key skills. Further investigation is needed to explore the impact of age on players' skills by including a broader range of age groups.
