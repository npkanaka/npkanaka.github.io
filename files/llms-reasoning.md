
**Title: Comparative Investigation of Grokking in Transformers and Beyond: A Study on Reasoning**

**Abstract:**
Large Language Models (LLMs) have transformed natural language understanding and generation but still face significant challenges in logical deduction, systematic reasoning, and generalization. These reasoning tasks often reveal weaknesses in current models, resulting in hallucinations and inconsistent outputs despite fluent language. Existing approaches mainly address reasoning capabilities through high-level interventions, overlooking core model limitations. Grokking—where models unexpectedly generalize after prolonged training beyond overfitting—offers a promising avenue for studying reasoning dynamics. This research systematically explores how dataset design and model architectures influence grokking’s emergence and efficiency. The study finds that GPT and LLaMA architectures exhibited grokking on the comparison task, though LLaMA did so more slowly than GPT. In contrast, RWKV and Mamba failed to grok under identical conditions. The research also examines dataset characteristics affecting grokking performance, observing that a minimum threshold of distinct entities is essential for effective grokking, while lower attribute value ranges accelerate generalization. These findings deepen understanding of reasoning tasks’ interaction with training dynamics and provide practical guidance for enhancing generalization in language models.

---

### Overview
This project aims to deepen our understanding of the phenomenon of *grokking* in neural networks—an unexpected, often sudden, improvement in generalization ability following prolonged training. We will conduct experiments across various neural network architectures, focusing on their ability to solve complex reasoning tasks and the inductive biases that shape these abilities. By systematically analyzing and comparing the performance of architectures such as transformers, selective state space models (SSMs), and linear attention models, we aim to uncover how unique structural properties influence generalization and grokking behavior.

### Objectives

1. **Investigate Inductive Biases and Grokking Patterns Across Architectures**
   - Analyze how the inherent structural characteristics of different neural network architectures affect their grokking behaviors on a set of complex reasoning tasks.
   - Compare discrete attention mechanisms in transformers with continuous state transitions in selective state space models to evaluate how these differences impact generalization patterns.

2. **Expand Reasoning Task Dataset for Enhanced Experimental Validity**
   - Curate and expand datasets to include a wider range of reasoning tasks with variable complexity. This enhanced dataset will provide a comprehensive testbed to rigorously assess model performance and grokking patterns across architectures.

3. **Experiment with Cross-Layer Knowledge Sharing, Memory Augmentation, and Recurrence in Transformers**
   - Conduct experiments within transformer architectures that incorporate cross-layer knowledge sharing, memory augmentation, and explicit recurrence mechanisms.
   - Assess whether these architectural enhancements improve generalization, potentially accelerating the onset of grokking and broadening the practical applications of transformers.

4. **Explore Linear Attention Models for Recurrence-Like Mechanisms in Grokking**
   - Investigate the impact of recurrence-like mechanisms inherent in linear attention models and their effect on grokking behaviors.
   - Test whether the sudden generalization observed in grokking depends strictly on traditional attention mechanisms or if it can emerge from other forms of attention structures.

5. **Investigate Practical Strategies to Accelerate Grokking in In-Context Learning**
   - Focus on in-context learning dynamics within the grokking framework, aiming to identify practical strategies that can hasten this phenomenon.
   - Optimize learning dynamics and generalization to support broader applications, such as few-shot learning, where rapid generalization and efficient task adaptation are crucial.

### Methodology

#### ⏳ (Under review)

### Expected Outcomes

- **Enhanced Understanding of Inductive Biases in Grokking**: Insights into the role of architecture-specific inductive biases in grokking behaviors, with detailed comparisons across diverse models.
- **Identification of Accelerative Factors in Grokking**: Documentation of architectural and methodological changes (e.g., cross-layer sharing, memory augmentation) that facilitate quicker generalization and grokking.
- **Broader Applicability of Grokking Insights**: Practical strategies to optimize learning dynamics in architectures suitable for real-world applications, especially in tasks requiring rapid adaptation through in-context learning.

### Impact
The findings from this research can contribute to the development of more robust, generalizable AI models capable of efficient reasoning and learning dynamics. By understanding the factors that drive grokking, we can apply these insights to improve model architectures for applications where adaptive learning and rapid generalization are paramount, including language understanding, automated reasoning, and decision-making systems in complex environments.
