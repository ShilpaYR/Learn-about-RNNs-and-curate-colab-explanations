#  Learn About RNNs and Curate Colab Explanations

**Course:** Deep Learning — CMPE 258  
**Student:** Shilpa Yelkur Ramakrishnaiah  
**Student ID:** 019151782  
**Assignment Due:** May 10, 2025 by 11:59 PM  
**Points:** 300  

---

##  Overview

This repository contains four Google Colab notebooks covering core deep learning architectures — executed, explained, and archived with full outputs. For each notebook, a YouTube video was recorded explaining every code block and output in detail. A detailed written report is also included in this repository summarizing all four notebooks, key concepts learned, and the full deliverables.

---

##  Colab Notebooks & YouTube Videos

| # | Notebook | YouTube Video |
|---|----------|---------------|
| 1 | [RNN / LSTM / GRU / WaveNet — Zero to Hero](./notebooks/final_rnn_lstm_gru_wavenet_zero_to_hero.ipynb) | [▶ Watch on YouTube](https://youtu.be/LgypN2QRZ8o) |
| 2 | [10 Years of Deep Learning in NLP](./notebooks/final_nlp_deep_learning_10_years_tutorial.ipynb) | [▶ Watch on YouTube](https://youtu.be/U5kaGbb4624) |
| 3 | [Vision Transformers — ViT, CLIP, DINOv2, SAM](./notebooks/final_vision_transformers_tutorial.ipynb) | [▶ Watch on YouTube](https://youtu.be/eia2zWUUgOY) |
| 4 | [GNN Fundamentals — Zero to Hero](./notebooks/final_gnn_fundamentals_tutorial.ipynb) | [▶ Watch on YouTube](https://youtu.be/8lRX_lkbWWU) |

---

##  Assignment Report

A comprehensive written report has been prepared and is included in this repository covering all four notebooks in detail.

**File:** [`Assignment_Report_ShilpaYelkurRamakrishnaiah.pdf`](./Assignment_Report_ShilpaYelkurRamakrishnaiah.pdf)

The report includes:
- Full student and course information
- Deliverables summary table (notebooks + YouTube links)
- Per-notebook breakdown with key topics, code implementations, and architecture details
- Architecture comparison tables for RNNs, NLP timeline, Vision Transformer timeline, and GNN graph applications
- GitHub repository structure
- Key learnings and takeaways from each notebook
- Assignment completion checklist

---

##  Repository Structure

```
Learn-about-RNNs-and-curate-colab-explanations/
├── README.md
├── Assignment_Report_ShilpaYelkurRamakrishnaiah.pdf
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

- **[RNN / LSTM / GRU / WaveNet](https://youtu.be/LgypN2QRZ8o)** — Explains sequence data motivation, Vanilla RNN math and hidden state recurrence, the vanishing gradient problem, LSTM gates (input, forget, output, cell state), GRU update and reset gates, deep stacked RNNs with dropout, gradient clipping, and WaveNet causal dilated convolutions with exponentially growing receptive fields.

- **[10 Years of Deep NLP](https://youtu.be/U5kaGbb4624)** — Walks through tokenization (character, word, subword/BPE), Word2Vec embeddings and the King−Man+Woman analogy, RNN Seq2Seq encoder-decoder, Bahdanau attention, the full Transformer architecture (Q/K/V self-attention, multi-head attention, positional encoding), BERT, GPT, LoRA fine-tuning, and the RLHF alignment pipeline behind ChatGPT and GPT-4.

- **[Vision Transformers](https://youtu.be/eia2zWUUgOY)** — Covers scaled dot-product attention built from scratch in PyTorch, Multi-Head Attention with 8 parallel heads, ViT patch embeddings (16×16 patches, [CLS] token, positional encoding), CLIP contrastive vision-language pretraining for zero-shot classification, DINOv2 self-supervised feature extraction, Segment Anything Model (SAM), and hybrid CNN-Transformer architectures (Swin Transformer, ConvNeXt).

- **[GNN Fundamentals](https://youtu.be/8lRX_lkbWWU)** — Introduces graph data structures (adjacency matrix, edge list, adjacency list), real-world graph applications across 8 domains, the message passing paradigm, GCN derivation from the normalized graph Laplacian, NumPy implementation from scratch, PyTorch GCN using nn.Module, and a node classification demo on a citation network dataset.

---

## Key Concepts Covered

### Notebook 1 — RNN / LSTM / GRU / WaveNet
- Why order matters in sequential data (text, audio, time-series, DNA)
- Character-level language modeling as the benchmark task
- Vanilla RNN: hidden state recurrence, h_t = tanh(W_ih·x_t + W_hh·h_{t-1})
- Vanishing gradient problem — tanh squashes gradients at every step
- LSTM: forget gate (f), input gate (i), output gate (o), cell state (c)
- Cell-state highway: additive update c_t = f⊙c_{t-1} + i⊙c̃_t prevents vanishing gradients
- GRU: update gate (z) and reset gate (r), no separate cell state, ~25% fewer params than LSTM
- Deep stacked RNNs (2 layers) with inter-layer dropout
- Gradient clipping with `clip_grad_norm_` (threshold = 1.0)
- Temperature-controlled text generation (0.2 / 0.8 / 1.5)
- WaveNet: causal padding (left-only) + dilated Conv1d, dilation = 2^i per layer
- Receptive field of 2^7 = 128 characters with just 7 layers
- Full benchmark: loss, time/epoch, parameter count across all 5 model variants

### Notebook 2 — 10 Years of Deep Learning in NLP
- Tokenization: character-level, word-level, subword/BPE — trade-offs explained
- SimpleTokenizer built from scratch with special tokens [PAD], [UNK], [START], [END]
- Word embeddings: dense vectors capturing semantic meaning via cosine similarity
- Word analogy arithmetic: King − Man + Woman ≈ Queen
- PCA projection of word embeddings to 2D for visual clustering
- RNN Seq2Seq encoder-decoder (2014) for machine translation
- Bahdanau attention mechanism (2015) — alignment scores remove encoder bottleneck
- Transformer (2017): self-attention Q/K/V, multi-head attention, positional encoding
- BERT (2018): encoder-only, masked language model, bidirectional context
- GPT: decoder-only, causal language model, autoregressive text generation
- LoRA: low-rank parameter-efficient fine-tuning
- Knowledge distillation: teacher-student model compression
- RLHF: reward model + PPO optimization → InstructGPT → ChatGPT / GPT-4

### Notebook 3 — Vision Transformers
- Scaled dot-product attention: softmax(QK^T / √d_k) · V
- Multi-Head Attention — h parallel heads each learning different relational patterns
- ViT: 224×224 image → 196 non-overlapping 16×16 patches as input tokens
- PatchEmbedding via Conv2d(kernel=16, stride=16) for efficient patch projection
- Learnable [CLS] token and learnable position embeddings
- TransformerEncoderBlock: Pre-Norm, MHA + FFN (GELU) + residual connections
- ViT variants: ViT-B/16 (86M params), ViT-L/16 (307M params)
- CLIP: dual-encoder contrastive pre-training on 400M image-text pairs
- Zero-shot image classification using cosine similarity between embeddings
- DINOv2: self-supervised ViT with emergent segmentation properties
- SAM: promptable segmentation accepting points, boxes, or mask inputs
- Swin Transformer: shifted window local attention + hierarchical feature maps
- ConvNeXt: modernized ResNet adopting Transformer design choices

### Notebook 4 — GNN Fundamentals
- Graph definition: G = (V, E) — nodes, edges, node feature matrix X
- Graph types: undirected, directed, weighted, bipartite
- Adjacency matrix A, edge list, adjacency list — when each representation is best
- 8 real-world graph domains: social networks, molecules, citations, knowledge graphs, etc.
- Why CNNs and MLPs fail on graphs (no fixed grid, permutation variance)
- Message passing paradigm: aggregate neighbor features, update node representations, repeat
- GCN derivation: degree matrix D, normalized adjacency Ã = D^{-½}AD^{-½}, self-loops
- GCN layer: H^{l+1} = σ(Ã · H^l · W^l)
- 2-layer GCN: softmax(Ã · ReLU(Ã · X · W_0) · W_1)
- GCN implemented first in NumPy (full transparency), then in PyTorch (nn.Module)
- Node classification training loop with Adam + CrossEntropyLoss

---

##  Assignment Checklist

- [x] All 4 notebooks copied to Google Drive with world sharing enabled
- [x] All 4 notebooks executed with full outputs visible
- [x] All 4 notebooks archived in this GitHub repository
- [x] 1 YouTube video recorded per notebook (code block by code block)
- [x] README with Colab + YouTube links table
- [x] Written report (PDF) included in the repository
- [x] Repository organized and publicly accessible

---

*Shilpa Yelkur Ramakrishnaiah · 019151782 · Deep Learning — CMPE 258 · Spring 2025*
