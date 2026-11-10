# Open issues (before freezing the preprocessing release)

1. **Test set size and stratification.** The brief says 100 test images (§4.1, 4.2) and 1,000 (§4.4.2, 4.4.3, one line reads "1,00"), and asks for a *stratified* val2017 subset identical for all groups. G9's current test set is 100 **random** images. Ask the teachers in writing. If it changes, regenerate `split_ids.json`, `image_manifest.csv`, the test archive and the audit files; the knowledge base, embeddings and indexes are unaffected (they come from train2017).
2. **Validation experiment.** The brief (§4.4.4) says the 100 validation images select the best preprocessing configuration. This comparison has not been run yet.
3. **Shape analysis** (second attribute in §4.3) and **scatter plots** are not done.
4. **Embedding config**: image batch size (32) is missing from `embedding_config.json`; run the vector-alignment check.
5. **Per-image metadata**: only object categories/counts are stored (human COCO annotations). Attributes, relationships and context are caption-keyword/bbox heuristics, not visual ground truth.
6. **Near-duplicates**: only byte-identical images were checked across splits.
7. **Known limits**: CLIP centre-crop loses image sides; apostrophes split in BM25; CLIP/BLIP may have seen COCO in pretraining.
8. **Test-set category coverage**: 8 categories are absent from the random test set (baseball glove, airplane, baseball bat, bear, toothbrush, scissors, hair drier, toaster); max prevalence gap 3.0 points.
