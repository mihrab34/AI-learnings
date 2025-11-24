# General Buzzwords in the LLM(Large Language Model) space

## Transformers Architecture

Transformers are a type of neural network architecture that is widely used in
natural language processing and language modeling.

***Characteristics***

- Applies attention which allows the model to consider the importance of all
words in a sentence simultaneously.

- Encoders and decoders are two parts of the transformer architecture. They are used to encode the input sequence and decode the output sequence.

- The transformer architecture is used in various tasks like machine translation, question answering, and text summarization.

## Attention

Attention mechanisms are fundamental components that allows transformer based
AI models to model to focus on different parts of the input sequence dynamically,
allowing it process and understand text more effectively.

***Characteristics***

- Introduced by Vaswani et al. in the paper  [“Attention is All You Need”](https://arxiv.org/pdf/1706.03762)


- With self-attention or scaled dot-product attention the model computes
attention scores between each pair of tokens in the input sequence. These
scores determine how much focus to allocate to each token when generating
the output.

## GPT
GPTs (Generative Pre-trained Transformers) are transformer based deep learning
language models designed to understand and capable of generating human-like
text. GPT is the underlying technology behind OpenAI’s ChatGPT.

## Open/Closed Source LLMs
The term “open source” refers to software source code that is publicly available
under free-to-use licenses and in AI refers to models whose weights are made publicly
available for use. See open source AI Definition for more details. [OSAID](https://opensource.org/ai/open-source-ai-definition)

Inversely, “closed source” refers to software source code that is publicly behind a
pay-wall through communication means such as APIs. e.g. OpenAIs ChatGPT,
Anthropics Claude, Dalle-E, Mistral AI(closed)

## Tokens

Tokens are the basic units of text an LLM processes. It can be single characters,
individual words, or even subwords, and the choice of tokenization strategy depends
on the use case and application.

## Hallucination
In artificial intelligence (AI), an hallucination effect or artificial
hallucination aka confabulation or delusion is a confident response by
an AI that does not seem to be justified by its training data.

## Prompt Engineering
Prompt Engineering is a process involved with designing, refining, and
optimizing the input/system prompts that are well-suited to a specific task
in order to achieve a tailored outputs. Some specific techniques in prompt
engineering include: rephrasing, format specification,
leading Information

Some prompting techniques include:

- **Few-Shot Learning**:
Few-shot Prompting/Learning, aka in-context learning is a leading information prompting technique that allows a model to process multiple labeled examples before attempting a task. The purpose is to increase the LLMs capabilities to respond in context, expand the knowledge base and provide alignment.

- **Chain of Thought**:
Chain of Thought Prompting is a prompting technique that allows a model to reason step by step. The purpose is to allow the llm break down complex tasks into sequential reasoning steps. This improves the model's ability to handle complex reasoning and provide more accurate responses.

- **Instruct**:
Instruct Prompting is a prompting technique that allows a model to respond in a structured way or behaviour by providing instructions to guide the model. It is Useful for getting consistent, formatted responses and often used together with few-shot learning / chain of thought.

- **One Shot**: This technique provides a single labeled example before asking the model to perform the task. It is a middle ground between zero-shot and few-shot prompting. It helps guide the model with minimal context.

- **Zero Shot**: This technique asks the model to perform a task without any examples or prior demonstrations. It relies on the model's pre-trained knowledge alone.   It is quick but may be less accurate for complex or specialized tasks.

## FineTuning
Fine-tuning in LLMs is a transfer learning technique where a pre-trained model is further trained on a specific dataset for downstream tasks. There are various techniques for performing fine-tuning including AdaLoRA, LORA, QLORA etc.
Fine-tuning can be done on the entire neural network, or on only a subset of its layers,
in which case the layers that are not being fine-tuned are “frozen” (not updated).


## Inference

In LLMs, inference is the operational process of generating output.
LLMs may not generate the same result every time because inference is a stochastic operation.

input[trained model] --> sequence of tokens --> next predicted token[output]