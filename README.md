# medical_chatbot_opensource_llm_llama2



## How to run?

#### Clone the repository

Project repo: https://github.com/veerandra7/medical_chatbot_opensource_llm_llama2.git

### STEPS 

#### STEP 01- Create a conda environment after opening the repository

conda create -n medical_chatbot_opensource_llm_llama2 python=3.8 -y

conda activate medical_chatbot_opensource_llm_llama2

#### STEP 02- install the requirements
pip install -r requirements.txt

#### STEP 03
Create a .env file in the root directory and add your Pinecone credentials as follows:

PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"

PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"

#### STEP 04
Download the quantize model from the link provided in model folder & keep the model in the model directory:

#### LLM model name : 

llama-2-7b-chat.ggmlv3.q4_0.bin

#### Dwonload the opensource LLM From the following link:

https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main


#### Embedding model name : 

sentence-transformers/all-MiniLM-L6-v2

#### Embedding model link :

https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2/tree/main

The dimension of the embedding model is 384.

Go to PINECONE,

Create the index(index_name = "medical-chatbot-opensource-llm-llama2") in PINECONE DB by putting the vector dimension as 384.



# run the following command
python store_index.py

# Finally run the following command
python app.py

#### Fially , 

open up localhost:

#### Techstack Used:
Python

LangChain

Flask

Meta Llama2

Pinecone



