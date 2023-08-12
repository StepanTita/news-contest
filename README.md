# 📰 Ukrainian News Classification Experiments 

Welcome to the repository containing Jupyter notebooks and findings from our research paper on Ukrainian news classification. Dive in to discover our methodologies, key findings, and comparisons of various pretrained models for the Ukrainian language.
This is the set of experiments conducted by [Stepan Tytarenko](https://github.com/StepanTita), whose solution used XLM-R and has won the in-class competition. 

---

## 🎯 Abstract

In the vast expanse of natural language processing, languages like Ukrainian face a pressing issue: the lack of datasets. This paper unveils a pioneering approach to dataset creation with minimal overhead, setting the stage for Ukrainian news classification.

---

## 📌 Key Findings

- **ukr-RoBERTa, ukr-ELECTRA, and XLM-R** are the crème de la crème of models.
- **XLM-R** is the go-to for longer texts.
- **ukr-RoBERTa** is a beacon for shorter sequences.
- **NB-SVM baseline**? A dark horse with commendable performance on a large dataset!

---

## 🔬 Experiments

Our experiments spread across:
1. Small training set with titles only 📃
2. Small training set, full text immersion 📜
3. Large training set, titles at the forefront 📃📃
4. Large training set, full text deluge 📜📜

Models were put to the test, each having a time window of 24 hours on a single P100 GPU.

### 📊 Benchmark Results

| Model | Short texts / small training set | Long texts / small training set | Short texts / large training set | Long texts / large training set |
|-------|----------------------------------|--------------------------------|----------------------------------|--------------------------------|
| NB-SVM baseline | 0.533 | 0.900 | 0.708 | 0.910 |
| mBERT | 0.790 | 0.910 | 0.675 | 0.907 |
| Slavic BERT | 0.636 | 0.907 | 0.620 | 0.940 |
| ukr-RoBERTa | 0.853 | 0.948 | 0.903 | 0.950 |
| ukr-ELECTRA | 0.685 | 0.950 | 0.745 | 0.948 |
| XLM-R | 0.840 | 0.915 | 0.909 | 0.915 |

🏆 **Note**: XLM-R takes the gold with an F1 score of 0.95 on the large full-text training set.

---

## 🧐 Observations

- **mBERT** & **Slavic BERT**: Not the stars of the show when it comes to F1-scores.
- **ukr-RoBERTa**: Climbs the ranks, especially on short-text terrain.
- **ukr-ELECTRA**: Balances the act between different text lengths.
- **XLM-R**: Reigns supreme with long texts, but faces hurdles with short ones.

---

## 📁 Dataset

Want the dataset? Fetch it on [Kaggle](https://www.kaggle.com/c/ukrainian-news-classification/).

---

## 📝 Citation

If our work aids your research, show some love with a citation:

```mathematica
D. Panchenko et al. (2021). Ukrainian News Corpus As Text Classification Benchmark.
```
