<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=17213A&height=180&section=header&text=BBC%20News%20Classifier&fontSize=42&fontColor=EDE7D8&animation=fadeIn&fontAlignY=38&desc=Transformer%20vs.%20Embeddings%20vs.%20Pipeline&descAlignY=58&descSize=18" alt="header banner" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&size=18&duration=2800&pause=900&color=17213A&center=true&vCenter=true&width=560&lines=Sorting+news+into+business%2C+tech%2C+politics%2C+sport%2C+entertainment...;Word2Vec+%2B+Transformer+built+from+scratch;MiniLM+embeddings+%2B+classic+ML;Fine-tuned+DistilBERT+in+a+transformers+pipeline" alt="typing banner" />
</p>

<p align="center">
  <a href="https://noga-66.github.io/bbc-news-classifier/">
    <img src="https://img.shields.io/badge/Live%20Demo-view%20app-c8891f?style=for-the-badge" alt="Live demo" />
  </a>
</p>

# BBC News Classifier — Transformer vs. Sentence Embeddings vs. Pipeline

A multi-class text classification project that compares three different NLP approaches on the same dataset: a Transformer encoder built from scratch, pretrained sentence embeddings with a traditional ML model, and a HuggingFace `transformers` pipeline.

## Dataset

[BBC News Articles](https://www.kaggle.com/datasets/bhavikjikadara/bbc-news-articles) (Kaggle, by Bhavik Jikadara) — news articles labeled into 5 categories: `business`, `entertainment`, `politics`, `sport`, `tech`.

## What's in this repo

| File | Description |
|---|---|
| `bbc_news_classification_project_en.ipynb` | Main Colab notebook: data loading, all 3 modeling approaches, and a final comparison table |
| `classifier-wire.html` | A standalone interactive demo UI (open directly in a browser, no server needed) |
| `README.md` | This file |

## Approaches compared

1. **Transformer from scratch** — Word2Vec static embeddings, sinusoidal positional encoding, a multi-head self-attention encoder block, and a classification head, trained end-to-end on the dataset.
2. **Sentence embeddings + ML** — document embeddings from `all-MiniLM-L6-v2` (Sentence-Transformers), fed into Logistic Regression / SVM / Random Forest.
3. **Transformers pipeline** — a zero-shot classification pipeline for a no-training baseline, plus a fine-tuned `distilbert-base-uncased` model wrapped in a `transformers` pipeline.

Each approach is evaluated on the same held-out test split so the final comparison table is apples-to-apples.

## Running the notebook

1. Open `bbc_news_classification_project_en.ipynb` in [Google Colab](https://colab.research.google.com/) (File → Upload notebook, or open directly from GitHub via Colab's "GitHub" tab once this repo is pushed).
2. Turn on a GPU runtime: Runtime → Change runtime type → T4 GPU.
3. Run the cells top to bottom. The dataset download cell needs a `kaggle.json` API token (from kaggle.com → Settings → API → Create New Token).

## Viewing the demo app

**Live:** [noga-66.github.io/bbc-news-classifier](https://noga-66.github.io/bbc-news-classifier/)

`classifier-wire.html` is fully self-contained (HTML/CSS/JS, no build step), so it's already deployed for free via GitHub Pages. To redeploy after edits, just push a new commit to `main` — Pages rebuilds automatically within about a minute.

Note: the demo's live classification is a lightweight in-browser keyword scorer for illustration — it's not the trained model from the notebook. It can be wired up to real model predictions via an API call if you add a backend.

## Results

_Fill in after running the notebook:_

| Approach | Test Accuracy |
|---|---|
| Transformer from scratch (Word2Vec + Positional Encoding) | |
| MiniLM embeddings + best ML model | |
| Zero-shot pipeline (no training) | |
| Fine-tuned DistilBERT pipeline | |

## License

Project code: MIT. Dataset license follows the terms on its [Kaggle page](https://www.kaggle.com/datasets/bhavikjikadara/bbc-news-articles).

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=17213A&height=100&section=footer" alt="footer banner" />
</p>
