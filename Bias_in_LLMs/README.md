# Bias in Large Language Models (LLMs)

This document explains where bias comes from in large language models (LLMs) and how it affects what these models learn and say. It also looks at the impact of biased data and algorithms.

<br>

## Introduction

Large language models (LLMs) are powerful tools used for understanding and generating language. But they can also carry and repeat bias that comes from the data they were trained on or how they were built. It’s important to know how these biases happen so we can try to reduce them and make AI more fair for everyone.

<br>

## Sources of Bias in LLMs

Bias in LLMs can come from different parts of the model-building process:

1. **Training Data Bias**  
   Models learn from the data they are given. If that data is unbalanced, outdated, or comes from only a few sources, the model will learn and repeat those biases.

2. **Algorithm Bias**  
   How the model processes data during training can add more bias. Some patterns may be given more importance than others, even if they aren’t fair or balanced.

3. **Bias in Model Output**  
   The way models are asked questions and how they are designed to answer can affect the fairness of their responses. Even the same model can give different answers based on how the prompt is worded.

<br>

## Training Data for Popular LLMs

The table below shows some popular LLMs and the main datasets they were trained on. These datasets strongly affect what the models learn and how they respond.

| Large Language Model | Training Data Used |
|----------------------|--------------------|
| T5                  | C4 (Colossal Clean Crawled Corpus) |
| BLOOM               | ROOTS (46 natural languages, 13 programming languages) |
| GPT-3               | Common Crawl, WebText, Books, Wikipedia |
| Bard                | Infiniset (proprietary) |
| Stable Diffusion    | LAION-5B |
| BERT                | BookCorpus, English Wikipedia |
| LLaMA 2             | Common Crawl, C4, GitHub, Wikipedia, Books |
| Grok 3              | Web crawls, curated datasets (details not shared) |
| RoBERTa             | BookCorpus, English Wikipedia, CC-News, OpenWebText, Stories |

**Note**: Some of these datasets are public, while others are private or not fully disclosed. If the data is biased — for example, by focusing too much on one region or ignoring certain groups — the model will reflect those biases in its output.

<br>

## Over-representation, Under-representation, or Wrong Information

- LLMs learn by identifying patterns in data.
- So, if some topics or groups appear too much in the data, the model might give them more importance than necessary.
- On the other hand, if certain topics or communities are missing, the model won’t understand or represent them well.
- Some of the training data might be outdated, incorrect, duplicated, or overly focused on certain sources.
- If a model is only trained on news articles or blogs, it won’t be good at writing poetry or technical medical reports.
- The diversity and accuracy of training data are key for building a well-balanced model.

<br>

## Systematic or Unintentional Bias in Data

- Some common areas where data bias may exist are complex and sensitive issues such as racism, gender and sexuality, politics, religion, world affairs, climate change, development, and sustainability.
- Global literature, opinions, news, discussions, and reasoning often reflect the beliefs, value systems, and opinions shaped by specific geographies, cultures, faiths, and historical events.
- When language models are trained on such naturally skewed data, the resulting bias is reflected in both model behavior and output.

<br>

### Different Types of Bias

| **Bias Type**                | **Description**                                      |
|-----------------------------|------------------------------------------------------|
| Demographic bias            | Over- or under-representation of certain groups      |
| Linguistic bias             | Less prevalent languages are underrepresented        |
| Temporal bias               | Data limited to a specific time period               |
| Confirmation bias           | Outputs reinforce specific beliefs or viewpoints     |
| Discrimination and stereotypes | Reflects societal prejudices embedded in data     |

<br>

- Bias can exist both intentionally and unintentionally in the data we collect or analyze. It often stems from natural human perspectives, social systems, or historical context. Below are some common causes and examples of data bias:

| **Cause of Data Bias**      | **Examples**                                                                 |
|----------------------------|------------------------------------------------------------------------------|
| Opinion differences         | - Social issues  <br> - Climate change  <br> - International relations       |
| Belief differences          | - Cultural beliefs  <br> - Religious beliefs                                 |
| Historical imbalances       | - Marginalization of women  <br> - Colonial influences                       |
| Systematic differences      | - Access to healthcare  <br> - Legal representation  <br> - Socio-economic status <br> - Political power |

<br>

## Bias Due to Unclean or Unvetted Data

- This type of bias arises when language models are trained on data that hasn't been properly cleaned or vetted. Filtering can be rule-based, manual, or automated.
- Unclean data may contain unethical, violent, or illegal content. Since language models do not inherently understand ethical or legal boundaries, they may learn and reproduce such harmful content.
- Most models include explicit disclaimers in their release notes acknowledging this risk and cautioning users accordingly.


## Bias in Fine-Tuning Data

- Some models are pre-trained for specific tasks using relatively small datasets.
- If the fine-tuning data is incomplete, incorrect, or biased, the resulting model may fail to perform its intended task effectively.
- After fine-tuning, such a model is often unsuitable for general-purpose use.
- Intentionally introducing incorrect or malicious data during training is known as **data poisoning**.


## Bias in Algorithm

- The training process itself can introduce significant differences in model performance.
- Factors such as model parameters, neural network architecture, and the availability or utilization of computing resources (e.g., GPUs/TPUs) can lead to variations in output.
- These differences may result in biased behavior or inconsistent performance across otherwise similar models.


## Output Bias

- Language models may occasionally generate content that reflects bias.
- Representational bias occurs when the model generalizes negatively about specific social groups.
- Since language models are trained on real-world data—which is inherently biased—they tend to inherit and reflect those societal biases.
- When a language model makes authoritative statements containing social bias, it risks reinforcing and amplifying those stereotypes in society.
