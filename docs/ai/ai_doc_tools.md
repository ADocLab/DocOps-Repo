# AI in Documentation

This section explores how AI can assist documentation workflows:

- Automating rewrites and editing  
- Generating structured docs  
- Extracting metadata  
- Ensuring consistency  
- Detecting missing sections  
- Improving clarity and accuracy  

# Semantic Search

**Definition**: Search done based on context or meaning rather than literal text search is called sematic search.

# Steps to achieve Sematic search

The search is broken into 4 parts:

- **Chunking**: Breaking long documents into smaller sections yet retaining the original meaning before converting them into embedding. This helps in load reduction on AI and make optimum use of resources.

!!! Example of a Chunk
        Chunk_Text: "Checkout repo copies the code from GitHub into the VM."
        Metadata:
            url: /docops/ci_cd_pipeline#checkout
            section: Step 1
            page: CI/CD Pipeline

- **Embeddings**: A mathematical way of representing the meaning of text as numbers in high-dimensional vector space, similar ideas form clusters and related chunks end up close to each other.

- **Vector Database**: Semantic search creates a dense vector and ingests data into a vector index.
Vector DB = a database designed to store meaning (embeddings). “A vector database is not rows and columns. It stores high‑dimensional embeddings and uses approximate nearest‑neighbor indexes (like HNSW or IVF) to retrieve the most semantically similar vectors. It is a search engine for meaning.”

- **K Nearest Neighbor (k-NN) search**: Find the vectors that are closest to the query vector. Semantic search uses k‑NN to retrieve nearest vectors.

## Chunking in detail

### Why?
Large pieces of data need to be broken down into smaller, semantically coherent chunks because embedding models have input length limitations

OpenAI ~512 tokens
BERT ~1,000 tokens
Cohere ~4,000 tokens (latest ones)

That’s not enough for entire docs.
So systems must chunk long documentation pages before embedding.

### What?
Chunks are usually a paragragh, sub-section, heading with body, or any small unit that contains just one idea.
Chunks are broken into pieces that are well defined with clear boundary walls, such chunks produce vectors that bring back accurate results.
