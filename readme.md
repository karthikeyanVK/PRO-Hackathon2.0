
```
import os
from openai import AzureOpenAI
    
client = AzureOpenAI(
    api_key="a34a353bd97c49f2917b7eb8d824e7ef",  
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
Run the cell and see the output
