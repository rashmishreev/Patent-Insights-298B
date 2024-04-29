* Prompt Engineering *

Purpose: Generation of synthetic dataset for fine-tuning

Approach 1
Manual using ChatGPT interface. 
-> Search for a patent within a specific domain or CPC class on Google Patents. Identify patents that share similarities with it. Provide a summary of each patent, including the abstract, summary, and claims. Use this information as the training data for fine-tuning, incorporating various use cases such as acceptance, rejection, inability to assess due to the submission of more than two patents for novelty evaluation, and other scenarios.


Approach 2 
Platform: Perplexity AI
Model: GPT-4

Prompt:1

Original: For the purpose of testing an AI system to detect plagiarized and non-plagiarized content, to prepare training data, can you help me generate a plagiarized and 
non-plagiarized content for the patent https://patents.google.com/patent/US20240022595A1 with Title, Abstract, Claims, and Summary.

Enhanced with ChatGPT: I am conducting a comprehensive evaluation of an AI system designed to identify plagiarized and non-plagiarized content. To facilitate the creation of robust training data, I need 
assistance in generating both plagiarized and non-plagiarized textual content for the patent with the identifier https://patents.google.com/patent/US20240022595A1. Specifically, I am 
interested in variations for the Title, Abstract, Claims, and Summary sections of the patent document. Your input will contribute to a more thorough assessment of the AI system's 
capabilities in detecting plagiarism. Please provide diverse and nuanced content to ensure a rigorous evaluation.

Approach 3
Utilize the gpt-llm-trainer Python script by Matt Shumer [https://github.com/mshumer/gpt-llm-trainer] to create the dataset, employing both gpt-3.5-turbo and gpt-4 to ensure a variety of examples are included.