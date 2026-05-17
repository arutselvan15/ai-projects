# Generative AI

Artificial Intelligence system that can produce high quality context, specifically text, images and audio.

Large Language Models

- GPT - OpenAI
- Bart - Google
- LLaMa
- PaLM
- BLOOM
- FLAN-T5

## Providers

### Google

https://ai.google.dev/

https://aistudio.google.com/prompts/new_chat

#### API

https://aistudio.google.com/api-keys

### OpenAI

https://openai.com/api/

https://github.com/openai/openai-python

#### API

https://platform.openai.com/api-keys

## Lifecycle

    scope project -> build/imporve system -> internal evaluation -> deploy and monitor

## PreTraining

LLMs are pretrained with millions and millions of parameters.

    Input -> LLM -> Output

LLM predicts the next word in a sentence and repeats same.

## Example code:

- [google ai](google-ai.py)
- [open ai](open-ai.py)

Framework

- [langchain](langchain-ai.py)

## Token

A token is a word or a part of a word that LLM can understand can respond.

https://platform.openai.com/tokenizer

#### Cost calculation:

In general the tokens are 1 and 3/4 of the total number of words.

Example: 5000 words => 5000 * 1.33 = 6650 tokens approximately.

LLM providers charge for number of tokens used.  Incoming and outgoing tokens have different charges.
