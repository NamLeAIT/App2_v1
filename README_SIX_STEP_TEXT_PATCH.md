# Six-Step Text Tab Patch

This patch replaces the old text tab UI with a 6-step pipeline matching the image app:

```text
1. Input
2. Text Compression
3. DNA Encoding
4. Strand Design
5. Text Reconstruction
6. Validation
```

It also fixes:

```text
_csv.Error: need to escape, but no escapechar set
```

by exporting CSV files with:

```python
quoting=csv.QUOTE_ALL
escapechar="\\"
doublequote=True
```

## How to use

Copy this patched file into your Streamlit project folder:

```text
text_sparse_semantic_dna_streamlit.py
```

Then run your app again.

## Test text tab only

You can also copy `app_text_only.py` into the same folder and run:

```bash
streamlit run app_text_only.py
```

## Note

Step 5 is called "Text Reconstruction", not "Image Reconstruction", because this is the text branch.
