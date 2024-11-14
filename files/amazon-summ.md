
# LexPlus: Extractive Summarization Algorithm 

## Project Overview

The primary objective of this project was to develop an extractive summarization algorithm tailored to product-centric reviews for Amazon Research, with a focus on analyzing reviews for specific products rather than Amazon's service-oriented feedback. Our algorithm is build on the top of LexRank, a well-regarded graph-based method for computing lexical centrality in text summarization, specifically chosen for its effectiveness in multi-document extractive summarization tasks.

LexRank, originally introduced by Erkan and Radev in their research, provides a robust stochastic approach to calculate sentence centrality using a similarity graph, with vertices representing sentences and edges weighted by cosine similarity. We customized the model to identify key thematic sentences across clusters of product reviews, thus enabling concise, meaningful summaries for potential customers.

## Methodology

The summarization algorithm was implemented based on the following principles:

1. **Sentence Similarity and Graph Construction**: Each sentence in a review is represented as a node within a graph, and edges are weighted by cosine similarity, calculated from TF-IDF-modified vectors. Only sentences with similarity scores above a certain threshold are connected, enhancing sentence relevance within the graph.

2. **Degree and Eigenvector Centrality**: LexRank uses degree and eigenvector centrality to determine the importance of each sentence. While degree centrality is effective for identifying commonly used product descriptors, eigenvector centrality prioritizes sentences central to the thematic network of the reviews.

3. **Threshold Tuning for Similarity Scores**: Based on our experiments, we adjusted the similarity threshold to balance precision and recall of significant sentences within each cluster of reviews. A low threshold captures more relevant sentences without overloading the graph with noise.

4. **Continuous LexRank for Weighted Graphs**: We retain cosine similarity weights, allowing for more nuanced importance assessments in denser graphs. This weighted approach is especially beneficial for handling large clusters of reviews with subtle topic variances.

## Implementation

The algorithm was implemented using Python and integrated with the MEAD summarization toolkit to facilitate feature extraction, vector scoring, and ranking processes. Our MEAD-based configuration allowed us to fine-tune LexRank’s parameters to optimize summary quality across different product categories.

Key implementation components:
- **MEAD Custom Policy Configuration**: LexRank was added as a feature to the MEAD toolkit, along with auxiliary features like sentence position and length to enhance summary readability.
- **Iterative Convergence via Power Method**: The power method was applied to calculate the stationary distribution of the graph, ensuring convergence of centrality scores across review clusters.

## Results and Evaluation

The summarization model was evaluated using ROUGE scores against human-created summaries for product reviews. Our algorithm demonstrated superior performance compared to centroid-based methods and baseline models, achieving higher ROUGE-1 scores across various product categories.

- **Threshold Experimentation**: We observed that a 0.1 similarity threshold yielded optimal summaries, balancing content richness with relevance.
- **Comparison with Baselines**: Generated summaries consistently outperformed lead-based and random sentence extraction baselines, particularly in clusters with high thematic consistency.

The algorithm is robust against noisy data, making it well-suited for real-world applications with unstructured product review content.

## Conclusion

By focusing on centrality and sentence similarity, our algorithm delivers concise, relevant summaries, enhancing the user experience on Amazon’s platform by providing product insights at a glance. Future work could involve integrating sentiment analysis to adjust summarization based on review polarity, offering a more nuanced product portrayal.
