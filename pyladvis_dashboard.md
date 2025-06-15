# 📊 pyLDAvis Dashboard: Interactive Topic Model Visualization

This project uses **pyLDAvis** to create an interactive dashboard for visualizing topics extracted from video transcripts using **Latent Dirichlet Allocation (LDA)**.  

---

## 🚀 Overview

The pyLDAvis dashboard helps you:
- Explore the **distribution of topics** across your corpus.
- Understand how **distinct or overlapping** the topics are.
- Inspect the **most relevant words** that define each topic.

---

## 🗂️ Components of the Dashboard

The dashboard consists of two main panels:

### 1️⃣ **Intertopic Distance Map (Left Panel)**  
- Each **bubble** represents a topic.
- **Bubble size** indicates how common the topic is in the overall corpus (larger = more prevalent).
- **Bubble distance** shows similarity: topics closer together share more words.
- Well-separated bubbles indicate distinct, meaningful topics.

### 2️⃣ **Top Terms for Selected Topic (Right Panel)**  
- Displays the top words that define the currently selected topic.
- **Red bars:** Word frequency within the selected topic.
- **Blue bars:** Word frequency across the entire corpus.
- The **λ (lambda) slider** adjusts how words are ranked:
  - **λ = 1.0:** Terms ranked by probability within the topic.
  - **λ = 0.0:** Terms ranked by how unique they are to the topic.

---

## ⚙️ How It Works

✅ **Input:**  
- Trained Gensim LDA model  
- Corpus (Bag-of-Words representation)  
- Dictionary mapping word IDs to words

✅ **Output:**  
- An HTML file (`ldavis_prepared_<num_topics>.html`) that can be opened in any browser for interactive exploration.

---

## 🧩 Why It’s Useful

- Visualizes topic **prevalence** and **separation** in 2D.
- Helps check if the number of topics is appropriate.
- Makes interpreting topics easier by showing their defining terms.
- Enables tuning of LDA hyperparameters by comparing bubble overlaps and term relevance.

---

## 📌 How to Use

1. Open the generated HTML file (`ldavis_prepared_<num_topics>.html`).
2. Hover over bubbles to see topic details.
3. Click on a bubble to update the Top Terms panel.
4. Adjust the λ slider for different term relevance views.

---

## ✅ Recommended Tips

- Aim for **distinct bubbles** with minimal overlap.
- Use λ ≈ 0.2–0.5 for balanced term relevance.
- Validate that top words make logical sense for each topic.

---

## 📁 File Location

You’ll find your saved pyLDAvis dashboard at:
