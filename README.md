<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>GreenVulBERT: Green Computing for Automated CVSS Scoring</title>
</head>
<body>

<h1>GreenBERT: Green Computing for Automated CVSS Scoring</h1>

<p>This repository contains the code implementation of <strong>GreenBERT</strong>, a lightweight and energy-efficient Transformer-based framework for automated software vulnerability scoring, as presented in our paper:</p>

<p><strong>"Green Transformer for Automated Prediction of Software Vulnerability Scores"</strong><br>
Mirtaheri et al., <em>Array Journal, 2025</em></p>

<h2>🔍 Overview</h2>
<ul>
  <li>Uses knowledge distillation to train compact student models for each CVSS base metric (AV, AC, PR, UI, S, C, I, A)</li>
  <li><strong>6%+ F1-score improvement</strong> over BERT</li>
  <li><strong>~80% faster inference</strong></li>
  <li><strong>~70% lower energy and CO₂ emissions</strong></li>
</ul>

<h2>📁 Project Structure</h2>
<ul>
  <li><code>code.py</code>: Main training and evaluation script</li>
  <li><code>data/combined.csv</code>: Vulnerability data with CVSS labels</li>
  <li><code>distilled_student_{metric}/</code>: Output directories for student models</li>
  <li><code>training_metrics_{metric}.csv</code>: Saved evaluation results</li>
</ul>

<h2>⚙️ Requirements</h2>
<pre><code>pip install torch transformers pandas scikit-learn tqdm
</code></pre>
<p><strong>Also required:</strong></p>
<ul>
  <li>CUDA-enabled GPU (e.g., NVIDIA RTX 2080 Ti)</li>
  <li>Teacher models (e.g., BERT), stored in: <code>./bert_cvss/bert_cnn/combined50/SBert/models/{metric}</code></li>
</ul>

<h2>🚀 How to Run</h2>
<pre><code>python code.py
</code></pre>
<p>This will:</p>
<ol>
  <li>Load and preprocess vulnerability data</li>
  <li>Train a student model for each CVSS metric</li>
  <li>Evaluate accuracy, F1, energy use, and CO₂ impact</li>
  <li>Save outputs in <code>distilled_student_{metric}/</code></li>
</ol>

<h2>📊 Output</h2>
<ul>
  <li>Trained models for AV, AC, PR, UI, S, C, I, A</li>
  <li>Evaluation metrics (accuracy, F1-score, energy use, CO₂ emissions)</li>
  <li>CSV logs with detailed epoch performance</li>
</ul>

<h2>📜 Citation</h2>
<p>If you use this code, please cite the following:</p>
<pre><code>@article{mirtaheri2025greenbert,
  title={Green Transformer for Automated Prediction of Software Vulnerability Scores},
  author={Mirtaheri, Seyedeh Leili and Kafi, Ali and Heydari, Hamid and Pugliese, Andrea},
  journal={Array},
  year={2025}
}
</code></pre>

<h2>📧 Contact</h2>
<p><strong>Leili Mirtaheri</strong><br>
Email: <a href="mailto:leili.mirtaheri@dimes.unical.it">leili.mirtaheri@dimes.unical.it</a></p>

</body>
</html>
