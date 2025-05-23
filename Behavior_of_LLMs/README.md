# Understanding the Behavior of Large Language Models (LLMs)

## Table of Contents
- [Understanding the Behavior of LLMs](#understanding-the-behavior-of-large-language-models-llms)
- [How Language Models Work (A Simple Explanation)](#how-language-models-work-a-simple-explanation)
- [Must-Have Skills for a Language Model](#must-have-skills-for-a-language-model)
- [Training a Large Language Model](#training-a-large-language-model)
- [How Language Models Generate Text](#how-language-models-generate-text)
- [Controlling the Output with Temperature (T)](#controlling-the-output-with-temperature-t)
- [What Happens When We Feed a Prompt to a Large Language Model?](#what-happens-when-we-feed-a-prompt-to-a-large-language-model)
- [Basic Capabilities of Large Language Models](#basic-capabilities-of-large-language-models)

<br>

# Understanding the Behavior of Large Language Models (LLMs)

Large Language Models (LLMs) like ChatGPT, Claude, and others are becoming a big part of our daily work and lives. It’s natural to think that LLMs:
<li> Help extract information quickly </li>
<li> Unlock the power of Artificial Intelligence (AI) </li>
<li> Boost efficiency at work </li>
<li> Personalize our experiences </li>
<li> Automate repetitive tasks </li>
<li> Assist in writing test code </li>
<li> Summarize articles, research papers, and other documents </li>

<br>

But it’s equally important to ask deeper questions:
<li> Can we always trust the answers given by LLMs? </li>
<li> Should we verify the facts they provide? </li>
<li> Could LLMs unintentionally (or intentionally) manipulate information? </li>
<li> What are the hidden costs (money, time, energy) behind using them? </li>
<li> Are there tasks where humans still outperform LLMs? </li>
<li> Is using an LLM always the best choice? </li>

<br>

At first, these questions might sound odd. But once you dive into how LLMs actually work, these concerns start to make a lot of sense.  
Understanding their behavior makes us smarter users of these tools.

<br>

# How Language Models Work (A Simple Explanation)

At their core, <b>language models predict the next word (or part of a word) based on what came before.</b>

More formally:
<li> A language model assigns a probability to a sequence of tokens (small pieces of words or characters).</li>

<br>

Imagine this:
<li> You have a "vocabulary" — a collection of all possible tokens (words or parts of words) the model knows.</li>
<li> Let's call it V = {token1, token2, ..., tokenN}.</li>
<li> You can arrange these tokens in many different sequences.</li>
<li> The language model calculates how likely each sequence is to happen.</li>
<li> The higher the probability, the more "natural" or "correct" the sentence sounds.</li>

<br>

# Example

Suppose the vocabulary contains:  
<b>V = {moon, the, is, satellite, a, natural}</b>

The language model might assign probabilities like this:
<li> P(the, moon, is, a, natural, satellite) → very high probability ✅ </li>
<li> P(a, natural, satellite, is, the, moon) → medium probability </li>
<li> P(a, the, is, moon, natural, satellite) → low probability ❌ </li>

<br>

Thus, the model would prefer to generate the first sequence because it sounds more natural and meaningful.

<br>

> <b>In short:</b><br>
> LLMs don't "understand" language the way humans do — they are <b>guessing</b> the most likely next word based on patterns they've seen during training.

<br>

# Must-Have Skills for a Language Model

<li>
<b>Syntactic Knowledge</b><br>
This helps the language model understand how words can be combined to form meaningful sentences, phrases, or utterances.  
In simple words, it’s about knowing the "grammar rules" of language.
</li>

<br>

<li>
<b>World Knowledge</b><br>
This gives the model an understanding of many different subjects, real-world facts, and common sense.  
It helps the model make connections across various knowledge areas.
</li>

<br>

<li>
<b>Linguistic Knowledge</b><br>
This means knowing detailed information about words — their meanings, relationships, synonyms, grammar, and how they fit together.  
It allows the model to use language more accurately and naturally.
</li>

<br>

# Training a Large Language Model

A large language model is trained on a massive amount of text data.  
This training data is collected from many sources, such as:

<li> Open data available publicly on the internet </li>
<li> Well-known common datasets created for research and AI training </li>
<li> Specially gathered collections like books, encyclopedias, articles, and sometimes even social media posts </li>

<br>

The more diverse and rich the training data, the better the model becomes at understanding and generating human-like language.

<br>

# How Language Models Generate Text

Let's consider an auto-regressive language model.  
An auto-regressive language model predicts the next token based on all previous tokens.

<br>

The probability of generating a sequence of L tokens (x₁, x₂, ..., xₗ) is:

<br>

$$
P(x_1, x_2, ..., x_L) = P(x_1) \times P(x_2 | x_1) \times P(x_3 | x_1, x_2) \times P(x_4 | x_1, x_2, x_3) \times \dots \times P(x_L | x_1, x_2, ..., x_{L-1})
$$

<br>

<b>For example:</b><br>

$$
P(\text{the}, \text{forest}, \text{is}, \text{quiet}) = P(\text{the}) \times P(\text{forest} | \text{the}) \times P(\text{is} | \text{the}, \text{forest}) \times P(\text{quiet} | \text{the}, \text{forest}, \text{is})
$$

<br>

An auto-regressive model efficiently computes these probabilities step-by-step as it generates text.

<br>

# Controlling the Output with Temperature (T)

A parameter called <b>Temperature (T)</b> is used to control how "random" or "creative" the model's outputs are.  
The formula adjusts as:

<br>

$$
x_i = P(x_i | x_1, x_2, ..., x_{i-1})^{1/T}
$$

<br>

<b>What Temperature does:</b>
<li> Lower T (e.g., T = 0.5) → The model sticks to the safest, most logical responses </li>
<li> Higher T (e.g., T = 1.5) → The model might surprise you with creative or unexpected answers </li>

<br>

Choosing the right temperature is important depending on whether you want "safe and reliable" text or "creative and surprising" text.

<br>

# What Happens When We Feed a Prompt to a Large Language Model?

When we prompt a Large Language Model (LLM), we are essentially **fixing the first i tokens** — these are the words (or parts of words) we feed into the model for prediction.

<br>

As a result, the model generates a response that is **conditioned on the input prompt (x₁:i)**.

<br>

<b>In simple terms:</b><br>
The model treats everything you type as the starting point and tries to predict the next most probable tokens based on it.

<br>

Now, if we set a limit like <b>max_tokens = t</b>, then the model will generate the next <b>(i+1) to (i+t)</b> tokens using the probabilistic method we discussed earlier.

<br>

<b>Formula-wise:</b><br>

If you gave it tokens x₁ to xᵢ, then it will predict:

<br>

$$
x_{i+1}, x_{i+2}, ..., x_{i+t}
$$

<br>

where each next token depends on all the previous tokens.

<br>

Thus, the final response is not random — it is shaped very strongly by the prompt you provide!

<br>

# Basic Capabilities of Large Language Models

Large Language Models (LLMs) can perform well at a variety of tasks.  
Broadly, their capabilities can be grouped into:

<br>

## 1. Summarization

LLMs can create concise or detailed summaries from large documents like:
- News articles
- Research papers
- Emails
- Code files

**Key abilities:**
- Create short or long summaries based on user needs
- Identify the focus or main theme of the content
- Tailor summaries depending on the target audience
- Extract just the key points if a brief overview is desired

<br>

## 2. Text Transformation

LLMs can transform text from one style, format, or language to another.

**They are capable of:**
- Translating text between different languages
- Changing the tone (e.g., formal ↔ casual)
- Correcting grammar and spelling
- Translating code between programming languages (e.g., Python → Java)
- Converting natural language descriptions into code (e.g., SQL, Python)

<br>

## 3. Extraction

LLMs can pull out important information from large text bodies.

**They can extract:**
- Sentiments (positive, negative, neutral)
- Specific phrases or language patterns
- Personally Identifiable Information (PII)
- Entities like names, organizations, places, dates
- Values, data points, or facts
- Answers to specific questions
- Main topics or themes

<br>

## 4. Expansion

LLMs can generate new and creative content across different areas.

**They are used for:**
- Writing creative content (stories, poems, scripts)
- Generating blogs, articles, or books
- Idea generation (brainstorming, creative ideation)
- Drafting email responses, proposals, and communication documents
- Producing informative content on new or existing topics
