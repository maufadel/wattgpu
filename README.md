# WattGPU

WattGPU is a framework for predicting the energy and latency characteristics of Large Language Model (LLM) inference on GPUs **without requiring profiling or hardware access**.

The repository contains the code, data processing pipeline, and models presented in the paper:

> **WattGPU: Predicting LLM Inference Power and Latency on Unseen GPUs Without Profiling**

WattGPU predicts:

- **Mean GPU power draw** during inference
- **Inter-Token Latency (ITL)**

using only:

- Public GPU specifications
- Public LLM metadata

The models generalize to **unseen GPUs and unseen LLMs**, enabling energy-aware deployment decisions before running experiments.

---

## Repository Contents

- `WattGPU.ipynb` — Main notebook containing:
  - Data preprocessing
  - Feature engineering
  - Model training
  - Evaluation
  - Reproduction of the paper results

- `requirements.txt` — Python dependencies

- Data used in the experiments, including the subset of [Watt Counts](https://arxiv.org/html/2604.09048v1) used for training and evaluation.

---

## Installation

### 1. Clone the repository

```bash
git clone <repository-url>
cd wattgpu
```

### 2. Create a Python environment with uv

We recommend Python 3.12.

```bash
uv venv --python 3.12
```

### 3. Activate the environment

#### Linux / macOS

```bash
source .venv/bin/activate
```

#### Windows

```powershell
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
uv pip install -r requirements.txt
```

---

## Running the Project

Start Jupyter Lab:

```bash
jupyter lab
```

Then open:

```text
WattGPU.ipynb
```

The notebook contains the complete pipeline used in the paper.

---

## License

Apache 2.0.