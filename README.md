# BiasJailbreak

Welcome to the official repository for BiasJailbreak. This repository contains all the necessary resources to get started with BiasJailbreak, including source code, data, and visualizations.

## BiasJailbreak Overview
BiasJailbreak is a robust system designed to prevent malicious jailbreak attempts on AI models. It utilizes advanced bias correction techniques to ensure the security and integrity of large language models. Below is an overview image representing our approach.

<img src="img/fig_2.png" alt="Overview Image" width="70%">

## Jailbreak Success Rate by Keyword
The following image illustrates the success rates of jailbreak attempts categorized by different keywords. This visualization helps identify patterns and weaknesses in the model's response to various prompts.

<img src="img/fig_1.png" alt="Keyword Jailbreak Success Rate" width="70%">

## PCA Results
Here we present the results of our Principal Component Analysis (PCA) on the data. These plots show the distribution and variance explained by the principal components, providing insight into the model's behavior under different conditions.

<img src="img/Phi-3.5-mini-instruct_pca.png" alt="PCA Result 1" width="70%">
<img src="img/Qwen2-7B-Instruct_pca.png" alt="PCA Result 2" width="70%">
<img src="img/Meta-Llama-3-8B-Instruct_pca.png" alt="PCA Result 3" width="70%">

The performance for each model is as follows:
- **LLaMA3**: 0.05
- **Qwen2**: 0.17
- **Phi-mini**: 0.41

A correlation between jailbreak performance and the degree of separation in the latent space clusters was observed.

## Running the Code
To get started with running the BiasJailbreak code, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/BiasJailbreak.git
    cd BiasJailbreak
    ```

2. **Set up your parameters**:
    Ensure you have the necessary parameters set:
    ```python
    token = "your_huggingface_token_here"
    csv_path = "ICLR_github/artifact/gpt3_jailbreak_responses.csv" # load base prompts
    model_id = "Qwen/Qwen1.5-7B-Chat"
    output_filename = 'qwen1.5_jailbreak_response.csv'
    device = "cuda"
    ```

3. **Run the main script**:
    Execute the following command to run the script:
    ```bash
    python src/main.py --csv_path "ICLR_github/artifact/gpt3_jailbreak_responses.csv" --model_id "Qwen/Qwen1.5-7B-Chat" --output_filename "qwen1.5_jailbreak_response.csv" --device "cuda"
    ```

4. **Explore the results**:
    After running the main script, the results will be generated and saved in the artifact URL.
    google drive url: [Google Drive](https://drive.google.com/drive/folders/1PcUnaNqcWXcvVZ0lM1wtsLyToGJOd0r8?usp=sharing)

## Dataset
Jailbreakbench: [https://jailbreakbench.github.io/](https://jailbreakbench.github.io/)
