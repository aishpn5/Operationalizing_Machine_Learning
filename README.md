# Operationalizing Machine Learning

In this project, we worked with the Bank Marketing dataset. We used Azure to configure a cloud-based machine learning production model, deploy it, and consume it. We also created, published, and consumed a pipeline. 

Architectural diagram![image](https://user-images.githubusercontent.com/48025239/112717396-66188b80-8f12-11eb-993a-fd53c7852bc6.png)

## Key Steps

1.Authentication : Here, we create a Security Principal (SP) to interact with the Azure Workspace.
2.Automated ML Experiment : In this step, we create an experiment using Automated ML, configure a compute cluster, and use that cluster to run the experiment.
3.Deploy the best model : Deploying the Best Model will allow us to interact with the HTTP API service and interact with the model by sending data over POST requests.
4.Enable logging : Logging helps monitor our deployed model. It helps us know the number of requests it gets, the time each request takes, etc.
5.Swagger Documentation : In this step, we consume the deployed model using Swagger.
6.Consume model endpoints : We interact with the endpoint using some test data to get inference.
Create and publish a pipeline : In this step, we automate this workflow by creating a pipeline with the Python SDK.

First of all , we create a new automated ml run in MS Azure Studio by selecting and uploading the bank marketing dataset and run the experiment using Classification.

Registered Dataset![registered dataset](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/registered%20dataset.png)

Best Model![best model](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/best%20model.png)

Then we deployed the best model (the Voting Ensemble, in our case) using Azure Container Instance and enabled authentication.
After the deploy is successful, we run the logs.py file to enable application insights.

Logs![logs](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/logs.png)

Application Insights Enabled![appInsightsEnabled](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/appInsightsEnabled.png)

Then we consume the model using swagger by downloading the swagger.json file using the swagger uri of the deployed model and run the swagger.sh and serve.py files in different terminals.

We interacted with the swagger instance running with the documentation for the HTTP API of the model by displaying the contents of the API for the model.

Swagger run![swagger run](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/swagger%20run.png)

Swagger interaction![swagger interaction](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/swagger%20interaction.png)

Next we consumed model endpoints by modifying the scoring_uri and key to match the key for our service and the URI that was generated after deployment . 

Endpoint and Benchmark![endpoint and benchmark](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/endpoint%20and%20benchmark.png)

Finally, we created and published a pipeline using the jupyter notebook provided in the starter files.

Pipeline![pipeline](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/pipeline.png)

Pipeline run![pipeline run](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/pipeline%20run.png)

Pipeline run complete![pipeline run complete](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/pipeline%20run%20complete.png)

Automl module![automl module](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/automl%20module.png)

Automl steps![automl steps](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/automl%20steps.png)

Pipeline endpoint![pipeline endpoint](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/pipeline%20endpoint.png)

Pipeline endpoint status active![pipeline endpoint status active](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/pipeline%20endpoint%20status%20active.png)

Run metrics![run metrics](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/run%20metrics.png)

Rundetails widget![rundetails widget](https://github.com/aishpn5/Operationalizing_Machine_Learning/blob/main/Images/rundetails%20widget.png)

## Screen Recording
https://youtu.be/-A6HbIA9p4g
