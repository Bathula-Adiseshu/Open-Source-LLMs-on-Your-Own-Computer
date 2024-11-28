# Open-Source-LLMs-on-Your-Own-Computer
## Chatbot with Llama 
### Get the Llama models
#### A screenshot from Hugging Face showing access
![Screenshot from 2024-11-28 11-03-16](https://github.com/user-attachments/assets/47d495e7-e0f2-4f32-b4cf-005e1ffade07)
### A screenshot of the downloaded local files using ls -al .
![Screenshot from 2024-11-28 11-08-15](https://github.com/user-attachments/assets/32917b03-40ee-40fa-a19f-04d2797a68db)
#### The appropriate download link of Q5_K_M quantitized Phi-3 mini model from Microsoft.
https://huggingface.co/microsoft/Phi-3-mini-4k-instruct-gguf/blob/main/Phi-3-mini-4k-instruct-q4.gguf
![image](https://github.com/user-attachments/assets/bbb9fdc9-c32d-4525-879d-fb4d0a85d380)
### Inference on the command-line
#### Ask a different question in the conversation and A screenshot of the output of the answer..
![Screenshot from 2024-11-28 11-32-47](https://github.com/user-attachments/assets/77f0b13f-0314-4df2-9b9a-76bd5d1b5476)
### Use the Chat Template to Carry a Conversation
#### Ask the next question in the conversation. Write it down as a complete command. A screenshot of the output in response to the next question in the conversation. 
wasmedge --dir .:. \
  --nn-preload default:GGML:AUTO:Phi-3-mini-4k-instruct-q4.gguf \
  llama-chat.wasm \
  --prompt-template llama-3-chat \
  --system-prompt "You are a high school social teacher. Explain the concepts of earth geography."
![Screenshot from 2024-11-28 11-54-44](https://github.com/user-attachments/assets/103b9df3-e925-4f5c-9b69-e1256239c5c2)
### Create a Web Service API
#### Ask the next question in the conversation. Write it down as a complete command. A screenshot of the output in response to the next question in the conversation.
![Screenshot from 2024-11-28 12-03-50](https://github.com/user-attachments/assets/043b3b2c-85a2-421a-8c53-5301c0b4c0bd)
### Create a Chatbot
#### Change the “system prompt” for the chatbot-ui to “You are a tour guide for Western tourists in Japan.” Then, submit the screenshot. Ask a few questions about Japan in chatbot-ui. Submit the screenshots. Configure LobeChat to use the http://localhost:8080/v1 as an "OpenAI API proxy address". Submit the screenshot. Chat on LobeChat. Submit the screenshot.
![Screenshot from 2024-11-28 12-16-28](https://github.com/user-attachments/assets/12941a2e-948b-44ae-94e2-c8f0bd6f587f)
## Add Knowledge to the Chatbot
### Create a Vector Database for External Knowledge
#### The output of curl 'http://localhost:6333/collections/chemistry' and a zip file containing the snapshot from the chemistry collection.
![Screenshot from 2024-11-28 12-24-57](https://github.com/user-attachments/assets/df055a9d-a390-40ff-80d5-5d92865f25ba)
### Improve the Vector Collection for Longer Context Windows
#### The chemistry.csv file you generated. The output of curl 'http://localhost:6333/collections/chemistry'. A zip file containing the snapshot from the chemistry collection.
![Screenshot from 2024-11-28 12-24-57](https://github.com/user-attachments/assets/908b03e1-fd5c-44d6-8fbb-2388c9b92548)
### Start an RAG API Server

