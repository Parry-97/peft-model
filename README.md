# **PEFT**-model

This project demonstrates how to perform parameter-efficient fine-tuning (PEFT) of transformer models from Hugging Face using the `peft` library.

## Requirements

- Python >= 3.13
- torch >= 2.7.1
- transformers >= 4.52.4
- peft >= 0.16.0

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/your_username/peft-model.git
cd peft-model
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install .
```

Or using Poetry:

```bash
pip install poetry
poetry install
```

## Usage

Edit `fine_tuning.py` to adjust the model checkpoint (default: `bigscience/mt0-large`), LoRA configuration (`r`, `lora_alpha`, `lora_dropout`), and task type (e.g., `SEQ_2_SEQ_LM`).

Run the script:

```bash
python fine_tuning.py
```

This script will load the model, apply the **PEFT** adapter, and print the number of trainable parameters.

## Extending

- Add a training loop using Hugging Face `Trainer` or custom training code.
- Integrate datasets for fine-tuning (e.g., using the `datasets` library).
- Experiment with different adapters (prefix tuning, prompt tuning, etc.).

## License

This project is provided under the [MIT License](LICENSE).
