# Bias in Large Language Models (LLMs)

This documentation explores the sources and implications of bias in large language models, focusing on how biases are introduced and propagated through training data, algorithms, and output formulation.

## Introduction

Large language models (LLMs) are powerful tools for natural language processing, but they can inadvertently perpetuate biases present in their training data or introduced through algorithmic design. Understanding and mitigating these biases is critical for developing fair and equitable AI systems.

## Sources of Bias in LLMs

Bias in LLMs can arise from multiple stages of the model development pipeline:

1. **Bias in Training Data**: The quality and composition of training datasets can introduce biases, as models learn patterns and representations from these corpora. If the data is skewed or unrepresentative, the model may produce biased outputs.
2. **Bias in Algorithmic Processing**: The way algorithms process and prioritize data during training can amplify certain patterns or perspectives, leading to biased learned representations.
3. **Bias in Output Formulation**: The design of how models generate responses, including prompt handling and output constraints, can influence the tone, perspective, or fairness of the results.

## Training Data for Popular LLMs

The table below lists several prominent LLMs and the datasets used for their training. These corpora significantly influence the models' learned representations and potential biases.

| Large Language Model | Data Corpus Used |
|----------------------|------------------|
| T5                  | C4 (Colossal Clean Crawled Corpus) |
| BLOOM               | ROOTS (46 natural languages, 13 programming languages) |
| GPT-3               | Common Crawl, WebText, Books, Wikipedia |
| Bard                | Infiniset (proprietary dataset) |
| Stable Diffusion    | LAION-5B |
| BERT                | BookCorpus, English Wikipedia |
| LLaMA 2             | Common Crawl, C4, GitHub, Wikipedia, Books |
| Grok 3              | Web crawls, curated datasets (specifics undisclosed) |
| RoBERTa             | BookCorpus, English Wikipedia, CC-News, OpenWebText, Stories |

**Note**: The datasets listed are based on publicly available information and may not be exhaustive, as some models (e.g., Grok 3, Bard) use proprietary or partially undisclosed corpora. Biases in these datasets, such as under-representation of certain demographics or overemphasis on specific cultural contexts, can lead to skewed model outputs.

