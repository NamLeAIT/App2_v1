# Manual Integration Instructions

## 1. Copy text module

Copy:

```text
text_sparse_semantic_dna_streamlit.py
```

into the root of your existing Streamlit project.

## 2. Replace app.py

Use the provided `app.py`, or manually add this import:

```python
from text_sparse_semantic_dna_streamlit import render_text_dna_storage_panel
```

Then wrap your existing image panels in an image tab:

```python
tab_image, tab_text = st.tabs(["🖼️ Image DNA Storage", "📝 Text DNA Storage"])

with tab_image:
    render_panel_1_upload()
    render_panel_2_compression()
    render_panel_3_encoding()
    render_panel_4_experiment()
    render_panel_5_decoding()
    render_panel_6_analysis()

with tab_text:
    render_text_dna_storage_panel()
```

## 3. Limit image DNA mapping to SM/Rinf

In `config.py`, set:

```python
MAPPING_OPTIONS = [
    "Simple Mapping",
    "RINF_B16",
]
```

## 4. Optional UI label cleanup

In `ui_design_system/ui_labels.py`, set:

```python
MAPPING_DISPLAY = {
    "Simple Mapping": "SM",
    "RINF_B16": "R∞",
}

MAPPING_ORDER = [
    "Simple Mapping",
    "RINF_B16",
]
```

## 5. Run

```bash
streamlit run app.py
```
