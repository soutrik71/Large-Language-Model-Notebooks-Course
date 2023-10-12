# Large Language Models Course: Learn Building LLM Projects.
This practical course about Large Language models and their applicacions is in development, I will be posting the different lessons as I complete them. 

The course provides a hands-on experience using models from OpenAI and the Hugging Face library. We are going to see and use a lot of tools and practice with small projects that will grow as we can apply the new knowledge"

Some of the topics and technologies covered in the course include:
 
* Chatbots. 
* Code Generation.
* OpenAI API.
* Hugging Face. 
* Vector databases.
* LangChain.
* Fine Tuning
* PEFT Fine Tuning
  - Soft Prompt tuning.
  - LoRA.
* Evaluate Models. 
* Knowdledge Distillation.

Each notebook is supported with a Medium article where the code is explained in detail. 
## Introduction to Large Language Models with OpenAI.
In this first section of the course, we will learn to work with the OpenAI API by creating two small projects. We'll delve into OpenAI's roles and how to provide the necessary instructions to the model through the prompt to make it behave as we desire.

The first project is a restaurant chatbot where the model will take customer orders. Building upon this project, we will construct an SQL statement generator. Here, we'll attempt to create a secure prompt that only accepts SQL creation commands and nothing else.
### Create Your First Chatbot Using GPT 3.5, OpenAI, Python and Panel.
We will be utilizing OpenAI GPT-3.5 and Panel to develop a straightforward Chatbot tailored for a fast food restaurant. During the course, we will explore the fundamentals of prompt engineering, including understanding the various OpenAI roles, manipulating temperature settings, and how to avoid Prompt Injections. 
* Article: https://medium.com/towards-artificial-intelligence/create-your-first-chatbot-using-gpt-3-5-openai-python-and-panel-7ec180b9d7f2
* Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/1-Introduction%20to%20LLMs%20with%20OpenAI/Vertical%20Chat.ipynb

### How to Create a Natural Language to SQL Translator Using OpenAI API.
Following the same framework utilized in the previous article to create the ChatBot, we made a few modifications to develop a Natural Language to SQL translator. In this case, the Model needs to be provided with the table structures, and adjustments were made to the prompt to ensure smooth functionality and avoid any potential malfunctions.

With these modifications in place, the translator is capable of converting natural language queries into SQL queries. 
* Article: https://pub.towardsai.net/how-to-create-a-natural-language-to-sql-translator-using-openai-api-e1b1f72ac35a
* Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/1-Introduction%20to%20LLMs%20with%20OpenAI/nl2sql.ipynb
  
## Vector Databases with LLM. 
A brief introduction to Vector Databases, a technology that will accompany us in many lessons throughout the course. We will work on an example of Retrieval Augmented Generation using information from various news datasets stored in ChromaDB.

### Influencing Language Models with Personalized Information using a Vector Database. 
If there's one aspect gaining importance in the world of large language models, it's exploring how to leverage proprietary information with them. In this lesson, we explore a possible solution that involves storing information in a vector database, ChromaDB in our case, and using it to create enriched prompts.
* Article: https://pub.towardsai.net/harness-the-power-of-vector-databases-influencing-language-models-with-personalized-information-ab2f995f09ba?sk=ea2c5286fbff8430e5128b0c3588dbab
* Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/2-Vector%20Databases%20with%20LLMs/how-to-use-a-embedding-database-with-a-llm-from-hf.ipynb

## LangChain
LangChain has been one of the libraries in the universe of large language models that has contributed the most to this revolution. 
It allows us to chain calls to Models and other systems, allowing us to build applications based on large language models. In the course, we will use it several times, creating increasingly complex projects.

### Retrieval Augmented Generation (RAG). Use the Data from your DataFrames with LLMs.
In this lesson, we used LangChain to enhance the notebook from the previous lesson, where we used data from two datasets to create an enriched prompt. This time, with the help of LangChain, we built a pipeline that is responsible for retrieving data from the vector database and passing it to the Language Model. The notebook is set up to work with two different datasets and two different models. One of the models is trained for Text Generation, while the other is trained for Text2Text Generation.
* Article: https://medium.com/towards-artificial-intelligence/query-your-dataframes-with-powerful-large-language-models-using-langchain-abe25782def5
* Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/3-LangChain/ask-your-documents-with-langchain-vectordb-hf.ipynb

### Create a Moderation system using LangChain. 
We will create a comment response system using a two-model pipeline built with LangChain. In this setup, the second model will be responsible for moderating the responses generated by the first model.

One effective way to prevent our system from generating unwanted responses is by using  a second model that has no direct interaction with users to handle response generation. 

This approach can reduce the risk of undesired responses generated by the first model in response to the user's entry. 


