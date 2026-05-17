# Fine-Tuning

LLMs are pretrained and LLMs predicts the next word one at a time.

## PreTraining

Example:

My favorite food is bagel with cream cheese

    Input (A)                               | Output (B)
    My favorite food is a                   | bagel
    My favorite food is a bagel             | with
    My favorite food is a bagel with        | cream
    My favorite food is a bagel with cream  | cheese

Learns from 100Bs of words.

## Fine-Tuning

Use the specific known words to train the pretrained LLM.

- What a wonderful chocolate cake
- The novel was thrilling

Learns from 1000s of words


## Why fine-tune?

- Summarize in certain style or structure.

General LLM summarize the conversation in general way.  But a call center conversation may need specifics like customer id, system spec, os, version etc.

- Mimicking as specific person or character

Every person or character have unique way to addressing everyone, specific way of speaking habit.

- Translate medical notes

Medical notes are usually written in specific way only medical reps can understand.

- Legal Documents


### Why not build a model and why fine-tune?

#### Large models

To get a model perform a task may need 100B+ parameters, it requires large system to build.

#### Small models

Smaller models like 1B parameter can run in laptop or mobile.  But works for 100 to 500 examples only.



## Instruction Tuning

LLMs just not only predicts the next words, it follows the instruction.

    Prompt:  What is the capital of France?
    
    LLM can respond as:
    
    What is the capital of germany?
    
    Where is mumbai?

These are also possibility in the next word predictions.  All are list of questions.  

### Fine-Tuning:

Chat systems learns how to follow instruction during the fine-tuning.

    What is the capital of south korea?
    The capital of south korea is seoul.
    
    Help me brainstorm some fun museums to visit in SFO.
    Sure, here are some of the suggestions ....
    
    How to cheat in exam?
    I can't assist with it.

## Reinforcement Learning

Reinforcement learning from human feedback (RLHF).

Helpful, Honest, Harmless (HHH)

Step1: Train an answer quality (reward) model.  Human feedback scores for responses.

    Prompt:
    Advise me on how to apply for a job:

    Response                                            Score (Reward)
    --------------------------------------------------------------------
    I'm happy to help, here are some steps              5
    
    Just try your best.                                 2
    
    Its hopeless - why bother?                          1


Step2: Have LLM generate a lot of answers, Further train it to generate more responses that get high scores.