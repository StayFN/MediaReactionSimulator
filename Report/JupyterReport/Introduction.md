# Introduction

## Overview
<!-- brief explanation of the topic -->

## Topic Relevance
<!-- Topic relevance -->

(methodological-approach)=
## Methodological Approach
<!-- Methodological approach -->
In order to evaluate the efficacy of Large Language Models (LLMs) in simulating human-like cognition, we focused on the AMUSE model's processing phase (Phase 2){cite}`reinecke2021media`. Specifically, we explored the feasibility of employing LLMs to replicate the propositions 2.1 and 2.2, which pertain to self-control in first-layer appraisal processes. To do so, we attempted to reproduce the social experiments detailed in the original papers using the *HuggingChat*[^1] LLM. Our methodology consisted of four stages: collecting relevant media, describing the media, simulating the propositions with the LLM, and analyzing the results.

The first phase of our study involved gathering media resources in the form of YouTube Shorts. To accomplish this, we developed a Python script that queried YouTube Shorts using a specific search term. The script then extracted various metadata for each resulting Short, including the title, description, channel title, publication date, duration, words per second, number of views, likes, and comments. Additionally, we retrieved video categories, the top 10 comments, and transcripts for each Short. All of this information was subsequently stored for use in the media description phase.

In the second phase, we employed the *HuggingChat* LLM to craft descriptions for the media gathered during the initial stage. With the majority of the collected information, the LLM generated summaries averaging 100 words in length. The prompt guiding this process was structured to enable the AI model to encapsulate the content of the media in a few short sentences. Following promt was used:
```text
You are a copywriter, create a 100 word summary of what this Youtube Short is about. Provide a neutral description. The summary should describe the overall atmosphere and pace of the video. It should also highlight important events from the video. Do not include any statements about a viewers response to the content or the overall viewing experience. Output the raw summary text.

Title: <title of the Short>
Channel: <title of the channel>
Transcript: <transcript of the Short>
Comments: <a list with the top 10 comments>
Category: <video category>
```
The resulting descriptions were saved to be processed in the next phase.

In the third phase, we utilized the *HuggingChat* LLM to simulate experiments that yielded the underlying propositions. We aimed to assess how individuals with varying levels of self-control would perceive and express emotions when exposed to similar stimuli. To achieve this, we devised two distinct methods to prepare the LLM. Firstly, we defined specific characteristics that distinguish individuals with high state self-control (SSC) and those with low SSC. Our definition of high SSC included attributes such as being goal-oriented, emotionally stable, self-aware, disciplined, resilient to setbacks, flexible, adaptable, possessing strong time management skills, nurturing solid relationships, exhibiting good decision-making abilities, and maintaining mental and physical well-being. Conversely, we characterized low SSC by attributes like impulsivity, difficulty with delayed gratification, lack of self-discipline, emotional instability, poor decision-making, susceptibility to addiction, and proclivity towards procrastination. During the first run, we programmed the LLM to emulate individuals with either high or low SSC by providing it with these defining features. In the second iteration, we simplified the process by instructing the LLM to simulate either a high or low SSC individual. Subsequently, we provided the LLM with the previously created YouTube Short descriptions and tasked it with rating the intensity and external visibility of emotions corresponding to each experimental scenario. Finally, the LLM was asked to export its responses in JSON format for further analysis.

In the last phase, the results of the previous proposition simulation were cleaned to exclude any malformed data produced by the LLM. Afterwards, the data was graphically prepared.

[^1]: <https://huggingface.co/chat/>