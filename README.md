# bias-propagation-summarization
This project studies how pre-training bias in language models affects text summarization. Using synthetic nationality-based data, we test BART and PEGASUS for hallucinated nationality changes. Results show zero bias in this setting, highlighting the role of real-world data in bias propagation.
A Case Study in Text Summarization Using BART & PEGASUS

This repository explores how pre-training biases in Large Language Models (LLMs) may propagate to downstream text summarization tasks. Specifically, we analyze whether models hallucinate nationality information when exposed to perturbed name inputs.

This work is based on the research paper:

When Do Pre-Training Biases Propagate to Downstream Tasks? A Case Study in Text Summarization (EACL 2023)

-Objective

To study if LLMs like BART and PEGASUS introduce biased or hallucinated nationality information in generated summaries when names are changed.-
🧠 Methodology
Step	Description
Dataset	Synthetic balanced data with multiple nationalities
Models	BART (abstractive) & PEGASUS (extractive)
Experiment	Replace original names with new nationality-based names
Evaluation	Measure if nationality in summary changes / hallucination occurs
Visualization	Heatmaps of hallucination rate

- Results

Both BART and PEGASUS produced zero hallucination in our synthetic-data setting.

The heatmap outputs were all zeros, indicating no nationality bias expression.

This shows synthetic balanced data suppresses bias, highlighting importance of real-world datasets in bias evaluation.

-Future Improvements

Use real-world balanced datasets

Add bias penalty loss during fine-tuning

Apply Adapter / LoRA fine-tuning

Integrate post-generation fact-checking (FEQA/FRANK)

Extend to gender & profession bias

- Tech Stack

Python

Hugging Face Transformers

PyTorch

NumPy / Pandas / Matplotlib / Seaborn
