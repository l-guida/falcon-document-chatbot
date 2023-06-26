# falcon-document-chatbot

![alt text](assets/chat_falcon.png)

![alt text](assets/arch.png)


## How to run the application in Amazon SageMaker Studio
1. Launch Amazon SageMaker Studio and launch the Terminal (File > New > Terminal)
2. Run `git clone https://github.com/l-guida/falcon-document-chatbot.git`
3. Deploy Falcon-7B or Falcon-40B in your account. You can use the `deploy-falcon-7b-instruct.ipynb` notebook to deploy Falcon-7B, or, as an alternative, the `deploy-falcon-40b-instruct.ipynb` notebook to deploy Falcon-40B.
4. While waiting for the model to be deployed, run the following commands
  `cd falcon-document-chatbot`
  `pip3 install -r requirements.txt`
5. Wait for model deployment completion (approximately 7 minutes for Falcon-7B). Once completed, Depending on the model you deployed, run
  `streamlit run chatbot-7b.py —server.port 8501`
  or
  `streamlit run chatbot-40b.py —server.port 8501`
6. Navigate to the Streamlit app. Copy the URL you find in the browser address bar and replace `lab/tree/falcon-document-chatbot` with `proxy/8501/` (the port may not be 8501 - check the Terminal for further details)
