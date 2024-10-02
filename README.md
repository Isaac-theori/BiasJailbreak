# PCJailbreak

Welcome to the official repository for PCJailbreak. This repository contains all the necessary resources to get started with PCJailbreak, including source code, data, and visualizations.

## PCJailbreak Overview
PCJailbreak is a robust system designed to prevent malicious jailbreak attempts on AI models. It utilizes advanced bias correction techniques to ensure the security and integrity of large language models. Below is an overview image representing our approach.

![Overview Image](img/fig_2.png)

## Jailbreak Success Rate by Keyword
The following image illustrates the success rates of jailbreak attempts categorized by different keywords. This visualization helps identify patterns and weaknesses in the model's response to various prompts.

![Keyword Jailbreak Success Rate](img/fig_1.png)

## PCA Results
Here we present the results of our Principal Component Analysis (PCA) on the data. These plots show the distribution and variance explained by the principal components, providing insight into the model's behavior under different conditions.

![PCA Result 1](img/Phi-3.5-mini-instruct_pca.png)
![PCA Result 2](img/Qwen2-7B-Instruct_pca.png)
![PCA Result 3](img/Meta-Llama-3-8B-Instruct_pca.png)

LLaMA3 0.05 0.0650 (+0.015) 0.0300 (-0.020) 0.035
Qwen-1.5 0.19 0.2175 (+0.028) 0.1675 (-0.022) 0.050
Qwen2 0.17 0.1971 (+0.027) 0.1671 (-0.012) 0.030
Phi-mini 0.41

## Running the Code
To get started with running the PCJailbreak code, follow these steps:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/pcjailbreak.git
    cd pcjailbreak
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
    python main.py --csv_path "ICLR_github/artifact/gpt3_jailbreak_responses.csv" --model_id "Qwen/Qwen1.5-7B-Chat" --output_filename "qwen1.5_jailbreak_response.csv" --device "cuda"
    ```

4. **Explore the results**:
    After running the main script, the results will be generated and saved in the artifact URL.
    google drive url: https://drive.google.com/drive/folders/1PcUnaNqcWXcvVZ0lM1wtsLyToGJOd0r8?usp=sharing
