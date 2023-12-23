# Advanced RAG Pipeline
Advanced RAG (Retrieval Augmented Generation) attempts to improve retrieval results and performance.
Consists of code from the introductory course on Building and Evaluating Advanced RAG by DeepLearning.AI: [Course](https://learn.deeplearning.ai/building-evaluating-advanced-rag/lesson/1/introduction)


## Examples

- Sentence window retrieval.
- Auto-merging retrieval.

### Sentence window retrieval
Adds n sentences before and after the sentence retrieved when performing the retrieval.
Different window sizes should be evaluated and compared with regardas to the RAG Triad.
- If the sentence window is too low: Context Relevance tends to be low -> Causes Groundedness to be low, because the model starts to rely on its pre-trained knowledge.
- If the sentence window is too high: Groundedness tends to drop -> As the context size increases, the LLM might be overwhelmed and starts to rely on its pre-trained knowledge instead of only using the retrieved context.

### Auto-merging retrieval
Divides context into smaller sub-chunks. If a majority of chunks belonging to a parent chunk is retrieved, the parent chunk is retrieved instead.
- Increasing the number of levels may improve Context Relevance, as well as decrease the total cost.


## Reranking
Using a reranker is a good way to balance the tradeoff between precision and efficiency.
Precomputing documents and storing them in a vector database, allows for efficient first retrieval of pretty relevant documents.
Recomputing the relevance of the retrieved documents using another embedding allows the second retrieval to retrieve precices documents.


## Evaluation
Uses TruLens to evalute the RAG performance using the RAG Triad, consisting of:
1. Answer Relevance. (Compares input and output to answer: Is the final response useful?)
2. Context Relevance. (Compares the input and intermediate results to answer: How good is the retrieval?)
3. Groundedness. (Compares the intermediate results and the output to answer: )

Builds a feedback recorder (dashboard) detailing RAG Triad scores on each query evaluation using Streamlit.

### Other evaluation metrics TruLens
Honest:
- Answer relevance
- Context Relevance
- Groundedness
- Embedding distance
- BLEU, ROUGE, ...
- Summarization quality
- Custom evaluations

Harmless:
- PII Detection
- Toxicity
- Stereotyping
- Jailbreaks
- Custom evaluations

Helpful:
- Sentiment
- Language mismatch
- Conciseness
- Coherence
- Custom evaluations