I will create separate notebooks for this task. One will involve models from OpenAI, and the others will utilize open-source models provided by Hugging Face. The results obtained in the three notebooks are very different. The system works much better with the OpenAI, and LLAMA2 models. 
* OpenAI article: https://pub.towardsai.net/create-a-self-moderated-commentary-system-with-langchain-and-openai-406a51ce0c8d?sk=b4903b827e44642f7f7c311cebaef57f
* OpenAI notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/3-LangChain/LangChain_OpenAI_Moderation_System.ipynb
  
* Hugging Face Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/3-LangChain/HF_gpt_j_6b_Moderation_System.ipynb

* Llama2-7B Article: https://levelup.gitconnected.com/create-a-self-moderated-comment-system-with-llama-2-and-langchain-656f482a48be?sk=701ead7afb80e015ea4345943a1aeb1d
* Llama2-7B Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/3-LangChain/HF_LLAMA2_LangChain_Moderation_System.ipynb

### Create a Data Analyst Assistant using a LLM Agent. 
Agents are one of the most powerful tools in the world of Large Language Models. The agent is capable of interpreting the user's request and using the tools and libraries at its disposal until it achieves the expected result.

With LangChain Agents, we are going to create in just a few lines one of the simplest yet incredibly powerful agents. The agent will act as a Data Analyst Assistant and help us in analyzing data contained in any Excel file. It will be able to identify trends, use models, make forecasts. In summary, we are going to create a simple agent that we can use in our daily work to analyze our data.

* Article: https://pub.towardsai.net/create-your-own-data-analyst-assistant-with-langchain-agents-722f1cdcdd7e
* Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/3-LangChain/LangChain_Agent_create_Data_Scientist_Assistant.ipynb

## Evaluating LLMs
The metrics used to measure the performance of Large Language Models are quite different from the ones we've been using in more traditional models. We're shifting away from metrics like Accuracy, F1 score, or recall, and moving towards metrics like BLEU, ROUGE, or METEOR. 

These metrics are tailored to the specific task assigned to the language model. 

In this section, we'll explore examples of several of these metrics and how to use them to determine whether one model is superior to another for a given task. We'll delve into practical scenarios where these metrics help us make informed decisions about the performance of different models.

### Evaluating Summarization with ROUGE. 
We will explore the usage of the ROUGE metric to measure the quality of summaries generated by a language model. 
We are going to use two T5 models, one of them being the t5-Base model and the other a t5-base fine-tuned specifically designed for creating summaries.

* Article: https://medium.com/towards-artificial-intelligence/rouge-metrics-evaluating-summaries-in-large-language-models-d200ee7ca0e6
* Notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/4-Evaluating%20LLMs/rouge-evaluation-untrained-vs-trained-llm.ipynb

## Fine Tuning & Optimization. 
In the FineTuning & Optimization section, we will explore different techniques such as Prompt Fine Tuning or LoRA, and we will use the Hugging Face PEFT library to efficiently fine-tune Large Language Models. We will explore techniques like quantization to reduce the weight of the Models. 

### Prompt tuning using PEFT Library from Hugging Face. 
In this notebook, two models are trained using Prompt Tuning from the PEFT library. This technique not only allows us to train by modifying the weights of very few parameters but also enables us to have different specialized models loaded in memory that use the same foundational model.

Prompt tuning is an additive technique, and the weights of the pre-trained model are not modified. The weights that we modify in this case are those of virtual tokens that we add to the prompt.
* article: https://medium.com/towards-artificial-intelligence/fine-tuning-models-using-prompt-tuning-with-hugging-faces-peft-library-998ae361ee27
* notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/5-Fine%20Tuning/Prompt_Tuning_PEFT.ipynb

### Fine-Tuning with LoRA using PEFT from Hugging Face. 
After a brief explanation of how the fine-tuning technique LoRA works, we will fine-tune a model from the Bloom family to teach it to construct prompts that can be used to instruct large language models.
* article: https://levelup.gitconnected.com/efficient-fine-tuning-with-lora-optimal-training-for-large-language-models-266b63c973ca?sk=85d7b5d78e64e568faedfe07a35f81bd
* notebook: https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/5-Fine%20Tuning/LoRA_Tuning_PEFT.ipynb
_____________
The course will consist of a minimum of 20 articles. To stay updated on new articles, don't forget to follow the repository or starring it. This way, you'll receive notifications whenever new content is added. 
_____________
# Papers used in the Course: 
[The Power of Scale for Parameter-Efficient Prompt Tuning](https://doi.org/10.48550/arXiv.2104.08691). Fine Tuning & Optimizacion Lesson. Prompt Tuning Sample. 

[LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685). Fine Tuning & Optimizacion Lesson. LoRA Tuning Sample. 

