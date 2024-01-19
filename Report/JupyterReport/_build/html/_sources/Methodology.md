# Method

This chapter describes the generation of the data sets and the analysis logic of our research. As described in [](methodological-approach), [](proposition-2-1) and [](proposition-2-2) of the AMUSE model were simulated using LLMs.

(proposition-2-1)=
## Proposition 2.1

Proposition 2.1 suggests that individuals with high SSC exhibit an enhanced ability of downgrading their emotional responses to external stimuli compared to those with low SSC{cite}`reinecke2021media`. The initial paper referenced several experiments which concluded in this proposition. The following paragraphs describe the conducted experiments and how they were reproduced in our research using LLMs. 

Researchers {cite}`muraven1998self` have demonstrated that individuals with low SSC produce stronger affective reactions to humorous media content relative to those with high SSC. In their study, participants were primed to either posess high or low SSC, exposing them to comedic videos while instructing them to restrain their emotional expressions during facial recording. The number of smiles and laughs was counted by raters who also provided a general rating of the participant's success in controlling emotions. To replicate this experiment utilizing LLMs, we leveraged the search terms `#skit #funny` and `#standupcomedy` to retrieve YouTube Shorts. Eighty-nine video descriptions were obtained, serving as input for our LLM simulation. We employed the [](methodological-approach) outlined earlier to prepare the LLM and requested ratings from it for each designated individual. Following promt was used to replicate the described experiment:
```text
You are watching a YouTube short and while you are watching the video, you try to hide your emotions to outside people. The YouTube short is described as follows:

<YouTube Short description of LLM>

You should output the number of your smiles and laughs while watching the video and should rate your overall externally visible amusement between 1 to 5. Output only the three fields in JSON only. Your answer must not include any further text or explanations.
```
Consequently, the LLM generated a JSON object for each query, resulting in a comprehensive dataset. An exemplary JSON output is illustrated below:
```json
{
    "smiles": 3,
    "laughs": 5,
    "amusement_rating": 2
}
```

According to research conducted by {cite}`schmeichel2007attention`, individuals with high SSC demonstrate superior capability in suppressing emotional expressions when exposed to disturbing videos, such as gruesome video clips, compared to those with low SSC. This finding was derived from an experiment where participants were first primed with varying levels of SSC through memory tasks, then presented with a gruesome video, and subsequently evaluated for their emotional states via self-reported ratings on a 1-5 scale for feelings of depression, tension, sadness, dissatisfaction, and anxiety. Additionally, trained judges assessed the visibility of their emotions on a 1-111 scale. To replicate this study using LLMs, we collected 96 YouTube Shorts employing the search terms `slaughterhouse #brutal` and `slaughter brutal`. Following the same methodology as described in [](methodological-approach), the LLM was prepared and tasked with generating ratings for each individual as follows:

```text
You are watching a YouTube short and while you are watching the video, you try to hide your emotions to outside people. The YouTube short is described as follows:

<YouTube Short description of LLM>

You should rate between 1 to 5 how depressed, tense, sorry, dissatisfied, and anxious you felt. Also provide a number between 1 to 111 how much your emotions were visible to outside persons. Output all six fields in JSON with the field names "depressed", "tense", "sorry", "dissatisfied", "anxious" and "emotions_visible". Your answer must not include any further text or explanations.
```
An exemplary JSON output is illustrated below:
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