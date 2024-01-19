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

(proposition-2-2-result)=
## Proposition 2.2