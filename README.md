# autocomplete-ml

This repository contains a character-level Transformer notebook (mini-GPT) for Java autocomplete experiments.

## Recommended environment setup

Pick one of the two approaches below.

### 1) Using a Python venv (pip)

```bash
# create and activate venv
python3 -m venv .venv
source .venv/bin/activate

# install dependencies
pip install -r requirements.txt
```

Note: PyTorch may require a specific wheel for CUDA or MPS. If the `pip install -r requirements.txt` command does not install a GPU-enabled build, follow the official PyTorch instructions for your platform: https://pytorch.org/get-started/locally/

### 2) Using conda

```bash
conda env create -f environment.yml
conda activate autocomplete-ml
```

For CUDA machines you might instead want to install PyTorch via conda with the correct `pytorch-cuda` package (see PyTorch docs). The provided `environment.yml` uses pip to install the same `requirements.txt` for simplicity.

## Quick checks

- Open and run `01_char_level_transformer.ipynb`.
- The notebook already contains a device-selection snippet that prints which device PyTorch is using (MPS/CUDA/CPU).

## Notes

- `requirements.txt` contains minimal packages used in the notebook (PyTorch, numpy, jupyter). Add more packages if you extend the notebook.
- To pin exact versions for reproducibility, replace the `>=` pins with exact versions (e.g. `torch==2.1.0`).
