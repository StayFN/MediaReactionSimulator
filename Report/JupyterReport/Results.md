---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Results

To verify whether LLMs can be used to simulate experiments in social science, several experiments were performed trying to replicate studies referenced in the initial research paper of the AMUSE model {cite}`reinecke2021media`. This section describes the results of the methods pointed out in [](methodological-approach) and [](method). The results are structured in [](proposition-2-1-result) and [](proposition-2-2-result).

(proposition-2-1-result)=
## Proposition 2.1

In our study, we successfully replicated the experiments described in {cite}`muraven1998self` by utilizing LLMs. Our simulation results, displayed in Figure [](funny-ssc-characteristics), reveal a significant variation in the average number of laughs, smiles, and overall amusement rating based on the individual's SSC level. We obtained these results by briefing the LLM on the characteristics of individuals with either high or low SSC before requesting its calculations. The findings indicate that individuals with low SSC exhibited an average of 1.94 smiles and 3.18 laughs per video, whereas those with high SSC showed an average of 0.79 smiles and 2.1 laughs per video, reflecting a notable difference of 60.3% less smiles and 33.96% less laughs for individuals with high SSC. Additionally, the average amusement rating was found to be 3.11 for individuals with low SSC, while those with high SSC had a rating of 2.22, which is 28.6% less.

```{figure} ./images/funny_ssc_characteristics.png
---
name: funny-ssc-characteristics
---
Humorous Videos (SSC Characteristics)
```

In Figure [](funny-ssc-defined), we see the outcomes of the same experimental simulation, but with a twist. This time, the LLM was not provided with any specific characteristics; instead, only the participants' SSC levels were defined as either high or low. The results show a notable difference in the average number of smiles and laughs between the two groups. Individuals with low SSC levels exhibited an average of 0.75 smiles and 2.38 laughs, while those with high SSC levels had an average of 0.62 smiles and 1.99 laughs. These findings indicate a decrease of 17.3% in smiles and 16.39% in laughs for individuals with high SSC levels compared to those with low SSC levels. The average amusement rating was found to be 2.13 for individuals with high SSC, compared to 2.07 for those with low SSC, representing an increase of 2.9% for individuals with high SSC. This contrasts with the findings of the study mentioned in {cite}`muraven1998self`, where no such correlation was observed.

```{figure} ./images/funny_ssc_defined.png
---
name: funny-ssc-defined
---
Humorous Videos (SSC Defined)
```

The simulated experiment yielded another interesting outcome: when the LLM was provided with descriptions of individuals' characteristics, the average number of smiles and laughs, as well as the average amusement rating, tended to be more exaggerated for individuals with high or low SSC scores. In the initial simulation run (see Figure [](funny-ssc-characteristics)), the ratings given by high SSC individuals averaged 40.95% lower than those given by low SSC individuals. However, in the second simulation run (see Figure [](funny-ssc-defined)), this discrepancy narrowed significantly, with high SSC individuals giving ratings that were only 10.26% lower on average compared to their low SSC counterparts.

Moreover, we replicated the experiment presented in {cite}`schmeichel2007attention` utilizing LLMs, and the outcome is depicted in Figure Figure [](gruesome-ssc-characteristics). The figure showcases the perceived emotions of depression, tension, disappointment, anxiety, and regret, along with the degree of emotion visibility to others. Our approach involved describing individuals' SSC characteristics to the LLM prior to requesting their evaluations. The findings indicate a substantial difference between individuals with high SSC (depressed: 3.65, tense: 8.16, dissatisfied: 6.22, anxious: 6.21, sorry: 3.47, emotions visible: 7.18) and those with low SSC (depressed: 20.12, tense: 37.2, dissatisfied: 28.96, anxious: 38.40, sorry: 11.13, emotions visible: 39.68). This diverges from the original study's outcomes {cite}`schmeichel2007attention`, where participants experienced emotions similarly. Nonetheless, individuals with high SSC demonstrated greater proficiency in concealing their emotions from others. According to our simulation, individuals with high SSC encountered emotions with an average intensity of 78.22% lower compared to those with low SSC. Additionally, the simulation suggests that individuals with high SSC possess improved ability to mask their emotions from external observers, aligning with the original experiment's conclusions {cite}`schmeichel2007attention`.

```{figure} ./images/gruesome_ssc_characteristics.png
---
name: gruesome-ssc-characteristics
---
Gruesome Videos (SSC Characteristics)
```

