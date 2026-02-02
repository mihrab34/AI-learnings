# LLM Application Landscape and Everything In Between

## BUILDING BLOCKS OF AI INFRASTRUCTURES AND APPLICATIONS

### GEN AI Stack

**What is the GEN AI Stack**

The AI stack combines integrated tools,libraries, and solutions to create applications with generative AI capabilities,such as image and text generation. The components of the AI stack include programming languages, model providers, large language model (LLM) frameworks, vector databases, operational databases, monitoring and evaluation tools, and deployment solutions.

**High Level view of the GEN AI Stack**

Application(web apps, mobile apps) <-> Tooling (Data, Infra) <-> Compute (GPU and LLMs)

**Low Level view of the GEN AI Stack**

Programming Language (python, typescript etc) <-> Model Provider(Gemini, Claude, Qween, Huggingface etc) <-> LLM Orchestrators and Frameworks (Langchain, AutoGen, LlamaIndex) <-> Operational and Vector Database(mongoDB, postgresql etc) <-> Monitoring and Observability <-> Deployment

### RAG – Retrieval Augmented Generation

**What is RAG**

It is a system design pattern that leverages information retrieval techniques and generative AI models to provide accurate
and relevant responses to user queries by retrieving relevant data to supplement user queries with additional context combined as input to LLMs.

**How RAG works**

- RAG uses a combination of a language model and a knowledge base to generate answers to questions.

- The language model is trained on a dataset of questions and answers, and the knowledge base can be a collection of documents, a database, or a knowledge graph that the language model can use to generate answers.

- The language model is given a question as input, and it uses the knowledge base to retrieve relevant documents that are then used to generate the answer.

- The language model then uses the retrieved documents and the question to generate the answer.

- The answer is then returned to the user.

- The process is repeated until the user is satisfied with the answer.

**How do you retrieve data in RAG?**

- Lexical search or keyword search
- Semantic search
- Vector search : generate embeddings from text chunks or a data point and store them in vector DB

### LLM Evaluation

MONITORING AND MEASURING PERFORMANCE OF INTELLIGENT SYSTEMS

**What is LLM Evaluation?**
LLM evaluation, also referred to as ‘LLM Eval,’ is the systematic process of formulating a profile of foundation models
or their derived fine-tuned variants to understand and capture their performance on certain specialized or general-purpose
tasks, reliability in certain conditions, effectiveness in particular use cases, and many other evaluative measurement criteria that help in gaining an overview of a model’s overall ability.

**Why Even Evaluate?**

Build PRIME Applications

P
Performance
Profiling

R
Risk and
Responsibility

I
Iterative
Enhancement

M
Model
Benchmarking

E
Ethical
Safeguarding
