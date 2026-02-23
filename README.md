# 📊 TOPSIS-Based Evaluation of Pre-trained Conversational Models

## 📌 Project Overview

This project evaluates multiple **Hugging Face pre-trained conversational AI models** using the  
**TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method.

The objective is to **select the best conversational model** by considering both **language quality** and **computational efficiency**, instead of relying on a single evaluation metric.

---

## 🎯 Problem Statement

Select the best **pre-trained conversational model** using **multi-criteria decision-making**.

The models are compared using the **TOPSIS algorithm**, which ranks alternatives based on their closeness to an ideal solution.

---

## 🤖 Models Evaluated

The following Hugging Face pre-trained models were used in this study:

- DialoGPT (Medium)
- BlenderBot (400M Distilled)
- BlenderBot (1B Distilled)
- FLAN-T5 (Base)
- GPT-Neo (125M)

All models are publicly available and designed for conversational or text generation tasks.

---

## 📊 Evaluation Criteria

Each model was evaluated using the following criteria:

| Criteria Name | Type (Benefit / Cost) | Weight | Description | Why It Matters |
|--------------|------------------------|--------|-------------|----------------|
| STS Score | Benefit | 0.30 | Benchmark semantic textual similarity score | Measures how well the model understands sentence meaning |
| Inference Time (seconds) | Cost | 0.20 | Time taken to generate embeddings | Faster models are better for real-time applications |
| Model Size (MB) | Cost | 0.20 | Memory required by the model | Smaller models are easier to deploy |
| Embedding Dimension | Cost | 0.10 | Length of output vector | Higher dimensions increase computation and storage |
| Cosine Similarity | Benefit | 0.20 | Similarity score between test sentences | Reflects semantic closeness between sentences |

The sum of all weights equals **1.0**, ensuring a balanced evaluation.

---



## 🧮 Methodology (TOPSIS)

The **TOPSIS** method was applied using the following steps:

1. Construction of the **decision matrix**
2. **Normalization** of criteria values
3. Assignment of **weights** to each criterion
4. Identification of **ideal best** and **ideal worst** solutions
5. Calculation of **Euclidean distances**
6. Computation of **closeness coefficient (TOPSIS score)**
7. **Ranking** of models based on TOPSIS score

The model with the **highest TOPSIS score** is considered the optimal choice.

---




## 📈 Results

The final output of the project includes:

- A ranked DataFrame containing:
  - TOPSIS Score
  - Rank of each model
- A bar graph visualizing TOPSIS scores for all models

The model ranked **1st** represents the best overall trade-off among all selected criteria.

---

## 🏆 Conclusion

Using the TOPSIS-based evaluation, the best pre-trained conversational model was selected by balancing both **model performance** and **computational constraints**.

This approach ensures a **systematic and fair comparison** and can be extended to evaluate other NLP models in future work.

---

## 🛠 Tools & Libraries Used

- Python  
- Hugging Face Transformers  
- Pandas & NumPy  
- Matplotlib  
- Google Colab  

---

