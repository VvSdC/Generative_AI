# Impact of Large Language Models on environment

- Negative impacts of large language models :
    - Carbon footprint
    - Energy consumption


### What is Carbon Footprint

> Carbon footprint refers to the **total amount of greenhouse gases** emitted directly or indirectly by an activity, product, or organization, typically measured in terms of **carbon dioxide equivalents (CO₂e)**.

- 🌍 **Greenhouse gases** such as water vapor, carbon dioxide (CO₂), chlorofluorocarbons (CFCs), nitrous oxide (N₂O), and methane (CH₄) trap heat from the sun’s rays, warming the **troposphere** (the lowest layer of Earth’s atmosphere). This phenomenon is known as the **greenhouse effect**.
- 🔥 **Greenhouse Warming Potential (GWP)** refers to the impact a greenhouse gas has on global warming, based on:
  - Its **abundance**
  - Its **lifetime** in the atmosphere
- 🕒 **Carbon dioxide** has an atmospheric lifetime of **300–1000 years**, making it one of the **most harmful greenhouse gases**.
- 🌡️ The increase in greenhouse gas emissions leads to **global warming**.
- 🧮 A **carbon footprint** accounts for all the greenhouse gas emissions caused by a specific **activity**, **product**, or **company**.
> ⚠️ **Anything that increases the carbon footprint poses a serious threat to environmental sustainability.**


### Carbon Footprint of Large Language Models

> Large Language Models (LLMs) have a significant carbon footprint due to their high energy consumption throughout their lifecycle.

- ⚡ The **computing hardware** required to train and run LLMs consumes a **large amount of energy**.
- 🔄 Since **energy production itself generates emissions**, the energy consumed by LLMs indirectly contributes to their **carbon footprint**.
- 📊 **Training a 175 billion parameter language model** can consume as much energy as required to power an **average American home for 40 years**.
- ⚙️ LLMs consume energy during both:
  - **Training phase** — when the model learns from data.
  - **Inference phase** — when the model generates responses.
- 🏢 **Data centers** housing these models also contribute to emissions due to:
  - High **air conditioning needs**  
  - Continuous **power supply requirements**
- 🏗️ The **manufacturing and maintenance** of infrastructure (servers, cooling systems, etc.) have their own carbon footprints and contribute to the **depletion of natural resources**.

> ✅ **Reducing the carbon footprint** of LLMs requires:
  - Designing **efficient training algorithms**
  - Optimizing **data center cooling and energy management**  
  - Implementing solutions like the **BCOOLER algorithm** for energy-efficient training



### Different Types of Emissions Due to Large Language Models

> Training and deploying large language models contribute to various forms of carbon emissions, both direct and indirect.

#### 1. ⚙️ Embodied Emissions  
Emissions associated with the **materials, production, and deployment** of computing infrastructure used in machine learning.
- **Dynamic Consumption**
  - Refers to the **electricity required to power the model during training**.
  - Measures the **energy consumed by servers** actively running training tasks.
- **Idle Power Consumption**
  - Energy consumed by **servers that are powered on but not actively used**.
  - Also includes energy used by supporting infrastructure just to **keep systems ready**.
- **Infrastructure Consumption**
  - Energy used by **data center infrastructure**, including:
    - Networking equipment  
    - Cooling systems  
    - Maintenance operations  
#### 2. 🔄 Operational Emissions  
Emissions resulting from **real-time use**, such as when models are deployed to handle user queries, including power required to run inference and maintain system availability.


### An Interesting Study

> 🔍 **Conclusion from Facebook AI Research:**  
> While the overall carbon footprint of machine learning models is currently smaller than many other sources, it is growing rapidly and will soon become a significant concern.  
> A rough power consumption breakdown of AI infrastructure shows **10% for experimentation, 20% for training, and 70% for inference**.  
> This reveals that **training emissions are just the tip of the iceberg**, and **inference — the most frequently occurring phase — is the largest contributor** to the long-term environmental impact of large language models.
