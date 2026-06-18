# Text Tab Mapping + Compression Metrics Patch

## Added

- DNA Encoding now has:
  - Simple Mapping
  - Rinf

- Text Compression now outputs binary before DNA encoding.

- New compression metrics:
  - input bits
  - output binary bits
  - output bits as % of input
  - bit reduction %

- Binary can be downloaded before DNA encoding.

- `Payload length` is now `Strand length`.

- Repair removed from main UI to avoid missing torch errors.

## Use

Replace:

```text
text_sparse_semantic_dna_streamlit.py
```

with this file.

Run:

```bash
streamlit run app.py
```

## Image layout note

To place `Input preview` and `Selected pixel image` side-by-side in the image tab, edit the image panel code like:

```python
col1, col2 = st.columns(2)

with col1:
    st.image(input_preview, caption="Input preview", use_container_width=True)

with col2:
    st.image(selected_pixel_image, caption="Selected pixel image", use_container_width=True)
```
