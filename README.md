# Sequence-Prediction-using-CRF
# Sequence Prediction using Conditional Random Fields (CRF)

This repository contains a minimal implementation and experiment script for **sequence labeling / structured prediction** using a **Conditional Random Field (CRF)** model.

The code was developed as part of my PhD work on modeling **event-driven data** where labels are **dependent across time/positions** (e.g., segmenting or tagging a sequence rather than predicting each element independently).

## What’s in this repo

- `CRF.ipynb` — single-file implementation / experiment script (training + inference + evaluation)

> This repo is intentionally lightweight: one file that runs end-to-end.

## Problem setting

Given an input sequence `x = (x1, x2, ..., xT)`, predict a structured output sequence `y = (y1, y2, ..., yT)` where adjacent labels are not independent.

CRFs model:
- **emission/feature contributions**: how each `xt` supports label `yt`
- **transition structure**: how `yt-1 → yt` is rewarded/penalized

This is useful when label consistency matters (e.g., state sequences, event phases, BIO tagging).

## Requirements

- Python 3.8+
- Dependencies listed in `CRF.<ext>` imports  
  (If you want, add a `requirements.txt` later once imports are stable.)

## How to run

1) Clone the repository:
```bash
git clone https://github.com/<your-username>/Sequence-Prediction-using-CRF.git
cd Sequence-Prediction-using-CRF
