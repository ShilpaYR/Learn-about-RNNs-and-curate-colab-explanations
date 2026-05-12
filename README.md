# Learn About RNNs and Curate Colab Explanations

**Course:** Deep Learning — CMPE 258  
**Student:** Shilpa Yelkur Ramakrishna  
**Student ID:** 019151782  
**Assignment Due:** May 10, 2025 by 11:59 PM  

---

##  Overview

This repository contains four Google Colab notebooks covering core deep learning architectures — executed, explained, and archived with full outputs. For each notebook, a YouTube video was recorded explaining every code block and output in detail.

---

##  Colab Notebooks & YouTube Videos

| # | Notebook | YouTube Video |
|---|----------|---------------|
| 1 | [RNN / LSTM / GRU / WaveNet — Zero to Hero](./notebooks/final_rnn_lstm_gru_wavenet_zero_to_hero.ipynb) | [▶ Watch on YouTube](https://youtu.be/LgypN2QRZ8o) |
| 2 | [10 Years of Deep Learning in NLP](./notebooks/final_nlp_deep_learning_10_years_tutorial.ipynb) | [▶ Watch on YouTube](https://youtu.be/U5kaGbb4624) |
| 3 | [Vision Transformers — ViT, CLIP, DINOv2, SAM](./notebooks/final_vision_transformers_tutorial.ipynb) | [▶ Watch on YouTube](https://youtu.be/eia2zWUUgOY) |
| 4 | [GNN Fundamentals — Zero to Hero](./notebooks/final_gnn_fundamentals_tutorial.ipynb) | [▶ Watch on YouTube](https://youtu.be/8lRX_lkbWWU) |

---

##  Repository Structure

```
Learn-about-RNNs-and-curate-colab-explanations/
├── README.md
└── notebooks/
    ├── final_rnn_lstm_gru_wavenet_zero_to_hero.ipynb
    ├── final_nlp_deep_learning_10_years_tutorial.ipynb
    ├── final_vision_transformers_tutorial.ipynb
    └── final_gnn_fundamentals_tutorial.ipynb
```

All notebooks are executed with full outputs visible and archived in this repository.

---

##  Video Explanations

Each YouTube video covers the corresponding notebook code block by code block:

- **[RNN / LSTM / GRU / WaveNet](https://youtu.be/LgypN2QRZ8o)** — Explains sequence data motivation, Vanilla RNN math, vanishing gradients, LSTM gates, GRU gating, deep/bidirectional stacking, gradient clipping, and WaveNet dilated convolutions.

- **[10 Years of Deep NLP](https://youtu.be/U5kaGbb4624)** — Walks through tokenization, Word2Vec, RNN Seq2Seq, attention, the full Transformer, BERT, GPT, LoRA, and RLHF/ChatGPT.

- **[Vision Transformers](https://youtu.be/eia2zWUUgOY)** — Covers scaled dot-product attention, Multi-Head Attention built from scratch, ViT patch embeddings, CLIP contrastive learning, DINOv2 self-supervised features, SAM, and hybrid architectures.

- **[GNN Fundamentals](https://youtu.be/8lRX_lkbWWU)** — Introduces graphs, adjacency matrices, the message passing paradigm, GCN math, NumPy implementation from scratch, PyTorch GCN, and node classification demo.

---

##  Key Concepts Covered

### Notebook 1 — RNN / LSTM / GRU / WaveNet
- Why order matters in sequential data
- Vanilla RNN: hidden state recurrence
- Vanishing gradient problem
- LSTM: input, forget, output, cell gates
- GRU: reset and update gates
- Deep stacked & bidirectional RNNs
- Gradient clipping (`clip_grad_norm_`)
- WaveNet: causal and dilated convolutions
- Character-level language model & text generation

### Notebook 2 — 10 Years of Deep Learning in NLP
- Tokenization: character / word / subword (BPE)
- Word embeddings (Word2Vec)
- Sequence-to-sequence encoder-decoder
- Bahdanau attention mechanism
- Transformer architecture (self-attention + FFN)
- BERT (encoder-only, masked language model)
- GPT (decoder-only, causal language model)
- LoRA and knowledge distillation
- RLHF, InstructGPT, ChatGPT / GPT-4

### Notebook 3 — Vision Transformers
- Scaled dot-product attention: Q, K, V
- Multi-Head Attention (8 heads in PyTorch)
- Patch embedding — 16×16 image patches
- [CLS] token and positional encoding
- ViT full encoder architecture
- CLIP: contrastive vision-language pretraining
- Zero-shot image classification
- DINOv2 self-supervised feature extraction
- Segment Anything Model (SAM)
- Swin Transformer and ConvNeXt hybrids

### Notebook 4 — GNN Fundamentals
- Graph definition: G = (V, E)
- Adjacency matrix, edge list, adjacency list
- Real-world graph applications
- Why GNNs over traditional ML
- Message passing paradigm
- GCN derivation: Ã H W
- GCN from scratch in NumPy
- GCN in PyTorch (nn.Module)
- Node classification on citation dataset

---

##  Assignment Checklist

- [x] All 4 notebooks copied to Google Drive with world sharing enabled
- [x] All 4 notebooks executed with full outputs
- [x] All 4 notebooks archived in this GitHub repository
- [x] 1 YouTube video recorded per notebook (code block by code block)
- [x] README with Colab + YouTube links table
- [x] Repository organized and publicly accessible

---

*Shilpa Yelkur Ramakrishna · 019151782 · Deep Learning CMPE 258 · Spring 2025*