Figure [](gruesome-ssc-defined) presents the outcome of a similar simulated experiment, where the LLM was not provided with any information about the participants' high or low SSC traits. Instead, the LLM was simply instructed to simulate individuals with either high or low SSC. The results revealed a substantial disparity between individuals with high SSC (depressed: 3.74, tense: 7.32, dissatisfied: 5.98, anxious: 5.86, sorry: 3.48, emotions visible: 5.61) and those with low SSC (depressed: 13.65, tense: 22.36, dissatisfied: 18.21, anxious: 20.63, sorry: 11.03, emotions visible: 30.29). These findings do not align with the experiments described by {cite}`schmeichel2007attention`, as the emotions experienced by individuals with high SSC were found to be 69.41% less intense compared to those with low SSC. Nonetheless, our simulation suggests that individuals with high SSC possess improved emotional control abilities, aligning with the original experiment's conclusions {cite}`schmeichel2007attention`.

```{figure} ./images/gruesome_ssc_defined.png
---
name: gruesome-ssc-defined
---
Gruesome Videos (SSC Defined)
```

In addition, the results of the two experimental simulations indicate that providing the LLM with descriptions of high or low SSC individuals yields more pronounced outcomes. Specifically, the first simulation (see Figure [](gruesome-ssc-characteristics)) revealed that individuals with high SSC experienced an average reduction of 78.22% in emotional intensity compared to those with low SSC, while the second simulation (see Figure [](gruesome-ssc-defined)) showed a decrease of 69.41%.

Furthermore, we replicated the results by Stucke & Baumeister {cite}`stuckeEgoDepletionAggressive2006`, which investigate the relationship between self-regulation and aggressive behavior. The Figure showcases the results of exposing the LLM to provocative videos. While the main takeaway from the paper was replicated `Individuals with lower SSC exhibit more aggressive reactions to provocation`, it is clearly visible that the LLM almost always chooses the lowest option for high SSC individuals, contradicting the observed diversity in real-world experiments {cite}`stuckeEgoDepletionAggressive2006`. While not as extreme, this trend can also be observed with low SSC individuals. The median is 2 for the prompts where we assigned the LLM the characteristics of a Low SSC Individual and 3 for where we defined the LLM as a Low SSC Individual. Compared with the results for high SSC individuals with a median of 1, this is a significant difference, especially when factoring in that only 3 values deviated from the median for high SSC individuals.

```{margin}
```{note}
Notched boxplots incorporate a "notch" around the median to visually indicate the confidence interval of the median. These notches are useful for assessing statistical significance, with non-overlapping notches between two boxes suggesting a significant difference in their medians. The width of the notch is typically proportional to the interquartile range and inversely proportional to the square root of the sample size, using a common formula of ±1.58 × IQR/√n.

Occasionally, this can result in 'flipped' notches, where the lower end of the notch is above the first quartile, or the upper end is below the third quartile, indicating low confidence in the median estimate. While unusual in appearance, these flipped notches provide important information about the uncertainty in the median's estimation.[^1]
```

The final paper we replicated connected to proposition 2.1 by Reinecke & Maier {cite}`reinecke2021media` was by Dillman Carpentier & Mazandarani {cite}`Sexy`
We could clearly confirm the statement made by Reinecke & Maier {cite}`reinecke2021media` that "high SSC individuals are better able to downregulate their emotional reactions, such as [...] or sexual stimulation". In Figure [](sex_stim) it can be observed that low SSC individuals experience significantly higher sexual stimulation when confronted with sexual content compared to high SSC individuals. For the high SSC individuals not a single of the 47 Shorts resulted in a value other than the lowest available one. Additionally, a significant difference can also be observed between the group where characteristics of a low SSC individual were supplied with the prompt compared to the group where we just defined the LLM to be a low SSC individual. The defined group experienced significantly higher stimulation as can be seen in [](sex_stim).

```{figure} ./images/sex_stim.png
---
name: sex_stim
---
Affectionate Reaction in Terms of Sexual Stimulation 

