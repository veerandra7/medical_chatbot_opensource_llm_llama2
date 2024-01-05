# Medical_chatbot_opensource_llm_llama2



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

From huggingface,
we can find that the vector dimension of above embedding model is 384

Go to PINECONE,

Create the index(index_name = "medical-chatbot-opensource-llm-llama2") in PINECONE DB by putting the vector dimension as 384.


#### run the following command


python store_index.py

#### Finally run the following command
python app.py

#### Fially , 

open up localhost:

#### Techstack Used:
Python

LangChain

Flask

Meta Llama2

Pinecone


## If creating from scratch

create the conda env like mentioned above.. 

step1 :  create and run the template.py file to create the folder structure.

step2 : create setup.py file to install "src" folder as your local package. or else, we won't be able to import src

step3 : Go to PINECONE and create "PINECONE_API_KEY" and "PINECONE_API_ENV".

step4 : create ".env" file and add "PINECONE_API_KEY" and "PINECONE_API_ENV" credentials in it. and add ".env" to gitignore

        example : PINECONE_API_KEY = "XXXXXXXXX"
                  PINECONE_API_ENV = "XXXXXXXXX"

step5 : create "helper.py" file

step6 : Go to PINECONE, Create the index(index_name = "medical-chatbot-opensource-llm-llama2") in PINECONE DB by putting the vector dimension as 384

step7 : create and run the "store_index.py" file 

step8 : create "prompt.py" in src folder

step9 : create "app.py"

step10 : create "chat.html" in templates folder

step11 : create "style.css" in static folder

step12 : run app.py with following command "python app.py"

step13 : open newtab in your browser, search for "localhost:8080" and post any of your query from the input pdf


