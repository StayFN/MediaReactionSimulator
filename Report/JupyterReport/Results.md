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