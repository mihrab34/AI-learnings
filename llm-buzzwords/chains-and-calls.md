# Chains and Calls Buzzwords

## Chains
A chain is a sequence of tasks that are executed in order to produce a final output.

Chains go beyond just a single LLM call, and /or sequences of calls (whether to an
LLM or a different utility). LLM chaining is the process of connecting large language
models to other applications, llms,tools, and/or services to produce the best possible
output from a given input and making it easier to handle complex tasks.

Langchain, AutoGen, HayStack, DarksuitAI and other frameworks provide a
standard interface for chains, lots of integrations with other tools, and end-to-end
chains for common applications.

**Calls**
A call is a request to an LLM or other tool to perform a specific task.

## Context Memory
Context Memory is the concept of persisting state between calls of a LLM
chain/agent. It gives the LLM chain, the capability to have conversational memory
aiding contextual understanding. Langchain, darksuitai and others provides a
standard interface for context memory and collection of memory implementations.

Google's recent paper [Nested Learning: The Illusion of Deep Learning Architectures](https://research.google/blog/introducing-nested-learning-a-new-ml-paradigm-for-continual-learning/) on context memory introduces a new paradigm that directly addresses limitations in current LLMs, including how they manage long-context memory and catastrophic forgetting. It provides a framework for building context-aware LLMs that can handle long-context memory. 

## LLM Parameters

Hyperparameters are like knobs and dials you can tweak to make your large language
model behave just how you want it.

**Characteristics**

- Temperature: This hyperparameter controls the randomness of the model’s output. A
temperature of 0 means always output the same response, it also controls the level
of creativity in the LLM’s output.

- Top-k: Setting a top-k limits the model’s output to the most probable tokens at each
step. This can help reduce incoherent or nonsensical output by restricting the model’s
vocabulary to a number of choices.

- Top-p: The top-p filters out words that do not meet a certain threshold (p). It lets the
model be a bit more diverse in what it says, but still keeps it from using super
unlikely words.

- Max tokens: This sets a cap on the maximum number of words the LLM should
generate.

- Stop: Stop words are usually set to stop token generation when they are
encountered.

- Presence penalty: The presence penalty is a hyperparameter that controls the
likelihood of the model generating words that have already been generated in the
past. it discourages the model from repeating any token that has already appeared appeared at least once in the output, promoting vocabulary diversity.

- Frequency penalty: same as presence penalty, but it applies a stricter penalty to tokens that have been used more frequently in the
past but compared to the presence penalty, it discourages tokens proportionally based on how frequently they've appeared, with more common tokens receiving stronger penalties.