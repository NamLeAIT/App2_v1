# Two-Branch Image/Text DNA Storage Project Patch

This package implements the new project structure:

```text
DNA Data Storage System
├── Image DNA Storage
│   ├── keeps your existing image compression pipeline
│   └── exposes only SM and R∞ DNA mapping
│
└── Text DNA Storage
    └── uses Sparse Semantic Token Coding
```

## Files

```text
app.py
text_sparse_semantic_dna_streamlit.py
patch_project_two_branch.py
requirements_text_optional.txt
MANUAL_INTEGRATION.md
```

## Recommended usage

Put this ZIP contents somewhere, then run:

```bash
python patch_project_two_branch.py /path/to/your/project
```

The patch script will:

1. Back up your existing `app.py`, `config.py`, and `ui_design_system/ui_labels.py`.
2. Copy `text_sparse_semantic_dna_streamlit.py` into your project.
3. Replace `app.py` with a two-tab app:
   - Image DNA Storage
   - Text DNA Storage
4. Modify `config.py` so image mapping options are only:

```python
MAPPING_OPTIONS = [
    "Simple Mapping",
    "RINF_B16",
]
```

5. Modify UI labels so the display names are:

```text
Simple Mapping → SM
RINF_B16 → R∞
```

## Run

```bash
streamlit run app.py
```

## Text branch

The text branch uses:

```python
from text_sparse_semantic_dna_streamlit import render_text_dna_storage_panel
```

It implements:

```text
A. Raw UTF-8 Text
B. Whole Text Compression
C. Dense Token Coding
D. Sparse Semantic Text Coding
```

The proposed method is:

```text
Sparse Semantic Text Coding
```

Important: this is designed for compressed + openable + non-exact readable text recovery under substitution errors. It is not exact text reconstruction and it is not ECC.

## Optional XLM-R repair

The text branch has optional XLM-R repair for `[UNK]` / invalid tokens only.

It is OFF by default.

If you turn it on, install:

```bash
pip install torch transformers sentencepiece
```
