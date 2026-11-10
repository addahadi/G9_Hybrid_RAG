# Large artifacts kept on Google Drive (not in this repo)

Shared folder: https://drive.google.com/drive/folders/14v47jEKJ3rVawyNBtb_BAI6XFGH1MJT7  (`G9_Hybrid_RAG`)

| Drive path | Contents | Why not in git |
|---|---|---|
| `data/splits/` | `split_ids.json`, `image_manifest.csv` | small — copy into `data/splits/` |
| `data/preprocessed_captions/` | `kb_captions_retrieval.csv` etc. | copy into repo if wanted (~MBs) |
| `data/images_archives/` | uncompressed ZIPs of 10,200 images | too large |
| `data/embeddings/clip_vit_base_patch32/` | `kb_image_embeddings.npy` (10,000×512), `kb_text_embeddings.npy` (50,000×512) | large |
| `data/indexes/` | `faiss_images.index` (20 MB), `faiss_captions.index` (102 MB), `bm25.pkl` (4.7 MB) | large |
| `results/eda/` | full EDA outputs incl. original PNG charts (`scene_complexity.png`, `object_cooccurrence_heatmap.png`, `top_20_*.png`, …) and big CSVs | PNGs/large CSVs stay on Drive; core stats are copied into `results/eda/` |
| `results/qa/` | `image_preprocessing_audit.csv`, `test_stratification_diagnostic.csv` | copy if needed |
| `results/retrieval/` | hybrid retrieval demos, `image_query_hybrid_visualization.png` (9 MB) | large |

Tip: use `git lfs` or keep these on Drive/Hugging Face and download with a script.
