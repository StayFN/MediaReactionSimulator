# Method

This chapter describes the generation of the data sets and the analysis logic of our research. As described in [](methodological-approach), [](proposition-2-1) and [](proposition-2-2) of the AMUSE model were simulated using LLMs.

(proposition-2-1)=
## Proposition 2.1

Proposition 2.1 suggests that individuals with high SSC are more capable of downgrading their emotional responses to external stimuli than persons with low SSC{cite}`reinecke2021media`. Several experiments were conducted to investigate this phenomenon. The following paragraphs describe the conducted experiments and how they were reproduced using LLMs. 

{cite}`muraven1998self` have conducted experiments which showed that individuals with low SSC produce stronger affective reactions to humorous media content than individuals with high SSC. In this experiment, participants were prepared to either have high or low SSC, were exposed to humorous videos, and were told to supress their emotions while they were videotaped. The number of smiles and laughs was counted by raters who also provided a general rating of the participants success in controlling emotions. To reproduce this experiment, the search terms `#skit #funny` and `#standupcomedy` were used to query for YouTube Shorts. Those search terms resulted in 89 YouTube Short descriptions which were used to simulate the experiment. To produce results, the LLM was prepared as described in [](methodological-approach) and was asked to output its rating for every defined individual as follows: 
```text
You are watching a YouTube short and while you are watching the video, you try to hide your emotions to outside people. The YouTube short is described as follows:

<YouTube Short description of LLM>

You should output the number of your smiles and laughs while watching the video and should rate your overall externally visible amusement between 1 to 5. Output only the three fields in JSON only. Your answer must not include any further text or explanations.
```
As a result, the LLM produced a JSON object for every query. In the following an example JSON output is shown:
```json
{
    "smiles": 3,
    "laughs": 5,
    "amusement_rating": 2
}
```

{cite}`schmeichel2007attention` have conducted an experiment which showed that individuals with high SSC can inhibit the expression of emotions better when watching gruesome video clips than individuals with low SSC. Before the experiment, participants were prepared to either have high or low SSC by completing different memory tests. In the next step they were asked to watch a gruesome video. Afterwards, they were asked to rate how depressed, tense, sorry, dissatisfied, and anxious on scales from 1 to 5 they were. Moreover, judges rated the extend to which their emotions were visible to outside persons on a scale from 1 to 111. To reproduce this experiment, 96 YouTube Shorts were collected by using the search terms `slaughterhouse #brutal` and `slaughter brutal`. The LLM was prepared as described in [](methodological-approach) and was asked to output its rating for every defined individual as follows: 
```text
You are watching a YouTube short and while you are watching the video, you try to hide your emotions to outside people. The YouTube short is described as follows:

<YouTube Short description of LLM>

You should rate between 1 to 5 how depressed, tense, sorry, dissatisfied, and anxious you felt. Also provide a number between 1 to 111 how much your emotions were visible to outside persons. Output all six fields in JSON with the field names "depressed", "tense", "sorry", "dissatisfied", "anxious" and "emotions_visible". Your answer must not include any further text or explanations.
```
The resulting JSON looked like follows:
```json
{
    "depressed": 3,
    "tense": 5,
    "sorry": 2,
    "dissatisfied": 3,
    "anxious": 5,
    "emotion_visibility": 20
}
```

(proposition-2-2)=
## Proposition 2.2

[^1]: <https://huggingface.co/chat/>