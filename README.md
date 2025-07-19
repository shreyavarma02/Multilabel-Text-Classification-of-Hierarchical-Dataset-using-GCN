Hierarchical Tweet Classification using GCN:
- This project applies Graph Convolutional Networks (GCNs) to classify tweets from the OLID dataset using a three-level hierarchical structure. Tweets are represented as nodes in graphs built from text similarity, and classified using a GCN at each level.

Objective:
Classify tweets through 3 hierarchical levels:
- Level 1 (subtask_a) – Offensive (OFF) vs Not Offensive (NOT)
- Level 2 (subtask_b) – Targeted (TIN) vs Untargeted (UNT)
- Level 3 (subtask_c) – Directed at Individual (IND), Group (GRP), or Other (OTH)
Each level has its own graph, GCN model, and training process.

Methodology:
- TF-IDF + Cosine Similarity: Connect tweets with similarity > 0.7 to form edges.
- Three Graphs (G1, G2, G3): One for each classification level.
- Node2Vec: Learn node embeddings based on graph structure.
- GCNs: 4-layer Graph Convolutional Network trained on each graph to classify tweets by label level.
