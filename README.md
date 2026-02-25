A Comparative Study of Transformer Models for Sentiment Analysis in Low-Resource Tamil Language
This repository contains a comparative research framework for sentiment classification in code-mixed Tamil-English (Tanglish) text. The project evaluates state-of-the-art multilingual Transformers, focusing on linguistic efficiency and statistical rigor.
📊 Dataset Overview
The project utilizes a large-scale corpus of 35,000+ instances of Dravidian code-mixed text (Tamil-English).

Nature of Data: Social media comments (YouTube/Twitter) exhibiting intra-sentential code-switching.

Classes: Multi-class sentiment (Positive, Negative, Mixed Feelings, Neutral, and Unknown State).

Complexity: The dataset presents significant challenges due to the agglutinative nature of Tamil, where multiple morphemes are combined into single words, often represented in Roman script.
🚀 Project UniquenessUnlike standard classification projects, this research implements three advanced evaluative pillars required for top-tier AI internships:
Linguistic Probing (Fertility Analysis): We calculate the Tokenizer Fertility Rate to analyze how WordPiece (mBERT) vs. SentencePiece (XLM-R) handles Tamil morphology. This explains why a model performs better based on its ability to preserve root word semantics.
Statistical Rigor: We implement McNemar’s Test, moving beyond raw accuracy to prove that the performance delta between models is statistically significant ($p < 0.05$).
Cross-Lingual Benchmarking: A direct comparison between mBERT and XLM-RoBERTa to identify which architecture better captures the syntax of Romanized Dravidian languages.
🛠️ Technical Implementation
Core Stack
Models: bert-base-multilingual-cased, xlm-roberta-base

Frameworks: PyTorch, Hugging Face Transformers, Scikit-Learn

Statistical Tools: Statsmodels (McNemar’s Test)

Pipeline Flow
Preprocessing: Cleaned noise from code-mixed strings and handled class imbalance using Macro-F1 optimization.
📜 How to Use
Clone the repo: git clone https://github.com/yourusername/tamil-sentiment-transformers.git

Install dependencies: pip install transformers torch statsmodels

Run the analysis: python main.py

Fine-Tuning: Implemented a custom Trainer loop with epoch-level evaluation on a T4 GPU.

Benchmarking: Comparative analysis of accuracy, F1-score, and sub-word fragmentation.
