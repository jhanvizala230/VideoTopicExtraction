# 🎥 Video Topic Extraction and Visualization

## 📌 Project Description

This project demonstrates an end-to-end pipeline for analyzing video content. It covers:
- Transcribing spoken content from video files.
- Normalizing and cleaning the text data.
- Extracting key phrases and relevant topics.
- Visualizing the extracted topics with an interactive dashboard.

This workflow is useful for automatic topic discovery, content summarization, and data-driven insights from recorded videos.

---

## ⚙️ Tech Stack

| Component | Technology |
|-----------|-------------|
| Programming Language | Python |
| Speech Recognition | Google Speech-to-Text via `SpeechRecognition` |
| Text Processing | NLTK, Regex, WordNet Lemmatizer |
| Keyphrase Extraction | KeyBERT |
| Topic Modeling | Gensim LDA |
| Visualization | pyLDAvis |
| Video Handling | MoviePy |
| Data Management | File system & Python standard libraries |

---

## 📚 Libraries Used

Below are the main Python libraries leveraged in this project:

- `SpeechRecognition` — Converts audio to text using Google’s Speech-to-Text API.
- `moviepy` — Extracts audio tracks from video files.
- `nltk` — Tokenizes, removes stopwords, and lemmatizes text for cleaner analysis.
- `keybert` — Extracts meaningful key phrases using BERT embeddings.
- `gensim` — Performs topic modeling with Latent Dirichlet Allocation (LDA).
- `pyLDAvis` — Creates an interactive web-based topic visualization.
- `pytube` — (Optional) For downloading YouTube videos.
- `pymysql` — (Optional) For database integration if needed.

---

## 🧮 Algorithms Used & Description

### 1️⃣ Speech-to-Text Transcription  
**Tool:** `SpeechRecognition` + Google Speech API  
**Description:** Extracts audio from videos and splits it into 1-minute segments. Each segment is sent to the Google API to produce a transcript.

---

### 2️⃣ Text Normalization  
**Tools:** `nltk`  
**Description:**  
- Lowercasing  
- Removing punctuation  
- Removing stopwords  
- Tokenization  
- Lemmatization (reduces words to their base form)

This cleans the raw transcript and makes it suitable for NLP tasks.

---

### 3️⃣ Keyphrase Extraction  
**Tool:** `KeyBERT`  
**Description:** Uses BERT embeddings to find phrases and words that capture the main ideas in the text. Works by ranking n-grams by semantic similarity to the document.

---

### 4️⃣ Topic Modeling  
**Tool:** `Gensim LDA`  
**Description:**  
- Transforms text into bag-of-words representation.
- Builds bigrams to capture common phrases.
- Trains a Latent Dirichlet Allocation (LDA) model to discover hidden topics in the text corpus.

---

### 5️⃣ Interactive Visualization  
**Tool:** `pyLDAvis`  
**Description:** Generates an HTML dashboard that lets you explore:
- Topic distribution


### The interactive pyLDAvis dashboard shows an intertopic distance map and the key words defining each topic. Well-separated bubbles indicate distinct topics, and the term bars help interpret the top keywords for each topic. The lambda slider fine-tunes how generic vs unique words are shown

---

## 📷 Demo Gallery

Below are sample visual outputs from the Video Topic Extraction pipeline:

| Key Phrases Bar Chart | pyLDAvis Dashboard |
|-----------------------|---------------------|
| ![Key Phrases](./keyphrases.png) | [🔗 View Interactive Dashboard](.video_topics.html) |

---

### 📑 Topic-wise Word Clouds

Each word cloud shows the most representative words for each discovered topic.

| Topic 0 | Topic 1 |
|---------|----------|
| ![Topic 0 Word Cloud](./wordcloud_topic_0.png) | ![Topic 1 Word Cloud](./wordcloud_topic_1.png) |

| Topic 2 | Topic 3 |
|---------|----------|
| ![Topic 2 Word Cloud](./wordcloud_topic_2.png) | ![Topic 3 Word Cloud](./wordcloud_topic_3.png) |

| Topic 4 |
|---------|
| ![Topic 4 Word Cloud](./wordcloud_topic_4.png) |

---