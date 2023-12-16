Open AI Code 
```
import os
from openai import AzureOpenAI
 
client = AzureOpenAI(
  api_key = "7282c43ed0b549118f59d015ccdc467d",  
  api_version = "2023-05-15",
  azure_endpoint = "https://openapiazconf.openai.azure.com/"
)
 
response = client.chat.completions.create(
    model="prohackathon-2", # model = "deployment_name".
    messages=[
        {"role": "system", "content": "Assistant is a large language model trained by OpenAI."},
        {"role": "user", "content": "suggest me a icecream shop name"}
    ]
)
 
#print(response)
print(response.model_dump_json(indent=2))
print(response.choices[0].message.content)
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


