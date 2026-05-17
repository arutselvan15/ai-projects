## RAG 

Retrival Augmented Generation

### General Chatbot

Pretrained LLMs responses are generic based on this training data, These data are mostly public data.

In case private company questions the LLMs cannot answer or provide accurate response.

Prompt:  Is there parking for employees?

### Chatbot with RAG

Company documents:
- benefits
- leave policy
- facilities
- payroll etc.

Provide the context from the document to LLM and ask to answer the question.

Context: Parking policy - All employee may part on level 1 and 2 ...

Prompt:  Is there parking for employees?

LLM will respond and link to policy.


### Big Idea - LLM as reasoning engine

- LLM have a lot of general knowledge but don't know everything
- By providing context in the prompt we can ask LLM to read a piece of text then process it to get an answer
- We are using it as a reasoning engine to process information rather than using it as a source information


- Panda Chat
- AskYourPDF
- PDF.ai
- docAnalyzer.AI
- ChatPDF
- LightPDF
- Tactic