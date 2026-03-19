# Spectrum-to-Signal for Tiny Language Models

This repository contains a research project on the effectiveness of the **spectrum-to-signal** method for small language models.

## Repository Structure

- `train/` - training notebooks (main code)
  - `only_sft.ipynb` - SFT-only training
  - `only_medium.ipynb` - SFT + GRPO training
  - `only_train.ipynb` - full training pipeline (SFT + experts + fusion + MGPO)
- `data/` - CSV datasets used by notebooks
- `text/` - report
- `requirements.txt` - Python dependencies

## Installation and Run (Linux)

1. Clone the repository and move to the project directory:

```bash
git clone git@github.com:VadosikRRR/SSP_TINY_MODELS.git
cd SSP_TINY_MODELS
```

2. Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Open and run the required notebook from `train/`:

```bash
jupyter notebook train/only_sft.ipynb
```

You can also run:

- `train/only_medium.ipynb` for SFT + GRPO
- `train/only_train.ipynb` for the full pipeline

## Notes

- Default dataset paths in notebooks point to files in `data/`.
- If you use external pretrained weights, update `rl_init_model_path` in notebook run configs.
