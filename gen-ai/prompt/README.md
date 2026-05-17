# Prompt

    prompt -> Model (LLM) -> completion

- prompt: the text passed to the llm
- inference: the act of generating text
- completion: output text

## context window

The place where input prompt passed to the model. (typically few thousand words)

## prompt engineering

the first request will not give you the right result, you revise the language multiple times to get better output, this process is called prompt engineering.

Develop and improve the prompt is called prompt engineering.

## In context learning (ICL)

Provide examples inside the context is called in-context learning.

### zero shot inference

Input data included in the prompt.  Preferred in larger models.

    Prompt                          Model                   Completion
    
    Classify this review:                               Classify this review:
    I loved this movie!             --> LLM -->         I loved this movie! 
    Sentiment:                                          Sentiment: Positive


### one shot inference

Single example included in the prompt.  Preferred in smaller models.

    Prompt                          Model                   Completion
    
    Classify this review:                               Classify this review:
    I loved this movie!             --> LLM -->         I loved this movie! 
    Sentiment: Positive                                 Sentiment: Positive

    Classify this review:                               Classify this review:
    I dont like this chair.                             I dont like this chair.
    Sentiment:                                          Sentiment: Negative


### few shot inference

Multiple examples included in the prompt.  Preferred in smaller models.

    Prompt                          Model                   Completion
    
    Classify this review:                               Classify this review:
    I loved this movie!             --> LLM -->         I loved this movie! 
    Sentiment: Positive                                 Sentiment: Positive

    Classify this review:                               Classify this review:
    I dont like this chair.                             I dont like this chair.
    Sentiment: Negative                                 Sentiment: Negative

    Classify this review:                               Classify this review:
    This is not great.                                  This is not great. 
    Sentiment:                                          Sentiment: Negative


Note: Remember the context window size.  So any situation that goes beyond 5 or 6 examples then use fine-turning.