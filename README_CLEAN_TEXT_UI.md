# Clean Text Tab UI Patch

This version removes long descriptive UI text and keeps a simpler professor-facing workflow.

## Changes

- Removed long captions/descriptions.
- Upload automatically extracts text and shows preview.
- Step 2 method names:
  - Raw Text
  - Compressed Text
  - Token Text
  - Error-Aware Token Text
- Advanced settings are hidden.
- Step 2 shows Result table and allows:
  - Download result CSV
  - Download result JSON
- Step 5 shows:
  - Original text
  - Decoded text after DNA errors

## Fixes preserved

- Safe CSV export.
- Unique download button keys.

## How to use

Replace:

```text
text_sparse_semantic_dna_streamlit.py
```

with this patched file.

Run:

```bash
streamlit run app.py
```

## Test text only

```bash
streamlit run app_text_only.py
```
