# RAG – Retrieval Augmented Generation

RAG is a type of LLM that uses a combination of a language model and a knowledge base to generate answers to questions.

The language model is used to generate the answer, while the knowledge base is used to retrieve relevant information to help the language model generate the answer.

## Embeddings
Vector embeddings are a type of representation that captures the semantic
meaning or context of words or sentences in a compact form. Essentially vectors of
real numbers (floats), where each dimension could represent a different feature that
captures something about that concept’s meaning.

## Chunking
Chunking is a process used to enhance the efficiency and accuracy of information
retrieval. In RAG apps, the input text is broken down into smaller, manageable units
called “chunks.” These chunks can be sentences, paragraphs, or by punctuation
marks. This approaches enhances the retrieval state in efficiency, accuracy and
scalability.

## Vector Stores

A vector store is a type of database that stores high-dimensional vector data and
provides query capabilities on those vectors such as similarity search, where the
goal is to find the most similar documents or items to any given query. Vector search
helps LLMs find similar information within their vast datasets using embeddings.

## Max Marginal Relevance (MMR)
Originally proposed in 1998, MMR refers to a technique by which relevant facts
provided by the retrieval step are reordered to create a more diverse set of facts.
This is most useful in critical RAG pipelines where many matching text chunks, from
multiple documents, are very similar or exactly the same.

## Reranking
Reranking is the process of re-assessing and re-ordering an initially retrieved set of
documents to enhance the relevance of the final set of documents used in the
generation process of RAG systems. It is used in a two-staged RAG pipeline where a
reranker algorithm is used to examines the details and contextual relevance of each
in the initial set of retrieved documents to ensure it does not contain many irrelevant
or marginally relevant entries due to the broad nature of the search.


# Process of Building a RAG Application

1. Define scope and data:
Choose target tasks, response format, SLAs (latency/accuracy).
Collect and clean source documents (PDFs, HTML, DB dumps, notes).

2. Chunking / preprocessing:
Split documents into chunks (sentences/paragraphs, semantic segs).
Normalize text, remove noise, keep provenance metadata.

3. Create embeddings:
Pick an embedding model (Sentence Transformers, OpenAI embeddings, etc.).
Encode chunks into vectors; store chunk id and metadata with each vector.

4. Vector store & indexing: 
Choose vector DB (FAISS, Milvus, Pinecone, Chroma, Weaviate).
Index vectors, tune index parameters (distance metric, shards).

5. Retrieval strategy:
Implement similarity search (k-NN) for candidate chunks.
Add filters/metadata queries to narrow scope (dates, source, tags).

6. Reranking / MMR:
Optionally rerank candidates with a cross-encoder or MMR to reduce redundancy and improve relevance.

7. Prompt design / context assembly:
Design prompt template that combines query + top-k retrieved chunks + instructions.
Control context size to fit model token limits; select chunks by relevance and provenance.

8. Generator integration:
Connect your LLM (API or local) to consume assembled context and generate final output.
Set generation params (temperature, top-p, max tokens, stop sequences, presence/frequency penalties).

9. Grounding & attribution:
Include provenance citations in responses.
Implement fallback behavior for low-confidence retrievals (e.g., say “I don’t know”).

10. Evaluation & iterating:
Define metrics: accuracy/ROUGE/BLEU, faithfulness, hallucination rate, latency.
Run human evaluation and automated tests; tune retriever, reranker, prompt template.

11. Optimization & production concerns:
Cache frequent queries, batch embedding calls, shard vector store.
Monitor cost, latency, and correctness in production.
Add logging, observability, and retraining/update pipelines for new documents.

12. Security & compliance: 
Ensure data privacy, access control, and sanitize sensitive content.
Maintain versioning and rollback for model and index updates.

Quick tool suggestions: LangChain/AutoGen for orchestration, FAISS/Chroma/Pinecone/Milvus for vector stores, sentence-transformers or OpenAI embeddings, cross-encoders for reranking