```

(proposition-2-2-result)=
## Proposition 2.2

In our study, we replicated an experiment previously described in {cite}`johnson2015self` by utilizing LLMs, and conducted a series of simulations. The initial run of the simulation yielded results that are illustrated in Figure [](short-story-ssc-characteristics), which presents the outcomes when the LLM was provided with descriptions of high or low SSC individual characteristics prior to evaluation requests. Our findings reveal a minor discrepancy in the experienced emotions, with high SSC individuals experiencing slightly more intense emotions on average (enjoyment: 3.38, fun: 3.23, moving 2.24, impression: 3.54, suspense: 1.82, transportation: 2.4, identification: 2.37) compared to those with low SSC (enjoyment: 3.18, fun: 3.56, moving 1.93, impression: 3.24, suspense: 1.59, transportation: 2.17, identification: 2.39). These results diverge from the original experiment's findings {cite}`schmeichel2007attention`, since our simulation showed that low SSC individuals experienced emotions 5.9% less intensely than their high SSC counterparts.

```{figure} ./images/short-story_ssc_characteristics.png
---
name: short-story-ssc-characteristics
---
Short-Story Videos (SSC Characteristics)
```

Figure [](short-story-ssc-defined) showcases the outcomes of the second simulation run, where the LLM was not provided with any specific characteristics of high or low SSC individuals. Instead, we merely distinguished between individuals possessing high or low SSC prior to querying the LLM for its responses. Notably, the emotional intensities varied more significantly between high and low SSC individuals in this run compared to the initial simulation. Specifically, high SSC individuals reported stronger experiences (enjoyment: 3.44, fun: 3.25, moving 2.27, impression: 3.52, suspense: 1.89, transportation: 2.45, identification: 2.51) than their low SSC counterparts (enjoyment: 2.96, fun: 2.85, moving 1.63, impression: 2.56, suspense: 1.51, transportation: 1.75, identification: 2.0).  On average low SSC individuals experienced emotions 21.53% less than high SSC individuals, contradicting the findings presented in the original experiment's paper {cite}`schmeichel2007attention`.

```{figure} ./images/short-story_ssc_defined.png
---
name: short-story-ssc-defined
---
Short-Story Videos (SSC Defined)
```

The findings from both simulation runs contradict the original research by {cite}`schmeichel2007attention`, which suggests that individuals with high SSC tend to experience less intense emotions compared to those with low SSC. Instead, our simulations yielded that low SSC individuals experience weaker emotions, with the first run (see Figure [](short-story-ssc-characteristics)) showing an average reduction of 5.9% in emotional intensity compared to high SSC individuals, while the second run (see Figure [](short-story-ssc-defined)) showed a larger discrepancy of 21.53%. Notably, these patterns were reversed when examining the simulation runs for [](proposition-2-1-result).


In our last experiment we were able to partly replicate the results of Tamborini et al. (2017) as cited in {cite}`reinecke2021media`. As can be seen in Figure [](sexist_jokes ) The enjoyment of sexist jokes was higher when the LLM was assigned a role with low SSC or similarly only with characteristics of a low SSC, both having a median enjoyment of 4 out of 5, while both high SSC groups experienced lower levels of enjoyment with a median of 3. We could not replicate the hypotheses, that low SSC individuals experience sexist jokes as more appropriate compared to high SSC individuals, our findings show the opposite. Low SSC individuals experienced the jokes as less appropriate with a median of 3 for the characteristics group and 2 for the defined group. High SSC individuals had a median of 3 for both groups, this effect gets more distinct when taking the mean into account (2,79 vs. 3.34 and 2.08 vs. 3.39 respectively).

```{figure} ./images/sexist_jokes.png
---
name: sexist_jokes
---
Reaction to Sexist Jokes
```

It's important to note that upon examining the boxplots, the distributions observed do not align with what one might typically expect from real-world data. To further substantiate these findings, we conducted significance tests, calculating the p-value for each group.

```{code-cell} python
from scipy import stats
import pandas as pd
df2 = pd.read_csv("files_for_python_code\df_sexist_jokes.csv")

column_pairs = [
    ('Low SSC Char. Enjoym.', 'High SSC Char. Enjoym.'),
    ('Low SSC Char. Appr.', 'High SSC Char. Appr.'),
    ('Low SSC Def. Enjoym.', 'High SSC Def. Enjoym.'),
    ('Low SSC Def. Appr.', 'High SSC Def. Appr.')
]

for col1, col2 in column_pairs:
    t_stat, p_value = stats.ttest_ind(df2[col1].dropna(), df2[col2].dropna())
    print(f'The p-value for {col1} and {col2} is {p_value:.30f}')
```

[^1]: <https://stackoverflow.com/questions/26291082/weird-behavior-of-matplotlibs-boxplot-when-using-the-notch-shape>