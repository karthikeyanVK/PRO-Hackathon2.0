Open AI Code 
```
import os
from openai import AzureOpenAI
    
client = AzureOpenAI(
    api_key="7282c43ed0b549118f59d015ccdc467d",  
    api_version="2023-10-01-preview",
    azure_endpoint = "https://openapiazconf.openai.azure.com/"
    )
    
deployment_name='azconfmodel' #This will correspond to the custom name you chose for your deployment when you deployed a model. 
    
# Send a completion call to generate an answer
print('Sending a test completion job')
start_phrase = 'Write a tagline for an ice cream shop. '
response = client.completions.create(model=deployment_name, prompt=start_phrase, max_tokens=10)
print(response.choices[0].text)
```
RAG Sample

https://colab.research.google.com/drive/1_k_vdynZOvPO7p7eWe3hpQdgdtgCFa1L#scrollTo=AsI2Y_JnHUKk

UI Interface:

Packages: Chainlit, Gradio, Any front-end code
Purpose: Interface for user interaction and input.
Query Processor:

Package: GPT-4
Purpose: Descriptive processing, understanding user queries or descriptions.
Model Creation:

Package: Lazy
Purpose: Creating predictive models dynamically at runtime based on user input.


