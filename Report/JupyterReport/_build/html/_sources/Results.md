# Results

To verify whether LLMs can be used to simulate experiments in social science, several experiments were performed trying to replicate studies referenced in the initial research paper of the AMUSE model {cite}`reinecke2021media`. This section describes the results of the methods pointed out in [](methodological-approach) and [](method). The results are structured in [](proposition-2-1-result) and [](proposition-2-2-result).

(proposition-2-1-result)=
## Proposition 2.1

In our research we were able to reproduce the results of the experiments described in {cite}`muraven1998self` by using LLMs. Figure [](funny-ssc-characteristics) shows our simulation results of the experiment by presenting the average number of laughs and smiles as well as the overall amusement rating. The results were produced by describing the characteristics of a person with high or low SSC to the LLM before asking it to calculate the results. It is shown that the average number of laughs and smiles as well as the average overall amusement rating differ significantly depending on the SSC level. While the average number of smiles for individuals with low SSC were 1.94 per Video, individuals with high SSC smiled on average 0.79 times per video which is 60.3% less. The average number of laughs per video is 3.18 for individuals with low SSC, while individuals with high SSC laughed only 2.1 times per video on average which is 33.96% less. Finally, the average amusement rating for persons with low SSC is represented with 3.11 while persons with high SSC have an average amusement rating of 2.22 which is 28.6% less.

```{figure} ./images/funny_ssc_characteristics.png
---
name: funny-ssc-characteristics
---
Humorous Videos (SSC Characteristics)
```

Figure [](funny-ssc-defined) shows the results of the same experiment simulation but this time, no characteristics were described to the LLM. Instead it was simply defined whether the participant has high or low SSC levels. The Figure shows that the results are less significant with the average number of smiles being 0.75 for individuals with low SSC and 0.62 for individuals with high SSC which is 17.3% less. The average number of laughs is 2.38 for individuals with low SSC while it lies at 1.99 for individuals with high SSC which is 16.39% less. The average amusement rating however was with 2.13 higher for individuals with high SSC than for individuals with low SSC which had an average amusement rating of 2.07. This is 2.9% more and does not correspond with the results of the study described in {cite}`muraven1998self`. 

```{figure} ./images/funny_ssc_defined.png
---
name: funny-ssc-defined
---
Humorous Videos (SSC Defined)
```

A further result of the simulated experiment is, that the average number of smiles and laughs as well as the average amusement rating is more extreme if characteristics of individuals with high or low SSC are described to the LLM. In the first simulation run, the generated ratings of high SSC individuals were on average 40.95% lower as the ratings for low SSC individuals. In the second simulation run, the ratings for high SSC individuals were on average only 10.26% lower than for low SSC individuals. 

Furthermore, we simulated the experiment described in {cite}`schmeichel2007attention` using LLMs. Figure [](gruesome-ssc-characteristics) shows our simulation results by showing the reported feelings depressed, tense, dissatisfied, anxious, sorry as well as a score of the emotion visibility to outside people. The results were produced by describing the characteristics of an individual with high SSC or low SSC to the LLM before it was asked to generate the ratings. It is shown that a significant difference between individuals with high SSC (depressed: 3.65, tense: 8.16, dissatisfied: 6.22, anxious: 6.21, sorry: 3.47, emotions visible: 7.18) and individuals with low SSC (depressed: 20.12, tense: 37.2, dissatisfied: 28.96, anxious: 38.40, sorry: 11.13, emotions visible: 39.68) exists. This does not comply with the results of the study described in {cite}`schmeichel2007attention`, as the participants felt the emotions roughly to the same extend. Individuals with high SSC were only more successful in controlling their emotions to outside people. In our experiment simulation, persons with high SSC felt the emotions on average 78.22% less intense than persons with low SSC. However, the simulated experiment also allows the conclusion, that persons with high SSC are more capable of hiding their emotions to outside people. This does comply with the experiment conducted by the researchers {cite}`schmeichel2007attention`.

```{figure} ./images/gruesome_ssc_characteristics.png
---
name: gruesome-ssc-characteristics
---
Gruesome Videos (SSC Characteristics)
```

Figure [](gruesome-ssc-defined) shows the same simulated experiment but this time, no characteristics of persons with high or low SSC were described to the LLM. Instead the LLM was only told if it should simulate a person with high or low SSC. The results of the simulation also showed a significant difference between individuals with high SSC (depressed: 3.74, tense: 7.32, dissatisfied: 5.98, anxious: 5.86, sorry: 3.48, emotions visible: 5.61) and individuals with low SSC (depressed: 13.65, tense: 22.36, dissatisfied: 18.21, anxious: 20.63, sorry: 11.03, emotions visible: 30.29). This does also not comply with the results of the experiments described by the researchers {cite}`schmeichel2007attention` since the experienced emotions were felt 69.41% less for individuals with high SSC than for individuals with low SSC. However, this experiment also shows that persons with high SSC have a better ability to control their emotions.

```{figure} ./images/gruesome_ssc_defined.png
---
name: gruesome-ssc-defined
---
Gruesome Videos (SSC Defined)
```

Also, for those two experiment simulations it is shown that the results are more extreme if characteristics of high or low SSC individuals are described to the LLM. While for the first simulation run, high SSC individuals experienced on average 78.22% less emotions than low SSC individuals, in the second simulation it was only 69.41%.

(proposition-2-2-result)=
## Proposition 2.2