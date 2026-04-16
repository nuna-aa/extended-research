# Extended Research

A collection of research notebooks exploring multilingual properties of large language models, with a focus on low-resource and non-Latin languages.

## Notebooks

### [Multilingual Induction Heads](mechanistic_interpretability/multilingual_induction_heads.ipynb)
**Area:** Mechanistic Interpretability

Investigates whether induction heads — attention heads responsible for in-context pattern copying — behave the same way across languages. Compares English and Yoruba using a combination of induction scoring, attention visualization, and ablation studies.

Key questions:
- Do the same attention heads drive induction across languages?
- Do "English induction heads" also matter for Yoruba, and vice versa?

Techniques used: induction scoring, attention pattern visualization, head ablation, cross-language comparison.

---

### [Multilingual Tokenization Parity](tokenization/multillingual_tokenization_parity.ipynb)
**Area:** Tokenization Fairness

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nuna-aa/paper-reproduction/blob/main/tokenization/fairness/multillingual-tokenization-parity.ipynb)

Measures the *tokenization premium* — how many more tokens a model uses to encode a given text in a non-English language compared to English — across the FLORES-200 benchmark (219 languages).

Models evaluated: NLLB-200, Gemma 3, Qwen3, Tiny-Aya.

Key findings:
- Training coverage, not vocabulary size, is the primary driver of tokenization fairness.
- Latin-script languages consistently receive the lowest premiums; Tibetan and Southeast Asian scripts the highest.
- Large vocabularies (e.g. Gemma 3 at ~256k tokens) do not guarantee equitable tokenization across scripts.

Reproduces findings from: *Language Model Tokenizers Introduce Unfairness Between Languages*.

## Setup

Each notebook includes its own install cell. Dependencies vary by notebook but generally require:

```bash
pip install transformers datasets torch huggingface_hub
```

See the top of each notebook for the full install command.
