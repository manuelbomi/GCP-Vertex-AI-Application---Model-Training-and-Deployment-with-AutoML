# GCP-Vertex-AI-Application---Model-Training-and-Deployment-with-AutoML
#### Brief Background About GCP's Vertex AI
Vertex AI is a comprehensive, unified machine learning (ML) platform offered by Google Cloud Platform (GCP). It enables developers  to build, train, deploy, and scale ML models and AI applications, including those leveraging large language models (LLMs). It integrates data engineering, data science, and ML engineering workflows, enabling teams to collaborate effectively and leverage GCP's infrastructure for scalability.

In this discourse, we shall show in details how Vertex AI can be used to train, build and deploy a model that can be used to predict whether on not a bank customer will make a deposit. The training data can be downloaded from Kaggle and interested users can also obtain it through this repo at: https://github.com/manuelbomi/GCP-Vertex-AI-Application---Model-Training-and-Deployment-with-AutoML/blob/main/bank-data.csv

#### Project Initiation on GCP
##### To start the Start a new Vertex AI project, log into your GCP home page and start by creating a named project

![Image](https://github.com/user-attachments/assets/7b181aff-5e21-497b-8f9c-f14752fda45f)

##### After creating the project, select the project

![Image](https://github.com/user-attachments/assets/7abb53e2-00ea-4710-99c2-927f2b859042)

##### Associate the project to a billing account
In this discourse, we also provided details about the cost implication of using Vertex AI to train the model an ddeploy it. The cost implication shall provide some relative guidance regarding cost to developers. 

![Image](https://github.com/user-attachments/assets/3fe94f99-994d-44fa-894e-1e6bf6a6945d)

##### Navigate back to your homepage at cloud.google.com and select 'view all products'


![Image](https://github.com/user-attachments/assets/91746335-ba86-4d4f-a643-027af53d0872)

##### Look for Vertex AI and pin it to ur menu for easier accessibility for subsequent projects. 
##### Select Vertex AI


![Image](https://github.com/user-attachments/assets/4631d4e0-b70a-4d8e-b6fa-baaa7b474fa7)

##### Enable vertexAI


![Image](https://github.com/user-attachments/assets/58c86c68-9da5-4849-9ff1-78e6ba1c88c5)

##### Select datasets on the left hand menu


![Image](https://github.com/user-attachments/assets/82313eee-8ecf-46a8-b545-6ed319f50c6a)

##### Select create dataset


 ![Image](https://github.com/user-attachments/assets/79587aa5-c6d3-441e-8f42-ffcfc0102ee8)

##### Select region.  Give the dataset a name 
##### select regression as the type of analysis


![Image](https://github.com/user-attachments/assets/bbe0af1e-5285-4f6c-900c-3ade56c770a2)

##### Click the appropriate region and select create

![Image](https://github.com/user-attachments/assets/d5dc461f-f476-405e-8e3d-dfbabe9f6c8a)

##### Add data to your project

![Image](https://github.com/user-attachments/assets/3bb9d1f2-e7a2-46c4-abb8-4157c007bc82)

##### Select a cloud storage path to upload data to


![Image](https://github.com/user-attachments/assets/551b54e1-b43d-4116-98d4-964a0bf18226)

##### Click 'generate statistics'

![Image](https://github.com/user-attachments/assets/f6798449-3904-451f-89c4-746e1457f0af)

##### Here is a summary of the data statistics 

![Image](https://github.com/user-attachments/assets/e88ba39b-8dba-411e-a929-750ccf86d796)

##### Click on any column to see detailed statistics
![Image](https://github.com/user-attachments/assets/868a4477-ba4e-47d0-b299-424e124c25c2)

##### Example of age statistics

![Image](https://github.com/user-attachments/assets/71a51858-fc68-4eaf-b561-552c13161d5a)


![Image](https://github.com/user-attachments/assets/24baa201-dcb0-4387-9ff6-ae75eea48c4e)

#### Model Training

click train new model and select AutoML to let VertexAI select best model for this dataset

![Image](https://github.com/user-attachments/assets/991796ea-c57e-418a-8f61-e83d98b59851)

enable dataflow

![Image](https://github.com/user-attachments/assets/23a0d56e-2694-4875-9960-2edf8c0339ce)

select the one off training method

![Image](https://github.com/user-attachments/assets/de88d581-9532-4dbe-b8a3-73f8db296012)

choose an output directory for the model

![Image](https://github.com/user-attachments/assets/5c36c296-d06c-4e5b-ac3f-56fc8e463c15)

Choose the target column (deposit column in our case)

![Image](https://github.com/user-attachments/assets/7ef23e59-a780-4197-8b84-df33a83228f8)

You can choose to allow AUtoML to choose best transformation option

![Image](https://github.com/user-attachments/assets/71b538e5-5abe-4f4e-b240-fdb11aef95cd)

enable the early stopping transformation option

![Image](https://github.com/user-attachments/assets/d141fa4c-1627-4800-8364-58826c2b506a)

choose an estimated budget time for training your model. Average could be 2 hours depending on dataset

![Image](https://github.com/user-attachments/assets/62f08519-b088-4e58-a229-e7cf4d3a42b5)

grant the necessary roles under IAm permissions

![Image](https://github.com/user-attachments/assets/a01da254-a9d1-4c10-b631-7e8872d33e46)

 grant the necessary roles under IAM permission if required

 ![Image](https://github.com/user-attachments/assets/3fb139b5-2d74-4d30-88e8-b148eeb784ac)

 some runtime analysis

 ![Image](https://github.com/user-attachments/assets/def3bf12-2fe6-4f71-a469-ea34890611c9)

 model registry

 ![Image](https://github.com/user-attachments/assets/80f18ea7-0f68-4a66-bd71-fc0ab9596fcf)

 click model and see some stats details

 ![Image](https://github.com/user-attachments/assets/0e159439-ab3c-4232-9ca8-3c91d1f9687d)

 precision and recall

 ![Image](https://github.com/user-attachments/assets/e7fa02d5-341d-4d5d-9c42-5eee2f74ce5c)

 precsion

 ![Image](https://github.com/user-attachments/assets/6ae1c147-e854-4661-a1d9-4e1fe473ec7a)

 confusion matrix

 ![Image](https://github.com/user-attachments/assets/7c7696f6-4484-4508-af70-d9e7826ff6a4)

  feature importance

![Image](https://github.com/user-attachments/assets/9526302f-b773-4bbf-b434-6520abaad89b)

go to deploy and test

![Image](https://github.com/user-attachments/assets/82b8d374-c5c9-458d-9afc-ae924f70ab82)

deploy to a named endpoint

![Image](https://github.com/user-attachments/assets/858726b2-0d9c-481b-8251-33d8736faa40)

Deploy model to the named endpoint

![Image](https://github.com/user-attachments/assets/61502b74-5ffc-4147-a0e3-db5d3a6a945d)

enable model monitoring to prevent drift

![Image](https://github.com/user-attachments/assets/e6104367-1a2a-4ad2-b001-9f220f7dc909)

 select prediction drift detection

 ![Image](https://github.com/user-attachments/assets/30ea1491-f08e-4dc1-bfa1-175621a8a612)

 endpoint will be created

 ![Image](https://github.com/user-attachments/assets/5878cb98-6f87-4a7b-a324-919be129b0ce)

 predict with your model

 ![Image](https://github.com/user-attachments/assets/868caef5-817b-4e4f-81da-1ef2d92aace4)

 predict wit your model

 ![Image](https://github.com/user-attachments/assets/73e869a2-ff5c-4784-b358-995f3281dcd4)

deposit yes 35% no 65 %

 ![Image](https://github.com/user-attachments/assets/1d41d8e5-b4b4-440d-b74c-37805ed79293)

 


 ![Image](https://github.com/user-attachments/assets/87972efa-74c8-4123-89c0-62bab768c606)

  Vary age and job deposit 79%

  ![Image](https://github.com/user-attachments/assets/662a5c10-dbdc-4747-9154-1320a271d335)

  cost over $64 USD

  ![Image](https://github.com/user-attachments/assets/3d7459d6-3448-4139-8440-3170b450c9f8)


##### Cost Implication
Cost of running and deploying the model as shown by GCP Gemini is a littel over $64 (USD), which looks a little steep given that the model was trained for less than 4 hours.

   ![Image](https://github.com/user-attachments/assets/b07d8c7e-897e-4951-bbaa-50cc8e3d75eb)

Complete breakdown of the cost could be obtained at:   https://github.com/manuelbomi/GCP-Vertex-AI-Application---Model-Training-and-Deployment-with-AutoML/blob/main/Cost%20of%20training%20model%20by%20GCP%20Vertex%20AI.csv

   

  




