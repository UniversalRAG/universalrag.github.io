# Results

We evaluate UniversalRAG on a comprehensive benchmark covering 10 datasets that span multiple modalities and granularities. The full results in Table 1 and the averaged performance across different LVLMs in Figure 3 indicate that, UniversalRAG outperforms strong unimodal and multimodal RAG baselines, validating the effectiveness of our modality- and granularity-aware routing.

<div class="figure-grid">
<figure>
  <img src="assets/fig/result_main.webp" alt="Main Results Table">
</figure>
</div>

**Table 1.** Results of diverse RAG methods with Qwen3-VL-8B-Instruct across modalities. <strong>Bold</strong> denotes the best performance and <u>underlined</u> indicates the second-best among UniversalRAG variants, using either <span style="color: green;">trained</span> or <span style="color: blue;">training-free</span> routers.

<br>

<div class="figure-grid">
<figure>
  <img src="assets/fig/result_main_avg.webp" alt="Main Results Avg Barplot Figure">
</figure>
</div>

**Figure 3.** Comparison of averaged evaluation results across different RAG methods and LVLMs.

<br>

We further conduct ablation studies to validate the effectiveness of UniversalRAG’s granularity-aware routing and cross-modal retrieval, and additionally demonstrate its efficiency in real-world usage scenarios.

<div class="figure-grid">
<figure style="display: flex; flex-direction: column; align-items: center;">
  <img src="assets/fig/result_cross_modal.webp" alt="Cross-modal Performance" style="height: 180px; width: auto; max-width: 100%;">
  <figcaption style="max-width: 100%; text-align: left;"><strong>Table 2.</strong> Performance comparison of uni-modal and cross-modal approaches across different router models.</figcaption>
</figure>
<figure style="display: flex; flex-direction: column; align-items: center;">
  <img src="assets/fig/result_gran.webp" alt="Granularity Performance" style="height: 180px; width: auto; max-width: 100%;">
  <figcaption style="max-width: 100%; text-align: left;"><strong>Table 3.</strong> Performance across different numbers of granularity (#Gn) for training-free router models.</figcaption>
</figure>
<figure style="display: flex; flex-direction: column; align-items: center;">
  <img src="assets/fig/result_latency.webp" alt="Latency Comparison" style="height: 180px; width: auto; max-width: 100%;">
  <figcaption style="max-width: 100%; text-align: left;"><strong>Figure 4.</strong> Retrieval latency per query across corpus sizes.</figcaption>
</figure>
</div>
