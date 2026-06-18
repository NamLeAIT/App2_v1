# DNA Storage Image/Text UI Patch v21

Changes:

1. Text validation preview now highlights decoded/repaired content:
   - unresolved/failed tokens are shown as `[MASK]`
   - repaired tokens are shown in bold/green highlight
   - changed decoded tokens are highlighted in amber
   - this makes error and repair positions visible for presentations/professor review

2. Removed the visible checkbox controls:
   - no more `Show only failed/repaired tokens` checkbox
   - no more `Show only word errors` checkbox
   The UI now shows compact error-focused tables by default.

3. Kept Token recovery preview hidden in an expander, showing only non-decoded/problem tokens by default.

4. Image reconstruction channel handling remains enforced through `robust_image_pipeline.py`:
   - grayscale outputs are coerced to `L`
   - RGB outputs are coerced to `RGB`
   - black-white outputs are coerced to binary-like grayscale `L`

Files to overwrite:
- text_dna_unified_panel.py
- robust_image_pipeline.py
- app.py
- panels.py
- dna_sparse_semantic_project.py

Run:
```bash
streamlit run app.py
```
