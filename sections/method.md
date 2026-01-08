# Why UniversalRAG?

**Can multimodal content be effectively retrieved from a single unified embedding space?** Multimodal encoders are trained to align semantically similar content across text, images, and videos, yet a persistent **modality gap** remains: embeddings tend to cluster by modality rather than meaning, as illustrated in Figure 1. This separation limits cross-modal retrieval as queries are implicitly routed by modality instead of true semantic similarity.

**UniversalRAG addresses this challenge** through **modality-aware routing**. Rather than forcing heterogeneous data into a single shared space, UniversalRAG dynamically identifies the most relevant modality-specific corpus and performs targeted retrieval within it. This design sidesteps the modality gap while remaining flexible to the introduction of new modalities. Beyond modality, UniversalRAG further organizes each corpus by **granularity**—from passages to full documents, or from short clips to full videos—so the retrieval process matches both the semantic intent and the scope of the user’s query. As shown in Figure 2, UniversalRAG yields a balanced distribution of retrieved items across modalities, automatically selecting the most appropriate knowledge source for each query.

<br>
<div class="figure-grid">
<figure style="display: flex; flex-direction: column; align-items: center;">
  <img src="assets/fig/embedding_space.webp" alt="Modality Gap" style="height: 250px; width: auto; max-width: 80%;">
  <figcaption style="max-width: 80%; text-align: left;"><strong>Figure 1.</strong> Modality gap in the unified embedding space.</figcaption>
</figure>
<figure style="display: flex; flex-direction: column; align-items: center;">
  <img src="assets/fig/result_selection_rate.webp" alt="Placeholder figure 2" style="height: 250px; width: auto; max-width: 80%;">
  <figcaption style="max-width: 80%; text-align: left;"><strong>Figure 2.</strong> Distribution of the retrieved data modalities.</figcaption>
</figure>
</div>

