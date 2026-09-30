# Embeddings & Vector Search

Embeddings map content into numeric representations useful for semantic similarity/search.

## Pipeline
Content → chunk/metadata → embedding → vector index → query embedding → nearest candidates → optional rerank/filter.

## Design questions
Chunking, metadata filters, freshness, access control, embedding version, retrieval recall/precision and deletion/update behavior.

## Important
Vector similarity is not authorization. Filter/enforce access using trusted metadata/security boundaries.

Vector databases are useful when semantic retrieval fits the problem; ordinary keyword/SQL search may be simpler for exact structured needs.
