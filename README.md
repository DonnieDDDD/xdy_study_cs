# Deep Learning Study Notebooks

Personal notebooks for learning core deep learning models, from MLPs to diffusion and generative models, plus a nanoGPT study.

## Naming convention

Notebooks follow the pattern:

```
<Model>_<Dataset>_learning[_].ipynb
```

- `<Model>` — the architecture being studied (e.g. `MLP`, `CNN`, `VAE`, `VQVAE`, `DDPM`, `FlowMatching`, `nanoGPT`)
- `<Dataset>` — the dataset it's trained on (e.g. `MNIST`, `FashionMNIST`, `CIFAR10`, `shakespeare`)
- A trailing underscore before `.ipynb` means the notebook **requires a GPU** — it will not run in reasonable time (or at all) on CPU. No trailing underscore means it's fine to run on CPU.

Examples:
- `VAE_MNIST_learning.ipynb` — VAE on MNIST, CPU-friendly
- `DDPM_CIFAR10_learning_.ipynb` — DDPM on CIFAR-10, needs a GPU
- `nanoGPT_shakespeare_learning_.ipynb` — nanoGPT on Shakespeare text, needs a GPU

## Setup

```bash
pip install -r requirements.txt
```

## Structure

- `*.ipynb` — study notebooks
- `data/` — downloaded datasets (not versioned)
- `models/` — saved model checkpoints (not versioned)
- `nanoGPT/` — cloned nanoGPT repo for the GPT study notebook
- `dockerfiles/` — Docker setup for GPU training
